# Labb8
Labb8
Issa Sheikh Haddadin


#syntaxkontroll




from wordqueue import Wordqueue
import string


class Syntaxfel (Exeception):
        pass


def läsFormel(ordkö):
        läsAtom(ordkö)
        if ordkö.peek() == ".":
                ordkö.dequeue()
            else:
                läsNum(ordkö)
                läsFormel(ordkö)
def läsAtom(ordkö):
        läsLETTER(ordkö)
        läsLetter(ordkö)


def läsLETTER(ordkö):
        bokstav = ordkö.dequeue()
        lista = set("ABCDEFGHIJKLMNOPRSTUVWXYZ")
        if bokstav in lista:
                return
       
        raise Syntaxfel("Saknad stor bokstav vid radslutet")
def läsLetter(ordkö):
        bokstav = ordkö.dequeue()
        lista1 = set("abcdefghijklmnoprstuvwxyx")
        if bokstav in lista1:
                return
        raise Syntaxfel("Saknad stor bokstav vid radslutet")




def läsNum(ordkö):
        tecken = ordkö.dequeue()
        if tecken in string.digits:
                return
        raise Syntaxfel("För litet tal vid radslutet")








def main():


Formel = input("- Skriv en formel")


while Formel:
   


    Formel = input("- Skriv en formel")
       
main()
