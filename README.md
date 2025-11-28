<pre>
  #include <iostream>

using namespace std;

//x(t) = t^2 ve y(t) = t^3 - 3t parametrik denklemleriyle verilen eğrinin
//t = 2 noktasındaki teğetinin eğimi (dy / dx) kaçtır?
double parametric_slope_q7(double t)
{
    //(dy/dt)*(dt/dx) = (dy/dt) / (dx/dt) = (3t^2 - 3) / (2t)
    double numerator = 3.0 * t * t - 3.0;
    double denominator = 2.0 * t;

    // t = 0 için tanımsızlık kontrolü
    if (denominator == 0.0)
    {
        return NAN; // Tanımsız
    }

    return numerator / denominator;
}

int main()
{
    const double T_VALUE = 2.0;
    double result_q7 = parametric_slope_q7(T_VALUE);

    cout << "dy/dx = (3t^2 - 3) / (2t)" << endl;
    cout <<  " t = 2 noktasındaki teğetin eğimi = 9/4 " << endl;

    return 0;
}
</pre>
