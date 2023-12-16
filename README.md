# ios-uibarbuttonitem-action-swift
## [ios uibarbuttonitem action swift](https://stackoverflow.com/questions/65153645/uibarbuttonitem-with-sf-symbols-displays-smaller-than-systemitem-in-the-navigati) <br><br>
```swift

override func viewDidLoad() {
        super.viewDidLoad()

  // Do any additional setup after loading the view.
        let rightBarButtonItem = UIBarButtonItem(title: "< Back", style: .plain, target: self, action: #selector(rightBarButtonItemTapped))
      
        self.navigationItem.leftBarButtonItem = rightBarButtonItem
    }
    
    @objc func rightBarButtonItemTapped() {
        // Show the navigation bar
        self.navigationController?.isNavigationBarHidden = false
        let allFilesViewController = HomeViewController.makeSelf()
                       
        DispatchQueue.main.async {
            self.navigationController?.pushViewController(allFilesViewController, animated: true)
        }
        

        
    }

```
