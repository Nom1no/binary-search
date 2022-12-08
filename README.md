# Practical-and-homework
class Phone {
    constructor (yearOfCreation, memory, price) {
        this.yearOfCreation = yearOfCreation;
        this.memory = memory;
        this.price = price;
    }

    calculatePrice() {
        return Math.round((this.price)/ 36.6);
    }

    calculateAge() {
        return 2022 - this.yearOfCreation;
    }

    description() {
        return `This is ${this.nameClass}, he is ${(this.calculateAge())} year old and costs ${(this.calculatePrice())} dollars`
    }
}

class Asus extends Phone {
    constructor (yearOfCreation, memory, price, color = 'silver', nameClass = 'Asus') {
        super (yearOfCreation, memory, price)
        this.color = color;
        this.nameClass = nameClass;
    }
}

class Samsung extends Phone {
    constructor (yearOfCreation, memory, price, color = 'white', nameClass = 'Samsung') {
        super (yearOfCreation, memory, price)
        this.color = color;
        this.nameClass = nameClass;
    }
}

class Xiaomi extends Phone {
    constructor (yearOfCreation, memory, price, color = 'pink', nameClass = 'Xiaomi') {
        super (yearOfCreation, memory, price)
        this.color = color;
        this.nameClass = nameClass;
    }
}

const asus = new Asus(2019, 128,17000 )
const samsung = new Samsung(2020, 256, 25000)
const xiaomi = new Xiaomi(2022, 64, 27000)


console.log (asus.description() + '\n', samsung.description() + '\n', xiaomi.description() + '\n')
