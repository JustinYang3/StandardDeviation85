# StandardDeviation85
int [] nums = new int [51];
        Scanner scan = new Scanner(System.in);

        //scans for integer
        System.out.println("Enter any number [-1 to quit]: ");
        int num = scan.nextInt();
        int sum = 0;
        float mean = 0;
        int count = 0;
        float sd = 0;
        float sum2 = 0;
        float deviation = 0;

        //keeps taking in values into the array until sentinel value is inputted
        //while also keeping track of count
        while (num!=-1)
        {
            nums[count] = num;
            sum = sum + num;
            System.out.println("Enter another integer: ");
            num = scan.nextInt();
            count++;
        }
        //finds mean value
        mean = (float)sum / (float)count;

        //finds numerator of standard deviation
        for (int i = 0; i<count; i++)
        {
            sum2 = (float) Math.pow(nums[i] - mean,2);
            sd = sum2 + sd;
        }

        //finds standard deviation
        deviation = (float) Math.sqrt(sd/count);
        //prints mean and standard deviation out
        System.out.println("Standard Deviation is: " +deviation);
        System.out.println("Mean is: "+mean);
    }
