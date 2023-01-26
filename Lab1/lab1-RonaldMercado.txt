import Foundation

/*
IOS Developent
Ronald M. Mercado H.
Lab 1 - BMI Calculation
21 Jan 2023
LaSalle College
*/

// Body Mass Index Program

// Data - Arrays
let firstName : Array<String> = ["Daniel", "Mark", "Sam", "Pierre","Jean"]
let lastName : Array<String> = ["Carvalho", "Zukemberg", "Smith", "Olivier", "Francois"]
let height : Array<Int> = [174, 178, 166, 182, 177] // in centimeters
let weight : Array<Double> = [82.5, 78.2, 120.0, 71.2, 92.9] // in kg

// Operations
// Iteration over arrays

for i in 0..<firstName.count {    
  let fullName = firstName[i] + " " + lastName[i] 
  let height = Double(height[i])
  let weight = weight[i]
  let bmi = weight / pow(height/100, 2)
  let category:String

  // Validation
  category = bmi < 18.5 ? "Underweight" : (bmi < 25.0 ? "Normal weight" : (bmi < 30.0 ? "Overweight" : "Obesity"))   

  //Output
  
  print("Patient number \(i + 1) : \(fullName)\n - Height : \(String(format: "%.f", height)) cm \n - Weight : \(weight) kg \n - BMI : \(String(format: "%.1f", bmi)) \n - Classification : \(category)")    
  print ("----------------------------------------------")
}
