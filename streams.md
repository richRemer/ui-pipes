Standard Streams
================
 * `fd0` standard input
 * `fd1` standard output
 * `fd2` standard error

Extended Streams
================
 * `fd6` document input
 * `fd7` document output
 * `fd8` object input
 * `fd9` object output

Document Streams
----------------
 * framed messages
 * similar to HTTP response stream
   * supported headers
     * Document-Ident: <ident>
     * Document-Continuation: (continues|continued|complete)
     * Content-Range: <range>
     * Content-Length: <bytes>
     * Content-Type: <media-type>
     * Trailer: <header>
     * Transfer-Encoding: <encoding>
   * partial results for multi-plexing
     * initial partial document
       * Document-Ident: dh23b
       * Transfer-Encoding: chunked
       * Trailer: Document-Continuation
       * ...data, data, data...
       * 0
       * Document-Continuation: continues
     * intermediary partial document
       * Document-Ident: dh23b
       * Document-Continuation: continued
       * Transfer-Encoding: chunked
       * Trailer: Document-Continuation
       * ...data, data, data...
       * 0
       * Document-Continuation: continues
     * final partial document
       * Document-Ident: dh23b
       * Document-Continuation: continued
       * Transfer-Encoding: chunked
       * Trailer: Document-Continuation
       * ...data, data, data...
       * 0
       * Document-Continuation: continues

Object Streams
--------------
 * line-based
 * JSON objects
   * strict objects
   * extended
     * numbers
     * strings
     * booleans
     * null
     * arrays
