# Bisection
I do not have the code for the bisection yet.

function [c, rootError] = Bisection(f,a,b,esp)

  %midpoint
  c = (a+b)/2;
  %Initialise the number of iterations
  niter = 0;

  while(abs(f(c)) > esp) && (niter < 100)
    if f(c)*f(b) < 0;
      a = c;
    else 
      b = c;
    end

    c = (a+b)/2;
    niter = niter + 1;
  end

  rooterror = abs(f(c) - 0)

  if niter >= 100
    disp('Error')
  end
end
