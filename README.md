# zkdao
Zero-Knowledge DAO. Also a meritocracy, TBH (meridao?).

 * Issue public ERC20 tokens via ICO (a la DAO 1.0)
 * zkDAO smart contract instantiated with link to public zkShare and funds raised during ICO
 * AZTEC note registry converts pubShares to zkShares
 * Votes are based on proving you own a certain number of shares 
 * Voting is different, to account for the privacy of notes:
   * Commit period: where we commit to our voting position. This simplifies logic/security around shares being transferred and 'double-voting'.
   * Reveal period: where we reveal an AZTEC ACE dividend proof (proof of shares we've voted with), and the proof that we committed to it earlier
   * Each reveal of an amount allows us to sum the 'votes' and do quorum-based voting
