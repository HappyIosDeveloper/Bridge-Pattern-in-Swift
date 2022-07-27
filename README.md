# Bridge Pattern in Swift

## Simple bridge design pattern written in Swift

    import Foundation
    
    protocol CarSystem {
    
        var ownerName: String { get set }
    
        func startEngine()
    }
    
    class Car: CarSystem {
    
        var ownerName: String
    
        func startEngine() {
            print("engine started for \(ownerName) car")
        }
    
        init(ownerName: String) {
            self.ownerName = ownerName
        }
    }
    
    class MotorCycle: CarSystem {
    
        var ownerName: String
    
        func startEngine() {
            print("engine started for \(ownerName) morocycle")
        }
    
        init(ownerName: String) {
            self.ownerName = ownerName
        }
    }
    
    var lamborgini = Car(ownerName: "Jack")
    lamborgini.startEngine()
    
    var ferrari = Car(ownerName: "John")
    ferrari.startEngine()
    
    var ducati = MotorCycle(ownerName: "Ahmadreza")
    ducati.startEngine()
    
    
    
    // MARK: Output:
    // engine started for Jack car
    // engine started for John car
    // engine started for Ahmadreza motorcycle
    
    
