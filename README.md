# ts-freak

Plot frequency of events from a list of timestamps.


## Requirements
- gnuplot

## Usage

*Note: Current expected timestamp format 'YYYY-MM-DD'*

`./tsf <ts_file`

Example usage in a processing pipe:
`sed s/<strips all text after ts>// log_file | ./tsf`

Example output:
```
 25 ++-+---+--+---+--+---+--+--+--+---+--+---+--+--+--+---+--+---+--+--+---+--+--+---+--+---+-++   
     +         +          +        +          +        +          +         +         +         +   
     |                                                      **********    Timestamp freq ****** |   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
  20 ++                                                     *        *                         ++   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
     |                                                      *        *                          |   
  15 ++                                 **********          *        *                         ++   
     |                                  *        *          *        *                          |   
     |              *********************        *          *        *                          |   
     |              *        **        **        *          *        *          **********      |   
     |              *        **        **        *          *        *          *        *      |   
     |    ***********        **        **        *          *        ************        *      |   
     |    *        **        **        **        *          *        **        **        *      |   
     |    *        **        **        **        *          *        **        **        *      |   
  10 ++   *        **        **        **        ************        **        **        *     ++   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
   5 ++   *        **        **        **        **        **        **        **        *     ++   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     |    *        **        **        **        **        **        **        **        *      |   
     +    *    +   **     +  **    +   **     +  **    +   **     +  **     +  **     +  *      +   
   0 ++-+-********************************************************************************---+-++   
          2016-01-01 2016-02-02016-03-01 2016-04-02016-05-01 2016-06-012016-07-012016-08-02016-09-01

```
