

# UIPickerView Example swift.
![Preview](./src/assets/icon.png)



### ViewController Class.

,,, 

import UIKit
class ViewController: UIViewController, UIPickerViewDataSource, UIPickerViewDelegate {
    

    @IBOutlet weak var pickerView: UIPickerView!
    
    
     let currencyArray = ["AUD", "BRL","CAD","CNY","EUR","GBP","HKD","IDR","ILS","INR","JPY","MXN","NOK","NZD","PLN","RON","RUB","SEK","SGD","USD","ZAR"]

    override func viewDidLoad() {
        super.viewDidLoad()
        
        pickerView.dataSource=self
        pickerView.delegate=self

    }

  
    /* total picker view row */
    func numberOfComponents(in pickerView: UIPickerView) -> Int {
        return 1
    }
    
    
    /* total row count*/
    func pickerView(_ pickerView: UIPickerView, numberOfRowsInComponent component: Int) -> Int {
        return currencyArray.count
    }
    
    /* show row view */
      func pickerView(_ pickerView: UIPickerView, titleForRow row: Int, forComponent component: Int) -> String? {
        return currencyArray[row]
    }
    
    /* when click row get index data */
    func pickerView(_ pickerView: UIPickerView, didSelectRow row: Int, inComponent component: Int) {
        print(currencyArray[row])
    }
    
} ,,,

![Preview](./src/assets/inCollage_20180212_202916674.jpg)


Made with ♥ by [Shofikul Islam](https://www.facebook.com/Shofikul1992)
