# Search
  fi  = [0]*26
  se  = [0]*26*26
  th  = [0]*26*26
  cnt = 0
  m   = 0
  n   = 0

  for x in s:
      z = ord(x)-97
      m = 26*z
      n = z

      for y in range(26):
          cnt   += th[m]
          th[n] += se[n]
          se[n] += fi[y]
          m+=1
          n+=26

      fi[z] +=1
  cnt%=1000000007
