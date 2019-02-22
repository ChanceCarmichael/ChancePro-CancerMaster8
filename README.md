# ChancePro-CancerMaster8
A program to aid in the determination of usefulness of screenings

# Question:
  ## Do you smoke tobacco?
    y: what is your age?
       ---n >= 55?
              y:
              n: test to see if below case...
       ---55 >= n <= 80?
              y: are you still smoking?
                 y: when did you start smoking? (n_0)
                    when did you quit smoking? (n_i)
                    how many individual, standard sized tobacco products do you smoke daily? (c_d / 20)
              n: test to see if below case...
       ---80 <= n?
              y:
              n: unreachable state...
    n: EXIT
    
    
    
    cigarettes per day = c_d/20
    years consuming tobacco (c_y) = n_i - n_0
    individual cigarettes per year = (c_y * c_d/20) * 365
      if year%400 = 0 || ((year%4 = 0) && (year%100 != 0)) == true, then year = 366 days
