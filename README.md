# TableViewNotes
Haciendo apuntes para cuando pierda la memoria

## Comenzando 🚀

1.- Crear TableView desde StoryBoard

2.- Crear @IBOutlet hacia ViewController
```
@IBOutlet weak var tableView: UITableView!
```
3.- Declarar delegate y datasource

```
override func viewDidLoad() {
        super.viewDidLoad()
        tableView.delegate = self
        tableView.dataSource = self
        
            }
```
4.- Declarar Array
```
        teams = ["Atletico de Madrid", "Barcelona", "Deportivo de la Coruña", "Las Palmas", "Malaga", "Rayo Vallecano", "Sporting", "Real Sociedad", "Espanyol", "Mallorca", "Valladolid", "Eibar",  "Ponferradina", "Albacete"]
```
5.- Declarar Delegate y Datasource en clase
```
extension ViewController: UITableViewDataSource
extension ViewController: UITableViewDelegate
```
6.- Agregar protocolos para TableView
```
func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {
          return teams.count
    }
func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
        let cell:UITableViewCell = UITableViewCell(style: UITableViewCell.CellStyle.subtitle, reuseIdentifier: "mycell")
        cell.textLabel?.text  = teams[indexPath.row]
        
        cell.imageView!.image = UIImage(named: teams[indexPath.row])!
        return cell
    }
```

## Referencias:
https://www.efectoapple.com/tutorial-introduccion-uitableview/
