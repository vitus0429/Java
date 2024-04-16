import java.util.Scanner;

public class f{
    public static class Point{
        private String N;
        public boolean M = false;

        public void Set(String N){
            this.N = N;
        }
    }

    public static boolean search(Point[][] arr, String[] ans, int i, int j, int now_length, int x, int y){
        if(now_length == ans.length){
            return true;
        }
        boolean now = false;
        if(arr[i][j].N.equals(ans[now_length]) && arr[i][j].M == false){
            arr[i][j].M = true;
            now_length++;
            if(now_length == ans.length){
                return true;
            }
            if(i - 1 >= 0 && !now)now = search(arr, ans, i - 1, j, now_length, x, y);
            if(i + 1 < x && !now)now = search(arr, ans, i + 1, j, now_length, x, y);
            if(j - 1 >= 0 && !now)now = search(arr, ans, i , j - 1, now_length, x, y);
            if(j + 1 < y && !now)now = search(arr, ans, i , j + 1, now_length, x, y);
        }
        if(now){
            return true;
        }
        else{
            return false;
        }
    }

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int x = s.nextInt();
        int y = s.nextInt();
        String t = s.nextLine();
        Point[][] arr = new Point[x][y];
        for(int i = 0; i < x; i++){
            String[] input = s.nextLine().split(" ");
            for(int j = 0; j < y; j++){
                arr[i][j] = new Point();
                arr[i][j].Set(input[j]); 
            }
        }
        String[] ans = s.nextLine().split("(?!^)");
        boolean rr = false;
        for(int i = 0; i < x; i++){
            for(int j = 0; j < y; j++){
                rr = search(arr, ans, i, j, 0, x, y);
                if(rr)break;
            }
            if(rr)break;
        }
        if(rr){
            System.out.println("true");
        }
        else{
            System.out.println("false");
        }
        s.close();
        
    }
}
