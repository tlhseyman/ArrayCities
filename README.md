package sample;

public class CityArrays {
    public static void main(String[] args) {
        String[][] cities = {
                {"Arlington","Richmond","Albany","Mineapolis", "New Jersey"},
                {"Houston", "Charlotte", "Baton Rogue","Oklahoma", "Boulder"},
                {"San Diego", "San Francisco", "Irvine","Miami","Orlando"},
                {"Kansas City", "Atlanta", "New York", "Boston", "Toronto"},
                {"Pittsburg", "Massachuset", "Virginia", "Seattle", "Los Angeles"}
        };
        printCitiesWithFirstLetterA(cities);
        System.err.println("===+++===+++");
        printCityNamesReversed(cities);
        System.err.println("===+++===+++");
        printCitiesBetweenAH(cities);
        System.err.println("===+++===+++");
        printCitiesHasA(cities);
    }

    public static void printCitiesWithFirstLetterA(String[][] cityNames){
        for (int i=0; i<cityNames.length; i++){
            for(int j=0; j<cityNames[i].length; j++){
                String city = cityNames[i][j];
                if(city.charAt(0)=='A'){
                    System.out.println(cityNames[i][j]);

                }

            }
        }
    }

    public static void printCityNamesReversed(String[][] cityNames){
        for(int g=0; g<cityNames.length; g++){
            for(int r=0; r<cityNames[g].length; r++){
                String city = cityNames[r][g];
                System.out.println(cityNames[r][g]);
            }
        }
    }

    public static void printCitiesBetweenAH(String[][] myCities){
        for(int y=0; y<myCities.length; y++){
            for(int g = 0; g < myCities[y].length; g++){
                if(myCities[y][g].charAt(0)>=65 && myCities[y][g].charAt(0)<=72){
                    System.out.println(myCities[y][g]);
                }

            }
        }
    }

    public static void printCitiesHasA(String[][] cities){
        boolean hasA = false;
        for(int i=0; i<cities.length; i++){
            for(int j=0; j<cities[i].length; j++){
                for(int k=0; k<cities[i][j].length(); k++){
                    if(cities[i][j].charAt(k)=='a'){
                        hasA = true;
                    }
                }
                if (hasA){
                    System.out.println(cities[i][j]);
                }
                hasA = false;
            }
        }
    }
}
