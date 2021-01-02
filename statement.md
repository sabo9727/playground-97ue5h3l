

using System;
using System.Collections.Generic;
using System.Linq;

class Hello 
{
    static void Main() 
    {
        List<string> animalNames = new List<string> {"fawn", "gibbon", "heron", "ibex", "jackalope"};

        IEnumerable<T> longAnimalNames = 
        from names in animalNames 
        where names.Length >= 5 
        orderby names.Length
        select names;

        Console.WriteLine(longAnimalNames);
    }
}


