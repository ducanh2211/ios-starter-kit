# How to create an init method

```swift
class OnboardingViewController : UIViewController {

    var titleLabel: UILabel = {
        let label = UILabel()
        label.translatesAutoresizingMaskIntoConstraints = false
//        label.text = "Your bill, your way"
        label.textAlignment = .center
        label.textColor = .black
        label.font = UIFont.boldSystemFont(ofSize: 28)

        return label
    }()
    
    init(titleText: String) {
        self.titleLabel.text = titleText
        super.init(nibName: nil, bundle: nil)
    }

    required init?(coder aDecoder: NSCoder) {
        super.init(coder: aDecoder)
    }
    
    // use like this
    class ViewController1: OnboardingViewController {...}
    
    let vc1 = ViewController1(titleText: "Your bill, your way")
```