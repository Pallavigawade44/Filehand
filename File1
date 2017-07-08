/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package filehandling;

import java.io.BufferedReader;
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.sql.Connection;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.util.Scanner;
import javax.swing.JOptionPane;

/**
 *
 * @author Admin
 */
public class Filehandling {
 
    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
      
     
           Connectivity con1=new Connectivity();
            Connection con2=con1.getConnection();
            
     BufferedReader br=null;
     String line=null;
     String str=null;
     String arr[];
     StringBuffer contain1=new StringBuffer();
     
     //System.out.println("Plz enter file name to be read");
     try
     {
         File f=new File("C:\\Users\\Admin\\Desktop\\Result_Result for Dr.txt" );
         
         br=new BufferedReader(new FileReader("C:\\Users\\Admin\\Desktop\\Result_Result for Dr.txt" ));
     String id=null;
     String name=f.getName();
      System.out.println(name);
        while((line = br.readLine())!=null){
           // System.out.println(line);
           
         contain1.append(line);
        }
        
         PreparedStatement ps=con2.prepareStatement("insert into fileorg(Name ,Content)"+" values(?,?)");
         
         ps.setString(1,name);
         ps.setString(2,contain1.toString());
         ps.executeUpdate();
         
       
                 
         
         
         


// System.out.println(line);
     }      
                catch(Exception e)
     {
         e.printStackTrace();
     }
      }
     
    
    
}
