#Iterators

Using Iterators in ArrayList and HashMap

#ScreenShot

![Iterators](Iterators.png)

#Code

~~~
package ph.edu.dlsu;

import java.util.*;

public class Main {

    public static void main(String[] args) {

        ArrayList<String> list = new ArrayList<String>();

        list.add("California");
        list.add("Oregon");
        list.add("Washington");
        System.out.println(list);

        ListIterator<String> listIterator = list.listIterator();
        while (listIterator.hasNext()){
            String value = listIterator.next();
            System.out.println(value);
        }

        HashMap<String, String> map = new HashMap<String, String>();

        map.put("California", "Sacramento");
        map.put("Oregon", "Salem");
        map.put("Washington", "Olympia");
        System.out.println(map);

        Set<String> keys = map.keySet();
        Iterator<String> iterator = keys.iterator();
        while (iterator.hasNext()){
            String value = iterator.next();
            System.out.println("The capital of " + value + " is " + map.get(value));
        }

    }
}
~~~
