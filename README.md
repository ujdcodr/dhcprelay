A C++ program that convert from Felix's connection vector format to a format more
suitable for reading by tmix-ns
  - replaces t, >, < lines with line with format:
  * {I,A} - initator or acceptor
  * time to wait after sending (usecs)
  * time to wait after receiving (usecs)
  * bytes to send (if 0, send a FIN)

 EXAMPLES:
  > 826             I   0    0    826
  t 534             A   0    534  1213
  < 1213            A   872  0    0
  t 872

  c< 190            A   0    0    190
  t< 505            I   0    0    396
  c> 396            A   505  0    46
  t> 6250           I   6250 0    0
  c< 46
