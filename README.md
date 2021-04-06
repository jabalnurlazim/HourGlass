# HourGlass



public static void hourGlass(int size) {
    int dimension = (size * 2) - 1, space = 0, stars = size - 1, printed = 0;
    for(int i=0; i<dimension; i++) {
        int actual = space;
        for (int j = dimension; j > 0; j--) {
            if (actual > 0) {
                System.out.print(" ");
                actual--;
            } else {
                System.out.print("*");
                if (stars == printed) {
                    actual = space;
                    printed = 0;
                } else {
                    actual = 1;
                    printed++;
                }
            }
        }
        if (i <= size - 2) { // will pattern spaces and stars from top to middle
            space++;
            stars--;
        } else { // will pattern spaces and stars from middle to top
            space--;
            stars++;
        }
        System.out.println();
    }
}

public static void main(String[] args) {
    hourGlass(7);
}
