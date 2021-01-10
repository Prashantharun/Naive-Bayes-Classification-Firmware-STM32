Project : Navive Bayes Classifier
Developer : Prashanth
Date : 8/Jan/2021

                          ***************README****************

1) Program Routine :

As per the requirement i need to write a algorithm to perform Naive Bayes Classifier with 10ms delay and without performance loss.

                             P(B|A) P(A)
*    Naive Bayes : P(A|B) = ----------------
                                 P(B)

*    Library Used : CMSIS DSP library for ARM series.


*    Core : ARM cortex M0.

I have used the following API's for Prediction:

1) arm_gaussian_naive_bayes_predict_f32(&S, in, result);

--> This API is used for the prediction of Naive Bayes from the CMSIS DSP library.

2) arm_max_f32(result, NB_OF_CLASSES, &maxProba, &index);

--> This API is used to obtain the max value of results.

3) HAL_Delay(10);

--> This API is used to provide a 10ms delay.

--------------------------------------------------------------------------------------------------------------------------------------

2) Clock Configuration : 

* A high speed external clock is used for performance.

* Clock frequency : 8 Mhz.

* Clock frequency is decided based on :
 
  a) Instructions per clock. 
  b) Core count : Single Core MCU.
  c) Multithreaded Application : No.

--------------------------------------------------------------------------------------------------------------------------------------

3) Power Consumption :

* A 5V 2A supply would make the core run without performance loss.




