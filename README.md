# polymorphism
polymorphism about Animals
package com.company;

abstract class Animal {
    protected String name;

    public Animal(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }

    public abstract void eating();

    public String toString() {
        return name;
    }
}

class Birds extends Animal {
    protected String name;

    public Birds(String name) {
        super(name);
    }

    @Override
    public void eating() {
        System.out.println("Eating: Eat Nuts");
    }

    public void fly() {
        System.out.println("Move: Fly");
    }

    public String toString() {
        return name;
    }
}

class Cattle extends Animal {
    protected String name;

    public Cattle(String name) {
        super(name);
    }

    public void run() {
        System.out.println("Move: Run");
    }

    @Override
    public void eating() {
        System.out.println("Eating: Eat grass");
    }

    public String toString() {
        return name;
    }
}


public class main1 {
    public static void main(String[] args) {
        Birds birds1 = new Birds("birds1");
        System.out.println(birds1.getName());
        birds1.eating();
        birds1.fly();
        System.out.println("the Class is: " + birds1.getClass().getSimpleName());
        if (birds1 instanceof Birds) {
            System.out.println(false + ", The Bird1 is instance of Cattle");
        }
        System.out.println("______________________");

        Birds birds2 = new Birds("birds2");
        System.out.println(birds2.getName());
        birds2.fly();
        birds2.eating();
        System.out.println("the Class is: " + birds2.getClass().getSimpleName());
        if (birds2 instanceof Birds) {
            System.out.println(false + ", The Bird2 is instance of Cattle");
        }
        System.out.println("______________________");

        Cattle cattle1 = new Cattle("cattle1");
        System.out.println(cattle1.getName());
        cattle1.eating();
        cattle1.run();
        System.out.println("the Class is: " + cattle1.getClass().getSimpleName());
        if (cattle1 instanceof Cattle) {
            System.out.println(true + ", The cattle1 is instance of Cattle");
        }
        System.out.println("______________________");

        Cattle cattle2 = new Cattle("cattle2");
        System.out.println(cattle2.getName());
        cattle1.eating();
        cattle1.run();
        System.out.println("the Class is: " + cattle2.getClass().getSimpleName());
        if (cattle2 instanceof Cattle) {
            System.out.println(true + ", The cattle1 is instance of Cattle");
        }
        System.out.println("______________________");

        Cattle cattle3 = new Cattle("cattle3");
        System.out.println(cattle3.getName());
        cattle1.eating();
        cattle1.run();
        System.out.println("the Class is: " + cattle3.getClass().getSimpleName());
        if (cattle3 instanceof Cattle) {
            System.out.println(true + ", The cattle3 is instance of Cattle");
        }
        System.out.println("______________________");
