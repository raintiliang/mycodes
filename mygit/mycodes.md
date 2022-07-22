###计算时间
struct timeval T_Begin, T_End;
#define TIME_START(T_Begin)  {gettimeofday(&T_Begin, NULL);}
#define TIME_END(T_Begin, T_End)    do{\
   gettimeofday(&T_End, NULL);\
   double T_us = 1000000.0f * (T_End.tv_sec - T_Begin.tv_sec) + (T_End.tv_usec - T_Begin.tv_usec) ;\
   printf("%s %d cal time %lu us \n", __FUNCTION__, __LINE__, T_us);fflush(stdout);\
}while(0);
