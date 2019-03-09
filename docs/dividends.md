
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



encoderFactory.encodeInputOwners = (inputOwners) => {
    const { length } = inputOwners;
    const ownerStrings = inputOwners.map(o => padLeft(o.slice(2), 64));
    const data = [padLeft(Number(length).toString(16), 64), ...ownerStrings].join('');
    return {
        data,
        length: Number(data.length / 2),
    };
};



inputCoder.dividendComputation = (proofData, challenge, za, zb, inputOwners, outputOwners, metadata) => {
    const configs = {
        CHALLENGE: challenge.slice(2),
        ZA: padLeft(Number(za).toString(16), 64),
        ZB: padLeft(Number(zb).toString(16), 64),
        PROOF_DATA: encoderFactory.encodeProofData(proofData),
        INPUT_OWNERS: encoderFactory.encodeInputOwners(inputOwners),
        OUTPUT_OWNERS: encoderFactory.encodeOutputOwners(outputOwners),
        METADATA: encoderFactory.encodeMetadata(metadata),
    };

    const abiParams = [
        'PROOF_DATA',
        'INPUT_OWNERS',
        'OUTPUT_OWNERS',
        'METADATA',
    ];

    return encoderFactory.encode(configs, abiParams, 'dividendComputation');



            /**
             * New calldata map
             * 0x04:0x24      = calldata location of proofData byte array  // proof data byte array
             * 0x24:0x44      = message sender // address
             * 0x44:0x64      = h_x     // crs
             * 0x64:0x84      = h_y     // crs
             * 0x84:0xa4      = t2_x0   // crs
             * 0xa4:0xc4      = t2_x1   // crs
             * 0xc4:0xe4      = t2_y0   // crs
             * 0xe4:0x104     = t2_y1   // crs
             * 0x104:0x124    = length of proofData byte array
             * 0x124:0x144    = challenge
             * 0x144:0x164    = za
             * 0x164:0x184    = zb
             * 0x184:0x1a4    = offset in byte array to notes
             * 0x1a4:0x1c4    = offset in byte array to inputOwners
             * 0x1c4:0x1e4    = offset in byte array to outputOwners
             * 0x1e4:0x204    = offset in byte array to metadata
             */ 



             /*
                ///////////////////////////////////////////  SETUP  //////////////////////////////////////////////
                */
                mstore(0x80, calldataload(0x44))
                mstore(0xa0, calldataload(0x64))
                let notes := add(0x104, calldataload(0x184))
                let n := calldataload(notes)
                let gen_order := 0x30644e72e131a029b85045b68181585d2833e84879b9709143e1f593f0000001                
                let challenge := mod(calldataload(0x124), gen_order)





                