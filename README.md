# collection-framework-hashmap-and-hashtable
package collection.framework.hash.map.and.hash.table;
import java.util.HashMap;
import java.util.Hashtable;
import java.util.Map;
import java.util.Scanner;
/**
 *
 * @author 1BSCCSA44
 */
public class CollectionFrameworkHashMapAndHashTable {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
 Map<String, Integer> hashMap = new HashMap<>();
Map<String, Integer> hashtable = new Hashtable<>();     
Scanner scanner = new Scanner(System.in);
System.out.print("Enter key-value pairs (key1=value1 key2=value2 ...);");
String input = scanner.nextLine();
// Parse the input string and add key-value pairs to both maps
String[] keyValuePairs = input.split("\\s+");
for (String pair : keyValuePairs) {
String[] keyValue = pair.split("=");
if (keyValue.length == 2) {
String key = keyValue[0];
int value = Integer.parseInt(keyValue[1]);
hashMap.put(key, value);
hashtable.put(key, value);
}
}
// Print keys and values of both maps
System.out.println("HashMap:" + hashMap);
System.out.println("Hashtable: " + hashtable);
// Close the scanner to avoid resource leaks
scanner.close();

        // TODO code application logic here
    }
    
}
output
Enter key-value pairs (key1=value1 key2=value2 ...);1  2
HashMap:{}
Hashtable: {}
BUILD SUCCESSFUL (total time: 10 seconds)


