# arrays
Creating, Accessing, Editing Arrays, iterations

import UIKit

// Arrays - Массивы

var visitedCities: [String] = ["Bishkek", "Istanbul", "Munich", "New York"]
let cities: [String] = ["Ankara", "New Jersey", "Dublin", "Toronto"]

var intArray: [Int] = [20, 32, 44, 20, 1, 35]
var doubleArray: [Double] = [1.5, 22.3, 5, 45.0]
var tupleArray: [(String, String)] = [("Aslan", "Arapbaev"), ("Donald", "Trump")]
var boolArray: [Bool] = [true, true, false]

//Использование вывода типа

var countries = ["Турция", "США", "Кыргызстан"]
var oddNumbers = [1,3,5,7,9]


// Доступ к элементам массива

let visitedCountries = ["Турция", "США", "Кыргызстан"]

print("Первым делом я полетел в \(visitedCountries[0])")
print("После я побывал в \(visitedCountries[1])")
print("И затем прилетел в \(visitedCountries[2])")
//print("А еще я хочу побывать в \(visitedCountries[3])")    // ERROR: Index out of range


// Добавление элементов в массив

var myVisitedCountries = ["Турция", "США", "Кыргызстан"]

myVisitedCountries.append("Франция")

myVisitedCountries.insert("Германия", at: 1)


// Объединение массивов

let fruits = ["банан", "киви", "черника"]
let liquids = ["мед", "йогурт"]

var smoothie = fruits + liquids

smoothie += ["грецкий орех"]
//smoothie += "грецкий орех"   // ERROR


// Удаление элементов из массива

var shoppingList = ["чеснок", "лимон", "мука", "туалетная бумага"]

let purchasedItem = shoppingList.removeLast()
shoppingList

let notGoingToPurchase = shoppingList.remove(at: 0)
shoppingList


shoppingList.removeAll()
shoppingList

//shoppingList.remove(at: 2)   //ERROR



// Замена элементов в массиве

var wildAnimals = ["Лев", "Слон", "Кошка", "Коза"]

wildAnimals[2] = "Зебра"
wildAnimals[3] = "Тигр"
wildAnimals

//wildAnimals[4] = "Кенгуру"   //ERROR



// Использование свойств массива

let myFriends = ["Манас", "Самат", "Медер"]

if myFriends.isEmpty {    // false
    print("У меня нет друзей.")
} else {
    print("У меня \(myFriends.count) друзей.")  // 3
}

// Обход циклом элементов массива

let pizzaToppings = ["Сыр", "Томат", "Пепперони", "Сосиски", "Грибы", "Лук", "Ананас"]

for topping in pizzaToppings {
    print(topping)
}


let myNumbers = [2, 5, 8, 12, 15, 20, 30]

for number in myNumbers {
    print("\(number) в квадрате равно \(number * number)")
}


// Some extra methods

var anyNumbers = [10, 2, 3, 43, 5]

let minNumber = anyNumbers.min()
let maxNumber = anyNumbers.max()

let firstNumber = anyNumbers.first
let lastNumber = anyNumbers.last

anyNumbers.contains(3)
anyNumbers.contains(22)

anyNumbers.sort() // массив изменился

var characters = ["c", "b", "a", "z", "x", "y"]


let sortedCharacters = characters.sorted()
print(sortedCharacters)
print(characters)  // не изменился


for (index, country) in myVisitedCountries.enumerated() {
    print("\(index + 1) - \(country)")
}

