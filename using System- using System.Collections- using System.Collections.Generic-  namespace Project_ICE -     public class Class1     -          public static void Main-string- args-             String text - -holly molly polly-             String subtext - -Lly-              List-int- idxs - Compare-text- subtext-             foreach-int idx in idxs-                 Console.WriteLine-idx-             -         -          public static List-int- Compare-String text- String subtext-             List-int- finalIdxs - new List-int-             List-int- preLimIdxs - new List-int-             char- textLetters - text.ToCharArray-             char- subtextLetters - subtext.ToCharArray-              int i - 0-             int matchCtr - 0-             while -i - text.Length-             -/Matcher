using System;
using System.Collections;
using System.Collections.Generic;

namespace Project_ICE
{
    public class Class1
    {

        public static void Main(string[] args){
            String text = "holly molly polly";
            String subtext = "Lly";

            List<int> idxs = Compare(text, subtext);
            foreach(int idx in idxs){
                Console.WriteLine(idx);
            }
        }

        public static List<int> Compare(String text, String subtext){
            List<int> finalIdxs = new List<int>();
            List<int> preLimIdxs = new List<int>();
            char[] textLetters = text.ToCharArray();
            char[] subtextLetters = subtext.ToCharArray();

            int i = 0;
            int matchCtr = 0;
            while (i < text.Length)
            {
                /// Make both letters lower case
                char lowSubtext = Char.ToLower(subtextLetters[matchCtr]);
                char lowText = Char.ToLower(textLetters[i]);

                if (lowSubtext == lowText)
                {
                    if (matchCtr == 0)
                    {
                        preLimIdxs.Add(i);
                    }

                    matchCtr++;

                    if (matchCtr == subtextLetters.Length)
                    {
                        finalIdxs.Add(preLimIdxs[0]);
                        preLimIdxs.Clear();
                        matchCtr = 0;
                    }

                    else
                    {
                        preLimIdxs.Clear();
                        matchCtr = 0;
                    }
                    i++;
                }
            }
            return finalIdxs;
        }
    }
}
