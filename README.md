# ztp
HENTO
import java.util.ArrayList;
import java.util.List;

public class TeaProject {
    
    private List<Tea> teas;
    
    public TeaProject() {
        this.teas = new ArrayList<>();
    }
    
    public void addTea(Tea tea) {
        teas.add(tea);
    }
    
    public void removeTea(Tea tea) {
        teas.remove(tea);
    }
    
    public List<Tea> getTeas() {
        return teas;
    }
    
    public static void main(String[] args) {
        TeaProject project = new TeaProject();
        
        Tea greenTea = new Tea("Green Tea", "China", 2.50);
        Tea blackTea = new Tea("Black Tea", "India", 3.00);
        
        project.addTea(greenTea);
        project.addTea(blackTea);
        
        List<Tea> teaList = project.getTeas();
        
        for(Tea tea : teaList) {
            System.out.println(tea.getName() + " from " + tea.getOrigin() + " - Price: $" + tea.getPrice());
        }
    }

}

class Tea {
    
    private String name;
    private String origin;
    private double price;
    
    public Tea(String name, String origin, double price) {
        this.name = name;
        this.origin = origin;
        this.price = price;
    }
    
    public String getName() {
        return name;
    }
    
    public String getOrigin() {
        return origin;
    }
    
    public double getPrice() {
        return price;
    }
}
