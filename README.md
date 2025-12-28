# shiny-fiesta

trash repo

this was added for trash purposes

TechniciansViewController:

import UIKit

class TechniciansViewController: UITableViewController {
    
    enum Availability {
        case available
        case busy
    }
    
    struct Technician {
        let name: String
        let availability: Availability
        let tasks: Int
        let hours: String
    }
    
    private var technicians: [Technician] = [
        .init(name: "Ali Fadhel", availability: .available, tasks: 142, hours: "6:00 - 12:00"),
        .init(name: "Fatema Hasan", availability: .busy, tasks: 98, hours: "12:00 - 18:00"),
        .init(name: "Fatima Ali", availability: .busy, tasks: 187, hours: "18:00 - 24:00")
    ]
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        tableView.separatorStyle = .none
        tableView.rowHeight = UITableView.automaticDimension
        tableView.estimatedRowHeight = 160
    }
    
    override func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
        technicians.count
    }
    
    override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
        guard let cell = tableView.dequeueReusableCell(withIdentifier: "TechnicianCardCell", for: indexPath) as? TechnicianCardCell else {
            return UITableViewCell()
        }
        
        let tech = technicians[indexPath.row]
        
        cell.nameLabel.text = tech.name
        cell.tasksValueLabel.text = "\(tech.tasks)"
        cell.hoursValueLabel.text = tech.hours
        
        switch tech.availability {
        case .available:
            cell.statusLabel.text = "Available"
            cell.statusLabel.backgroundColor = UIColor.systemBlue
            cell.dotView.backgroundColor = UIColor.systemBlue
        case .busy:
            cell.statusLabel.text = "busy"
            cell.statusLabel.backgroundColor = UIColor.systemRed
            cell.dotView.backgroundColor = UIColor.systemRed
        }
        
        return cell
        
        /*
         // MARK: - Navigation
         
         // In a storyboard-based application, you will often want to do a little preparation before navigation
         override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
         // Get the new view controller using segue.destination.
         // Pass the selected object to the new view controller.
         }
         */
        
    }
}

TechniciansCardCell:

import Foundation
import UIKit

final class TechnicianCardCell: UITableViewCell {
    
    @IBOutlet weak var hoursViewCard: UIView!
    @IBOutlet weak var tasksViewCard: UIView!
    @IBOutlet weak var cardView: UIView!
    @IBOutlet weak var hoursValueLabel: UILabel!
    @IBOutlet weak var tasksValueLabel: UILabel!
    @IBOutlet weak var statusLabel: UILabel!
    @IBOutlet weak var nameLabel: UILabel!
    @IBOutlet weak var dotView: UIView!
    override func awakeFromNib() {
        super.awakeFromNib()
        
        selectionStyle = .none
        
        dotView.layer.cornerRadius = dotView.bounds.height / 2
        dotView.clipsToBounds = true
        
        statusLabel.layer.cornerRadius = 5
        statusLabel.clipsToBounds = true
        
        cardView.layer.cornerRadius = 16
        cardView.layer.masksToBounds = false
        cardView.layer.shadowOpacity = 0.12
        cardView.layer.shadowRadius = 10
        cardView.layer.shadowOffset = CGSize(width: 0, height: 6)
        
        tasksViewCard.layer.cornerRadius = 14
        tasksViewCard.layer.masksToBounds = true
        tasksViewCard.layer.borderWidth = 1
        tasksViewCard.layer.borderColor = UIColor.systemGray5.cgColor
        
        hoursViewCard.layer.cornerRadius = 14
        hoursViewCard.layer.masksToBounds = true
        hoursViewCard.layer.borderWidth = 1
        hoursViewCard.layer.borderColor = UIColor.systemGray5.cgColor
        
        contentView.clipsToBounds = false
        clipsToBounds = false
        
    }
    
    override func layoutSubviews() {
        super.layoutSubviews()
        
        dotView.layer.cornerRadius = dotView.bounds.height / 2
    }
}
