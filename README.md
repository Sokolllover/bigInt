# bigInt
public BigInt divide(BigInt bigInt) {
        BigInt bigintRes = new BigInt();
        BigInt counter = new BigInt();
        int a = bigInt._digits.size();
        int p=1;
        int r = 1;
        if (bigInt == null ){//  || a если само число  null? + 178)
            error("empty bigInt1");
        }
        if(isZero() || compareTo(bigInt) == -1) { // 800 2
            return bigintRes;
        }
        if(bigInt.isZero()){
            error("cannot be divided by 0");
        }
        else {
            for (int i = 0; i <= a; i++) {
                counter.copyOf();
            }
            while (substruct(bigInt.multiply(bigintRes))._positiveSign) {
                while (counter.substruct(bigInt.multiply(p))._positiveSign) {
                    p++;
                }
                bigintRes.addLast(p - 1);
                counter.substruct(bigInt.multiply(p - 1));
                if (ostatok != 0) {
                    counter.clear;
                    counter.addFirst(ostatok);
                }
                else {
                    counter.clear;
                }
                while (counter.size() < a) {
                    counter.addLast([a + r]);
                    r++;
                }
            }
        }
        if(bigInt._positiveSign ^ _positiveSign){
            bigintRes._positiveSign = false;
        }
        else{
            bigintRes._positiveSign = true;

        }
        return bigintRes;
    }



