// MP1: XML Validator
// Implementation of the XMLValidator class.

// You should implement this class.
// You should add comments, documentation comments, and improve the documentation.

using System;
using System.Collections.Generic;
using System.Text;

namespace XMLValidator
{
    public class XMLValidator
    {
        //field(s) here
        private readonly Queue<XMLTag> theTag;

        public XMLValidator()
        {     
            theTag = new Queue<XMLTag>();
        }

        public XMLValidator(Queue<XMLTag> tags)
        {   
            try
            {
                theTag = tags;
            }
            catch(ArgumentException)
            {
                Console.WriteLine("The queue passed is null");
            }
        }

        public void AddTag(XMLTag tag)
        {
            try
            {
                theTag.Enqueue(tag);
            }
            catch(ArgumentException)
            {
                Console.WriteLine("The XMLTag passed is null");
            }
        }

        public string GetTags()
        {
            return null; // return a dummy value for now: ToFix
        }

        public void Remove (string element)
        {
        }

        public void Validate()
        {
        }

    }
}
