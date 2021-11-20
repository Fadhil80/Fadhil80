package replit;

import javafx.application.Application;
import javafx.stage.Stage;
import javafx.scene.Scene;
import javafx.scene.control.Label;
import javafx.scene.control.TextField;
import javafx.scene.control.Button;
import javafx.geometry.Pos;
import javafx.scene.text.Text;
import javafx.scene.layout.GridPane;
import javafx.scene.paint.Color;


public class Main extends Application

{

@Override
public void start(Stage primaryStage) {
        Text orderForm = new Text("Pizza Order");
        orderForm.setFont(javafx.scene.text.Font.font("Gautami", javafx.scene.text.FontWeight.BOLD, 20));

        Label user_id=new Label("Name:");
        Label password = new Label("ID:");
        Label price = new Label("Price:");
        TextField tf1= new TextField();
        TextField tf2= new TextField();
        TextField tf3 = new TextField();
        Button b = new Button("Print Order");

        b.setAlignment(Pos.CENTER);
        GridPane root = new GridPane();
        root.addRow(0,orderForm);
        root.addRow(1, user_id);
        root.addRow(2, tf1);
        root.addRow(3, password);
        root.addRow(4, tf2);
        root.addRow(5, price);
        root.addRow(6, tf3);
        root.addRow(11, b);

        Scene scene=new Scene(root,300,200, Color.GRAY);
        
        primaryStage.setScene(scene);
        primaryStage.setTitle("Online Order Form");
        primaryStage.show();

    }

public static void main(String[] args) {

launch(args);

}

}
