Wspomaganie
===========

...
clc

format compact

format long

f=@(x)(cos(x)+sin(x))/(-sin(x)+cos(x))


x=-2*pi:0.1:2*pi;

y1=x*0;

y=cos(x)+sin(x);

x=x/pi;

plot(x,y,x,y1)

xlabel('x/\pi')

ylabel('?')


x1=0.01*pi;

x0=x1+1;

while abs(x1-x0)>=10^(-3)

    x0=x1;
    
    x1=x0-f(x0);
    
end

i

x1/pi
