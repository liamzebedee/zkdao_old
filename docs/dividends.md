
https://sourcegraph.com/github.com/AztecProtocol/AZTEC/-/blob/packages/protocol/contracts/ACE/validators/dividendComputation/DividendComputation.sol#L151

/*
Enforce the condition k_3 = (k_1)(z_b) - (k_2)(z_a)
*/

https://sourcegraph.com/github.com/AztecProtocol/AZTEC/-/blob/packages/aztec.js/test/proof/dividendComputation/verifier.spec.js#L36




```
/*
Test case:
- k_in = 90
- Interest rate = 5%
- k_out = 4
- k_res = 5
- za = 5
- zb = 100
*/

k = [90, 4, 50]
za = 100
zb = 5

Interest rate = 5%


note A and B
prove B is 5% of A
A = k1 = 90
B = k2 = 4

k3 = k1*zb - k2*za

k3 = 90*5 - 4*100


50 = 90*5 - 4*100
50 = 450 - 400
50 = 50


```