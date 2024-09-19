#include<stdio.h>		//<> 안에 영문 단어 틀리지 않게 조심하기
#include<stdlib.h>		//추가 코드
#include<string.h>
#define p printf

//printf 출력확인하기
#include<stdio.h>		//<> 안에 영문 단어 틀리지 않게 조심하기
#include<stdlib.h>		//추가 코드
#define p printf		//printf를 p로 변경

int main(void)
{
	printf("be happy!\n");
		system("pause");  //추가코드

	return 0;
}

#include<stdio.h>
int main(void)

{
	printf("수업 진행중");
}


#include<stdio.h>
int main(void)
{
	int a,b;
	a = 10;
	b = 20;
	printf(a+b);
	return 0;
}

#include<stdio.h>		//< > 안에 영문 단어 틀리지 않게 조심하기
int main(void)
{
	printf("be happy!\n");
	printf("ABCDEFG");



	return 0;
}



//상수 연산 적용 단. printf가 없어서 출력값은 보이지 않음

int main(void)
{
	10 + 20;

	return;
}

//2024-04-24 교제 57p 예제 2-3 제어문 실습
#include<stdio.h>
int main(void)
{
	printf("be happy!\n");
		printf("1234567890123456789!\n");
		printf("my\tfriend\n");
		printf("goot\bd\ttchance\n");
		printf("cow\rw\a\n");

		return 0;
}

#include<stdio.h>
int main(void)
{
	printf("%d\n", 10);
	printf("%lf\n", 3.4);
	printf("%.1lf\n", 3.45);
	printf("%.10lf\n", 3.4);

	printf("% d과 % d의 합은 % d입니다.\n", 10, 20, 10 + 20);
	printf("%.1lf-%.1lf=%.1lf\n", 3.4, 1.2, 3.4 - 1.2);
	return;
}



#define	PI 3.14
#define R 3
int main()
{
	printf("원주율:%lf,%lf,%lf,%lf\n", PI * PI, R * R, PI * R, 2 * PI * R);
}


#include<stdio.h>
int main(void)
{
	printf("%d\n", 12);		// 10진수로 2글자로 시작하는 상수이다, 10진수는 상수 그대로 적는다
	printf("%d\n", 014);	// 8진수로 0~7까지로 반복한다, 014는 10진수 처럼  보이지만 0은 8진수를나타낸다
	printf("%d\n", 0xc);	// 16진수로0~9까지 표기후 10부터는 a로 표기하며 f까지 존재한다, 0xc에서 0x는 16진수라는것을 나타낸다
	printf("%d\n", 0xff);	// 16진수로0~9까지 표기후 10부터는 a로 표기하며 f까지 존재한다, 0xff에서 0x는 16진수라는것을 나타낸다
							// 또한 ff 라는것은 2진수로 표기시 1111 1111 인것처럼 f 하나가 1111 즉 2진수를 전부를 담당한다
}							

#include<stdio.h>
int main(void)
{
	printf("%.1lf\n", 1e6);			//1e6 이라는지수형태의 실수를 소수점 형태로 출력
	printf("%.7lf\n", 3.14e-5);		//소수점 이하 7자리 까지 출력
	printf("%le\n", 0.0000314);		//소수점 형태를 지수로 표현
	printf("%.2le\n", 0.0000314);	//지수의 형태로 소수점 둘째자리가지 표현
}



#include<stdio.h>
int main(void)
{
	printf("%c\n", 'A');
	printf("%s\n", "A");
	printf("%c은 %s입니다.\n" ,'1',"first");

	return 0;
}


#include<stdio.h>
#include<math.h>
int main(void)
{
	printf("%lf\n", pow(2, 0));
	printf("%lf\n", pow(2, 1));
	printf("%lf\n", pow(2, 10));
	printf("%lf\n", pow(2, 20));
	printf("%lf\n", pow(2, 30));
	printf("%lf\n", pow(2, 32));
	printf("%lf\n", pow(3.14,2.72));
}

#include<stdio.h>

void print_int(int num)
{
	printf("%d : ", num);
	for (int i = 31; i >= 0; i--) {
		if (i % 8 == 7 && i != 31) printf("_");
		printf("%d", (num >> i) & 1);
	}
	printf("\n");
}

void print_double(double dnum)
{
	typedef union _DOUBLE {
		double d;
		int i[2];
	} DOUBLE;

	DOUBLE DNUM = { dnum };
	printf("%lf : ", dnum);
	for (int i = 1; i >= 0; i--) {
		for (int j = 31; j >= 0; j--) {
			if (j % 8 == 7 && !(i == 1 && j == 31)) printf("_");
			printf("%d", (DNUM.i[i] >> j) & 1);
		}
		printf("\n");
	}
}

void print_char(int c)
{
	printf("%c : ", c);
	for (int i = 31; i >= 0; i--) {
		if (i % 8 == 7 && i != 31) printf("_");
		printf("%d", (c >> i) & 1);
	}
	printf("\n");
}

int main()
{
	print_int(-2);
	print_int(10);
	print_double(10.0);
	print_double(-6.5);
	print_char('\n');
	print_char('a');
	print_char('A');
	print_char(65);
	printf("%d\n", sizeof(10));
	printf("%d\n", sizeof(10.0));
	printf("%d\n", sizeof('A'));
	printf("%d\n",'A');
	printf("%d\n", sizeof('a'));
	printf("%d\n",'+');
}


#include<stdio.h>
#define p printf	// 임의적으로 printf를 p로 변환
int main()
{
	int a;			//int를 a로 변환
	int b, c;		//int를 b와 c로 변환
	double da;		//double를 da로 변환
	char ch;		//char를 ch로 변환

	a = 10;
	b = a;
	c = a + 20;
	da = 3.5;
	ch = 'A';

	p("변수 a의 값: %d\n", a);
	p("변수 b의 값: %d\n", b);
	p("변수 c의 값: %d\n", c);
	p("변수 da의 값: %.1lf\n", da);
	p("변수 ch의 값: %c\n", ch);


			//     변수를 저장하는곳  > "a = 10" < 저장되는 변수의 값

}



#include<stdio.h>
#define p printf
int main()
{
	char ch1 = 'A';
	char ch2 = 65;

	p("문자%c의 아스키 코드값: %d\n", ch1, ch1);
	p("아스키 코드값이 %d인 문자: %c\n", ch2, ch2);
}



#include<stdio.h>
#define p printf
int main()
{
	short sh = 32767;
	int in = 214783647;
	long ln = 2147483647;
	long long lln = 123451234512345;

	p("short형의 변수 출력:%d\n", sh);
	p("int형의 변수 출력:%d\n", in);
	p("long형의 변수 출력:%ld\n", ln);
	p("long long형의 변수 출력:%lld\n",lln);

}



#include<stdio.h>
#define p printf
int main()
{
	unsigned int a;
	a = 4294967295;
	p("%d\n", a);
	a = -1;
	p("%u\n", a);

}




#include<stdio.h>
#define p printf

int main(void)
{
	int a, b, c;

	a = 35000000;
	b = 12;
	c = a / b;

	p("%d\n", c);
}


#include<stdio.h>
#define p printf

int main(void)
{
	float ft = 1.234567890123456789;
	double db = 1.234567890123456789;

	p("float형의 변수값:%.20f\n", ft);
	p("double형의 변수값:%.20f\n", db);
}
//
#include<stdio.h>
#define p printf
int main(void)
{
	char fruit[20] = "strawberry";
	p("딸기:%s\n", fruit);
	p("딸기잼:%s %s\n", fruit, "jam");
}
//strcpo 활용하기
#include<stdio.h>
#define p printf
int main(void)
{
	char fruit[20] = "strawberry";
	p("%s\n",fruit);
	strcpy(fruit, "banana");
	p("%s\n", fruit);
}
#include<stdio.h>
#define p printf
int main(void)
{
	int income = 0;
	double tax;
	const double tax_rata = 0.12;
	
	income = 456;
	tax = income * tax_rata;
	p("세금은: %.1lf입니다.\n", tax);
}

#include<stdio.h>
int main()
{
	int a;
	scanf("%d", &a);
	printf("입력된 값 :%d\n", a);

}


//혼자하는 연습

#include<stdio.h>
int main()
{
	int a,b,c,d,e,f,g;
	printf("a에 들어갈 값을 입력해주세요 \n");
	scanf("%d", &a);
	printf("a에 입력된 값 입니다:%d\n", a);

	printf("b에 들어갈 값을 입력해주세요 \n");
	scanf("%d", &b);
	printf("b에 입력된 값 입니다:%d\n", b);

	printf("c에 들어갈 값을 입력해주세요 \n");
	scanf("%d", &c);
	printf("c에 입력된 값 입니다:%d\n", c);

	printf("d에 들어갈 값을 입력해주세요 \n");
	scanf("%d", &d);
	printf("d에 입력된 값 입니다:%d\n", d);

	printf("e에 들어갈 값을 입력해주세요 \n");
	scanf("%d", &e);
	printf("e에 입력된 값 입니다:%d\n", e);

	printf("f에 들어갈 값을 입력해주세요 \n");
	scanf("%d", &f);
	printf("f에 입력된 값 입니다:%d\n", f);

	printf("g에 들어갈 값을 입력해주세요 \n");
	scanf("%d", &g);
	printf("g에 입력된 값 입니다:%d\n", g);
	
	printf(a - b);
}


#include<stdio.h>
int main()
{
	int a = 0;
	a = a + 1;
	a = a + 2;
	a = a + 3;
	printf("a:%d", a);
}



#include<stdio.h>
int main()
{
	int tot;

	int kor = 70;
	int eng = 80;
	int mat = 90;
		
	tot = kor + eng + mat;

	printf("국어:%d점 영어:%d점 수학:%d점\n", kor,eng,mat);
	printf("총점은:%d점\n", tot);
}

#include<stdio.h>
int main()
{
	int age;
	double height;

	printf("나이와 키를 입력하세요: ");
	scanf("%d%lf", &age, &height);
	printf("나이는 %d살 키는 %1.lfcm입니다\n", age, height);
}



#include<stdio.h>
int main()
{
	double a;
	double b;
	double c;
	a = 0.7;
	b = 15;
	c = 120;
	
	printf("지금 남은 높이:%lf\n", c - b);
	printf("남은 컵을 올릴수있는 갯수 %lf\n",(c-b)/a );
}
*/

/*

.
// 어떤 전자제품에 원가에 30%의 이익을 붙여서 정가를 정하였다 이정가에서 20% 할인하여 판매하였더니 이익이 5000원 이상이였다 이전자 제품의 원가는얼마인지 구하시오
#include<stdio.h>
int main()
{
	float a; // 할인값 5000원
	float b; // 20% 할인율 0.8
	float c; // 30% 이익률 1.3
	float d;

	a = 5000;
	b =1.2;
	c = a * b;
	d = 1.3;

	printf("할인 전 가격:%.2f\n", a * b);
	//20% 할인전 가격은 6000원

	printf("원가에서 30퍼센트 이익을 붙인값:%.2f", c * d);

}



#include <stdio.h>

int main() {
	float discounted_price;
	float original_price;
	float cost;

	// 판매된 가격 입력 받기
	printf("할인된 가격을 입력하세요: ");
	scanf("%f", &discounted_price);

	// 정가 계산
	original_price = discounted_price / 0.8;

	// 원가 계산
	cost = original_price / 1.3;

	// 결과 출력
	printf("전자제품의 원가는 %.2f원 입니다.\n", cost);

	return 0;
}


#include <stdio.h>

int main()
{
	double 원가 = 0;//?
	double 정가 = 0.;//?
	double 판매가 = 0.;//?
	const double 이익률 = 0.3;
	const double 할인율 = 0.2;
	double 판매이익 = 5000.;

	정가 = 원가 + 원가 * 이익률; // 원가*(1+0.3)=원가*1.3
	판매가 = 정가 - 정가 * 할인율; // 정가*(1-0.2)=정가*0.8
	// 판매이익 = 판매가 - 원가; // 원가=판매가-판매이익
	//원가 = 판매가 - 판매이익;
	//원가 = 정가 - 정가 * 할인율 - 판매이익;
	//원가 = 정가*(1-할인율) - 판매이익
	//원가 = (원가 + 원가 * 이익률)*(1-할인율)-판매이익
	//원가 = 원가(1 + 이익률) * (1 - 할인율) - 판매이익
	//판매이익=원가*((1 + 이익률) * (1 - 할인율)-1)
	//원가=판매이익/((1 + 이익률) * (1 - 할인율)-1)
	원가 = 판매이익 / ((1 + 이익률) * (1 - 할인율) - 1);
	판매가 = 원가 + 판매이익;
	정가 = 판매가 / (1 - 할인율);
	
	printf("원가: %lf\n", 원가);
	printf("판매가: %lf\n", 판매가);
	printf("정가: %lf\n", 정가);



	return 0;
}



#include<stdio.h>
int main()
{
	double a; // 입장권 가격
	double b; //할인율 20% (0.8)

	a = 2000;
	b = 0.8;
	// 최대 구매 일떄 할인 받는 금액 (30*2000)*0.8

	printf("30명 최대로 할인 받을때: %lf\n", (a * 30) * 0.8);
}



#include<stdio.h>
int main()
{
	char grade;
	char name[20];

	printf("학점 입력: ");
		scanf("%c",&grade);
	printf("이름 입력: ");
		scanf("%s",name);
		printf("%s의 학점은 %c 입니다\n",name,grade);
}



#include<stdio.h>
int main(void)
{
	char fruit[20];
	int cnt;

	printf("내가 좋아하는 과일: ");
	scanf("%s", fruit);
	printf("몇 개: ");
	scanf("%d", &cnt);
	printf("%s를 %d개 드립니다", fruit,cnt);

	return 0;

}

#include<stdio.h>
int main()
{
	char ch;
	printf("문자입력: ");
	scanf("%c", &ch);
	printf("입력한 문자의 아스키 코드값은 %d입니다",ch);
}

//사칙연산자
// +,-,*,/,=,=/=
//>,>=,<,<=,==,!=
*/

/*
#include<stdio.h>
int main()
{
	int a;
	int b;
	int c;
	a = 7; //유정이의 나이
	b = 5; //유정이의 아빠의 나이 배수차이
	c = 4; //유정이와 아빠의 나이 합차이

	//a*b+c

	printf("유정이의 아빠의 나이:%d\n", a * b + c);

}
*/
/*
#include<stdio.h>
int main()
{
	// 1000이 한번 갈때 6씩
	// 100이 한번 갈때 3씩
	// 10이 한번갈때 5씩
	// 1이 한번갈떄 8씩
	// 이때 5번뛰어 갈때 숫자는

	int a;
	int b;
	int c;
	a = 4180;	//현재 남아있는 금액
	b = 1000;	//매달 입금한 금액
	c = 3;		//적금한 달 수
	// 10월,11월,12월 3달 3천원
	printf("혜미가 통장에 저금한 돈:%d\n", b * c + a);
}
*/

//-------------------------------------------------------------------------------------------------------------------------------4/26

/*
연산자: + -
사칙연산: + - * / %					정수 실수
비교연산 > >= < <= == !=			정수 실수
논린연산자&& || ! (and or not)		맞다 틀리다,trua false
비트연산& | ~ ^						정수-16진수용
배열 연산 []
함수연산 ()
구조 연산 . ->

#include<stdio.h>
int main()
{
	int a, b;
	int sum, sub, mul, inv;

	a = 10;
	b = 20;
	sum = a + b;
	sub = a - b;
	mul = a * b;
	inv = -a;

	FILE* fp = fopen("test.txt", "w");

	fprintf(fp,"a의 값 : % d, b의 값 % d\n",a, b);
	fprintf(fp, "덧셈:%d\n", sum);
	fprintf(fp, "뺄셈:%d\n", sub);
	fprintf(fp, "곱셈:%d\n", mul);
	fprintf(fp, "a의 음수 연산:%d\n", inv);

	fclose(fp);
}

#include<stdio.h>
int main()
{
	FILE* fe = fopen("test2.txt", "w");

	double apple;
	int banana;
	int orange;


	apple = 5.0 / 2.0;
	banana = 5 / 2;
	orange = 5 % 2;
	fprintf(fe,"apple:%.1lf\n", apple);
	fprintf(fe,"banana: %d\n", banana);
	fprintf(fe,"orange: %d\n", orange);

	fclose(fe);

}



a=a+1; //a에 1을 더해서 a에 넣어
a+=1; //a에 1을 더해
++a; //a를 증가시켜
a++; //


#include<stdio.h>
int main()
{
	int a = 10, b = 10;
	++a;
	--b;
	printf("a:%d\n", a);
	printf("b:%d\n", b);
}



#include<stdio.h>
int main()
{
	int a = 5, b = 5;
	int pre, post,npre,npost;
	pre = (++a) * 3;
	post = (b++) * 3;
	npre = ++a * 3;
	npost = b++ * 3;

	printf("증감 연산후 초깃값 a=%d,b=%d\n", a, b);
	printf("전위형: (++a)*3=%d, 후위형:(b++)*3 =%d\n", pre, post);
	printf("전위형: ++a *3 =%d, 후위형:b++ *3 =%d\n", npre, npost);

}




#include<stdio.h>
int main()
{
	int a=10, b = 20, c = 10;
	int res;

	res = (a > b);
	printf("a>b:%d\n", res);

	res(a >= b);
	printf("a<b:%d\n", res);

	res(a < b);
	printf("a<=b:%d\n", res);

	res(a <= b);
	printf("a>b:%d\n", res);

	res(a >= b);
	printf("a>=b:%d\n", res);

	res(a <= c);
	printf("a<=c:%d\n", res);

	res(a==b);
	printf("a==b:%d\n", res);

	res(a!=c);
	printf("a!=c:%d\n", res);

}



#include<stdio.h>
int main()
{
	int a = 30;
	int res;

	res = (a > 10) && (a < 20);
	printf("(a>10)&&(a<20):%d\n", res);
	res = (a < 10) || (a > 20);
	printf("(a<10)&&(a>20):%d\n", res);
	res = (a >= 30);
	printf("!(a>30):%d\n", res);
}



#include<stdio.h>

int main()
{
	double a=4.0, b = 1.2;
	printf("a = 4.0, b = 1.2\n");
	printf("%.1lf + %.1lf = %.1lf\n", a, b, a + b);
	printf("%.1lf - %.1lf = %.1lf\n", a, b, a - b);
	printf("%.1lf * %.1lf = %.1lf\n", a, b, a * b);
	printf("%.1lf / %.1lf = %.1lf\n", a, b, a / b);
}



#include<stdio.h>
int main()
{
	int a, b, tot;
	double avg;
	
	printf("두 과목의 점수: ");
	scanf("%d %d",&a,&b);
	tot = a + b;
	avg = tot / 2.0;
	printf("평균: %.1lf\n", avg);
}


#include<stdio.h>

int main()
{
	// 국어 점수3.8 학점3
	// 수학 점수3.9 학점4
	// 영어 점수4.4 학점5

	int income=0;

	int res;

	int kor;	//국어 학점 3 
	int eng;	//영어 학점 5
	int mat;	//수학 학점 4
	int a;		//학점합계
	double ksc; //국어 평점 3.8
	double esc; //영어 평점 4.4
	double msc; //수학 평점 3.9
	double b;	//평점 합계

	kor = 3, eng = 5, mat = 4, ksc = 3.8, esc = 4.4, msc = 3.9;
	a = kor + eng + mat;
	b = ksc + esc + msc;
	printf("\n");
	printf("\t전체 학점은:%d 입니다\n", a);
	printf("\t평점의 평균은:%1.lf 입니다\n", b/ 3);

	printf("\ta는 학점이며 b는 평균 평점입니다\n");
	printf("\t학점은 10을 넘고,평균 평점이 4를 넘어야합니다\n");
	res = (a >= 10) && (b >=4);
	printf("\t따라서 (a>=10)&&(b>=4)이며 값은 :%d\n",res);

	printf("\t1이 뜨면 합격 0이뜨면 불합격입니다\n");
}


#include<stdio.h>
#include<stdlib.h>

int main()
{
	char msg[10];
	int idata[100];
	double ddata[1000];

	printf("%d\n", sizeof(msg));
	printf("%d\n", sizeof(char[10]));
	printf("%d\n", sizeof(idata));
	printf("%d\n", sizeof(int[100]));
	printf("%d\n", sizeof(ddata));
	printf("%d\n", sizeof(double[1000]));

	//scanf_s(msg, _contof(msg), "hello hello");
	//ㄴ 함수에 배열을 넘길때 배열의 크기정보를 넘겨줘야한다
	//왜냐하면 함수 안쪽에서는 배열의 크기를 c 에서는 알수없게만들었기떄문이다

}

#include<stdio.h>

int main()
{
	int a = 10 , b = 20;
	int res = 2;
	a += 20;
	res *= b + 10;
	printf("a=%d,b=%d\n", a, b);
	printf("res=%d\n", res);
}

#include<stdio.h>

int main()
{
	int a = 10, b = 20, res;
	res = (a < b) ? a : b;
	printf("큰값:%d\n", res);
}

#include<stdio.h>
int main()
{
	int a = 10;
	int b = 12;
	printf("a & b: % d\n", a & b);
	printf("a ^ b: % d\n", a ^ b);
	printf("a | b: % d\n", a | b);
	printf("~ a: % d\n", ~a);
	printf("a << 1: % d\n", a << 1);
	printf("a >> 2: % d\n", a >> 2);
}


#include<stdio.h>

int main()
{
	int a;
	int b;
	//int c;
	
	//c = a / b;
	
	printf("\t\t\t\t\t전체 좌석수/입장인 수\n");
printf("전체 좌석 수와 입장인 수를 입력하요: ");
scanf("%d", &a,&b);
//printf("인원당 입장률은: %lf %%입니다", c);

}


#include<stdio.h>
int main()
{
	int hour, min, sec;
		double time = 3.76;

		hour = (int)time;
		time -= hour;
		time *= 60;
		
		min = (int)time;
		time -= min;

		time *= 60;
		sec = (int)time;
		
		printf("3.76시간은 %d시간 %d분 %d초 입니다.\n");
}




#include<stdio.h>
int main()
{
	int weight;
	double height;
	printf("몸무게와(kg)와 키(cm) 입력하세요 :");
	scanf("%d%lf", &weight, &height);

	double bmi = weight / (height / 100 * height / 100);
	printf("bim 지수는:%lf 입니다\n", bmi);
	printf("%s\n",((bmi > 20.) && (bmi < 25.)) ? "표준입니다" : "체중관리가필요합니다");
}
----------------------------------------------------------------------
#include <stdio.h>
#include <string.h>

int main()
{
	int res;

	res = (sizeof(short) > sizeof(long)) ? 1 : 0;
	printf("%s\n", (res == 1) ? "short" : "long");

	char ans[10];
	(res == 1) ? strcpy(ans, "short") : strcpy(ans, "long");
	printf("%s\n", ans);

	char ans[10] = (res == 1) ? "short" : "long";

	return 0;

	int seats = 70;
	int audience = 65;
	double rate;

	rate = (double)audience / seats;

	printf("입장률 : %.1lf", rate);
}

*/

//--------------------------------------------------------------------------- 4/29

/*
#include<stdio.h>
int main()
{
	int a = 20;
	int b = 10;

	if (a > 10)
	{
		b = a;
	}

	printf("a:%d,b:%d\n", a, b);

	
}



#include<stdio.h>
int main()
{
	int a = 10;
	if (a >= 10)
	{
		a = 1;
	}
	else
	{
		a = -1;
	}
	printf("a:%d\n", a);
}


#include<stdio.h>
int main()
{
	int a = 0, b = 0;

	if (a > 0)
	{
		b - 1;

	}
	else if (a == 0)
	{
		b = 2;
	}
	else {
		b = 3;
	}
	printf("b:%d\n", b);
}



#include<stdio.h>
int main()
{
	int chest = 95;

	char size;
	size = 95;

	if (size<90)
	{
		size = 'S';

	}
	else if (90 < size < 100) // <- 이 표현법은 파이썬 표현법 이니 해당 표현법을 사용할것-> 90<size && size<100
	{
		size = 'M';
	}
	else
	{
		size = 'L';qq`
	}
	printf("size:%d\n", size);

}



#include<stdio.h>
int main()
{
	int rank = 2, m = 0;
	switch (rank)

	{
	case 1:
		m = 300;
		break;
	case 2:
		m = 200;
		break;
	case 3:
		m = 100;
		break;
	default:
		m = 10;
		break;
	}
	printf("m:%d\n", m);
}



//브레이크(break)가없을경우 switch 값에 해당되는 아렛값 전부를불러옴 또한 정수값만 가능하다

#include<stdio.h>
int main()
{
	int a;
	printf("정수입력:");
	scanf("%d", &a);
	switch (a % 3)

	{
	case 0:
		printf("거짓");
		break;
	case 1:
		printf("참");
		break;
	case 2:
		printf("참");
		break;
	default:
		printf("거짓");
		break;
	}
}




#include<stdio.h>
int main()
{
	int age=25, chest = 95;
	int size;
	if(age<25)

}




#include<stdio.h>
int main()
{
	int a = 1;
	while (a < 10)
	{
		a = a * 2;
	}

		printf("a:%d\n", a);

}



#include<stdio.h>
int main()
{
	int a = 1;
	int i;

	for (i = 0; i < 3; i++)
	{
		a = a * 2;
	}
	printf("a: %d\n", a);
}


#include<stdio.h>
int main()
{
	int a = 1;
	do
	{
		a = a * 2;
	} while (a < 10);
	printf("a;%d\n", a);
}


#include<stdio.h>
#define n 1000000000
int num[n];
int num2[n];
int main()
{
	FILE* fp=fopen("data.txt", "w");
	for (int i = 0; i < sizeof(num) / sizeof(num[0]); i++){
		num[i] = i;
	printf("num[%d]=%d\n",i, num[i]);
	fprintf(fp,"%d\n",num[i]);
}
	fclose(fp);
	FILE* fp2 = fopen("data.txt", "r"); 
		for (int i = 0; i < sizeof(num2) / sizeof(num2[0]); i++){
			fscanf(fp2, "%d", &num2[i]);
		printf("num2[%d]=%d\n", i, num2[i]);
	}
	fclose(fp2);
}




#include <stdio.h>
// 프로그램의 일반적인 구조
void show_menu()
{
	printf("1. 파일\n");
	printf("2. 편집\n");
	printf("3. 보기\n");
}
int get_order()
{
	int order;
	printf("무엇을 할까요?(종료:-1) ");
	scanf("%d", &order);
	return order;
}
int main() // 1
{
	while (1) { // 2
		show_menu(); // 3
		int order = get_order();
		switch (order) {
		case 1:
			printf("파일 처리를 합니다~\n");
			break;
		case 2:
			printf("편집을 합니다~\n");
			break;
		case 3:
			printf("보기를 수행합니다~\n");
			break;
		case -1:
			printf("프로그램을 종료합니다.\n");
			return 0;
		default:
			printf("명령을 다시 입력해주세요~\n");
			break;
		}
	}
}

#include<stdio.h>
#include<Windows.h>
int main(vodi)
{
	int i, j;
	for (i = 0; i < 30; i++)
	{
		for (j = 0; j < 50; j++)
		{
			printf("*");
			Sleep(1000);
		}
		printf("\n");
	}
	return 0;
}


//193p 연습문제
#include<stdio.h>
int main()
{
	int i;
	for (i = 0; i < 9; i++)
	{
		printf("&", i);
	}
		
}

#include <stdio.h>
#include <Windows.h>
int main()
{
	printf("\033[0;33m");
	while (1) {
		printf("\b*");//printf("\b\b\b\b\b* * *");
		Sleep(500);
		printf("\b ");//printf("\b\b\b\b\b * * ");
		Sleep(500);
	}
}


#include<stdio.h>
int main()
{
	for(int i=1;i<+9;i++)
	{
		printf("2*%d=%2d\n", i, 2 * i);
	}

	for (int j = 2; j <= 9; j++)
	{
		for (int i = 1; i <= 9; i++)
		{
			printf("%d*%d=%2d\n", j, i, j * i);
		}
	}
	
}


#include<stdio.h>
int main(void)
{
	int i;
	int sum = 0;
	for (i = 1; i < 10; i++)
	{
		sum += i;
		if (sum > 30)break;
	}
	printf("누적한값: %d\n", sum);
	printf("마지막으로 더한 값: %d\n", i);
}



#include<stdio.h>
int main()
{
	for (int i = 0; i < 10; i++){
		printf("%d\n", i);
	if (i > 4) break;
}

for (int j = 0; j < 10; j++) {
	if (j % 3 == 0) continue;
	printf(" % d\n", j);
}


}



#include<stdio.h>
int main()
{
	int ax[5];
	int ay[8];
	int az[11];
	
	double axx[2][5];
	double aay[5][5];
	double az[9][7];
	double axx[2][5];

	student as[5];
	monitr am[5];
	back aax[2][5];

}



#include<stdio.h>
int main()
{
	char stat[5][5] = {
		{'*',' ',' ',' ','*'},
		{' ','*',' ','*',' '},
		{' ',' ','*',' ',' '},
		{' ','*',' ','*',' '},
		{'*',' ',' ',' ','*'},
	};
	int i, j;
	for (i = 0; i < 5; i++) {
		for (j = 0; j < 5; j++) {
			printf("% c", stat[i][j]);
		}
		printf("\n");
	}
}


#include <stdio.h>

int main()
{
	int num = 100;
	int prime_number;
	while (1) {
		printf("2 이상의 정수를 입력하세요 : ");//menu
		scanf("%d", &num);//get order
		if (!(num >= 2)) continue;
		int cnt = 0;
		for (int i = 2; i <= num; i++) {
			prime_number = 1;
			for (int j = 2; j < i; j++) {
				if (i % j == 0) {
					prime_number = 0;
					break;
				}
			}
			if (prime_number == 1) {
				printf("%5d", i);
				cnt++;
				if (cnt % 5 == 0) {
					printf("\n");
				}
			}
		}
		printf("cnt %d\n", cnt);
	}

}




#include<stdio.h>

int sum(int x, int y);

int main()
{
	int a = 10, b = 20;
	int result;

	result = sum(a, b);
	printf("resulf: %d\n", result);
	return 0;
}
int sum(int x, int y)

{

	int temp;
	temp = x + y;
	return 0;
}




다음 일차 함수를 정의 하고 호출한 결과를 구하시오
y=f(x)3*x+1/
y=f(7)

다음 이차 함수를 정의하고 호출한 결과를 출력하싱ㅎ
y=gx=3*6*33*x+21

다음 사맟 함수를 정의하고



#include<stdio.h>

void print_char(char ch, int count);
int main()
{
	print_char('@', 5);

	return 0;
}
void print_char(char ch, int conut)
{
	int i;

	for (i = 0; i < conut; i++)
	{
		printf("%c", ch);
	}
}
*/

/*
다음과 같이 함수를 호출할때 함수의 모양을 완성하시오
int r=FA(3,4) 답:int FA(int,int);
int r=FB(3,14);
double r = FC(3,4,5.4);
int r=FD(3.143.14,2.72,4);
double r=FE(1,2,3,3.14);



#include<stdio.h>
*/
/*
#include<stdio.h>

void abc(char ch, int count);
int main()
{
	abc('@', 5);

	return 0;
}
void abc(char ch, int conut)
{
	int i;

	for (i = 0; i < conut; i++)
	{
		printf("%c", ch);
	}
}

void a(char ch, int count,int c);
int main()
{
	a('@', 5,8);

	return 0;
}
void a(char ch, int conut,int c)
{
	int i;
	int j;


	for (i = 0; i < conut; i++)
	{
		for (j = 0; j < c; j++) {
			printf("%c", ch);
		}
		printf("\n");
	}
}



#include <stdio.h>
int 자판기(int, int); // 2. 함수 원형 선언

int main()
{
	// 커피 = 자판기(동전, 커피선택);
	// 500원을 넣고 커피를 선택하면 커피가 나온다.
	// 커피는 1. 아메리카노, 2. 카페라떼, 3. 망고주스
	int 음료 = 자판기(500, 1); // 1. 함수 호출

	return 0;
}

int 자판기(int 동전, int 음료선택)
{
	int 음료;
	if (동전 == 500) {
		if (음료선택 == 1) {
			printf("아메리카노를 준비하겠습니다.");
		}
		else if (음료선택 == 2) {
			printf("카페라떼를 준비하겠습니다.");
		}
		else if (음료선택 == 3) {
			printf("망고주스를 준비하겠습니다.");
		}
		음료 = 음료선택;
	}
	return 음료;
}


void print_line(void);
int main(void)
{
	print_line();
	printf("학번 이름 전공 학점\n");
	print_line();
	void print_line(void);
}
int i;
for (i = 0; i < 50; i++)
{
	printf("_");
}
printf("\n");
}

void fruit(void);
int main(void)
{
	fruit();
	return 0;
}
void fruit(void)
{
	printf("apple\n");
	fruit();
}


int func(int n);
int poly(int n);
int main(void)
{
	p("%d\n", func(-3));
	return 0;
}

int func(int n)
{
int res;
res = poly(n);
if (res >= 0)return res;
}
int poly(int n)
{
	return((2 * n * n) + (3 * n));
}


void auto_func(void);
void static_func(void);

int main(void)
{
	int i;

	p("일반 지역 변수 (auto)를 사용한 함수........\n");
	for (i = 0; i < 3; i++)
	{
		auto_func();
	}

	p("정적 지역 변수 (static)를 사용한경우........\n");
	for (i = 0; i < 3; i++)
	{
		static_func();
	}
	return 0;
}

void auto_func(void)
{
	auto int a = 0;

	a++;
	p("%d\n", a);
}
void static_func(void)
{
	static int a;
	a++;
	p("%d\n", a);
}



void add_ten(int a);
int main(void)
{
	int a = 10;

	add_ten(&a);
	p("a:%d\n", a);

	return 0;
}
void add_ten(int* a)
{
	a = a + 10;
	//*a = *a + 10;
	//a[0] = a[0] + 10;
}


void func(void);

int a = 10;
int main(void)
{
	a = 20;
	func();
	p("%d", a);
	return 0;
}

void func(void)
{
	a = 30;
}


int func(void);
int main(void)
{
	int i, sum = 0;
	for (i = 0; i < 10; i++)
	{
		sum += func();
	}
	p("%d", sum);
	return 0;
}

int func(void)
{
	static int a = 0;
	a++;
		return a;
}


#include <windows.h>
void main()
{
	MessageBox(0,L"Hello Windows!",L"",0);
	return 0;
}

#include <windows.h>
void main()
{
	MessageBox(
		0,
		L"Hello Windows!",
		L"win",
		MB_YESNOCANCEL);

	return 0;
}

#include <windows.h>
void main()
{
	MessageBox(
		0,
		L"동의하십니까?",
		L"투표",
		MB_OKCANCEL);

	return 0;
}


#include <windows.h>
void main()
{
	printf(L"Before MessageBox()\n");
	CreateWindow(
		L"button",
		L"PUSH ME!",
		WS_OVERLAPPEDWINDOW | WS_VISIBLE,
		100,
		100,
		100,
		100,
		0,
		0,
		0,
		0);
	MessageBox(
		0,
		L"Hello Windows!",
		"",
		0);
	printf(L"After MessageBox()\n");
}



int main()

{
	int a;
	int* pa;

	pa = &a;
	*pa = 10;
	p("")

}


int main()
{
	int a = 10, b = 15, total;
	double avg;
	int* pa, * pb;
	int* pt = &total;
	double* pg = &avg;

	pa = &a;
	pb = &b;
	*pt = *pa + *pb;
	*pg = *pt / 2.0;
	printf("두 정수의 값: %d,%d\n", *pa, *pb);
	printf("두 정수의 합: %d\n", *pt);
	printf("두 정수의 평균: %.1lf\n", *pg);

	return 0;
}


int my_average(int* pt, double* pg, int* pa, int* pb)
{
	*pt = *pa + *pb;
	*pg = *pt / 2.0;

	printf("두 정수의 값: %d,%d\n", *pa, *pb);
	printf("두 정수의 합: %d\n", *pt);
	printf("두 정수의 평균: %.1lf\n", *pg);

}
int main()
{
	int a = 10, b = 15, total;
	double avg;

	my_average(&total, &avg, &a, &b);

	return 0;
}


int main()
{
	int a = 10, b = 20;
	const int* pa = &a;

	p("변수 a의 값:%d\n", *pa);
	pa = &b;
	p("변수 b의 값:%d\n", *pa);
	pa = &a;
	a = 20;
	p("변수 a의 값:%d\n", *pa);

	return 0;
}




int main()
{

	char ch = *pa;
	int in = *pb;
	double db = *pc;
}

int main()
{
	int a = 10;
	int* p = &a;
	double *pd;
	
	pd = double;

	printf("%lf\n", *1000);
	return 0;
}

void swap(int* pa, int* pb);
int main()
{
	int a = 10, b = 20;
	swap(&a, &b);
	printf("a:%d, b:%d\n", a, b);
	return 0;
}
void swap(int* pa, int* pb)
{
	int temp;

	temp = *pa;
	* pa = pb;
	*pb = temp;
}


void swap(double* pa, double* pb);
void line_up(double* maxp, double* midp, double* miup);
int main()
{
	double max, mid, min;
	printf("실수값 3개 입력: ");
	scanf(" %lf %lf %lf", &max, &mid, &min);
	line_up(&max, &mid, &min);
	printf("정렬된값 출력: %.1lf,%.1lf,%.1lf", max, mid,min);
	return 0;

}
void swap(double* pa, double* pb)
{
	double temp;
	temp = *pa;
	*pa = *pb;
	*pb = temp;
}

void line_up(double* maxp, double* midp,double* minp)
{
	if (*maxp < *midp)swap(maxp, midp);
	if (*maxp < *minp)swap(maxp, minp);
	if (*midp < *minp)swap(midp, minp);
}


int main()
{
	int ary[3];
	int i;
	*(ary + 0) = 10;
	*(ary + 1) = *(ary + 0) + 10;

	printf("세번쨰 배열 요소에 키보드 입력: ");
	scanf("%d", ary + 2);


	for (i = 0; i < 3; i++)
	{
		printf("%d5", *(ary + i));
	}
	return 0;
}


void input_ary(double* pa, int size);
double find_max(double* pa, int size);

int main()
{
	double ary[5];
	double max;
	int size = sizeof(ary) / sizeof(ary[0]);
	input_ary(ary, size);
	max = find_max(ary, size);
	printf("배열의 최댓값: %.lf\n", max);
	return 0;
}
void input_ary(double* pa, int size)
{
	int i;
	printf("%d개의 실수값 입력: ", size);
	for (i = 0; i < size; i++) 
	{
		scanf("%lf", pa + i);
	}
}
double find_max(double* pa, int size)
{
	double max;
	int i;
	
	max = pa[0];
	for (i = i; i < size; i++)
	{
		if (pa[i] > max)max = pa[i];
	}
	return max;
}
*/

/*
void f(int* ip) {
	printf("%d\n", *ip);// <=> *(ip+0)
	printf("%d\n", ip[0]); // *(ip+0) <=> ip[0]
	printf("%d\n", *(ip + 1));
	printf("%d\n", ip[1]); // *(ip+N) == ip[N]
}
int main()
{
	int a[2] = { 20, 30 };
	//a[0] <=> *(a+0)

	f(a);// int *ip = &a[0]
	printf("%d %d %d\n", a[0], *a, *(a + 0));
}
*/
/*
void input_nums(int* lotto_nums);
void print_nums(int* lotto_nums);

int main(void)
{
   int lotto_nums[6];

   input_nums(lotto_nums);
   print_nums(lotto_nums);

   return 0;
}
void input_nums(int* lotto_nums)
{
   int lotto_num;
   for (int i = 0; i < 6; i++) {
	  while (1) {
		 printf("번호 입력: ");
		 scanf("%d", &lotto_num);
		 if (i == 0) {
			if (lotto_num>=1 && lotto_num <= 45) {
			   lotto_nums[0] = lotto_num;
			   break;
			}
		 }
		 else {
			int j;
			for (j = 0; j < i; j++) {
			   if (lotto_nums[j] == lotto_num) {
				  printf("같은 번호가 있습니다!\n");
				  break;
			   }
			}
			if (j < i);
			else {
			   if (lotto_num >= 1 && lotto_num <= 45) {
				  lotto_nums[i] = lotto_num;
				  break;
			   }
			}
		 }
	  }
   }
}

void print_nums(int* lotto_nums)
{
   printf("로또 번호 : ");
   for (int i = 0; i < 6; i++) {
	  printf("%5d", lotto_nums[i]);
   }
}
*/

/*
int main()
{
	int rnum;
	srand(33);
	for (int i = 0; i < 10; i++)
	{
		rnum = rand();
		printf("%6d",rnum%45+1);
	}
	printf("\n");
}*/

/*
int main()
{
	char small, cap = 'G';
		if ((cap >= 'A') && (cap <= 'Z'))
		{
			small = cap + ('a' - 'A');
		}
		printf("대문자: %c%c", cap, '\n');
		printf("소문자: %c", small);

		return 0;
}
*/

/*
int main()
{
	while(1)
	{
		char ch1, ch2;
		scanf("%c%c", &ch1, &ch2);
		printf("[%c%c]", ch1, ch2);
	}
	return 0;
}

*/

/*
int main()
{
	int ch;
	ch = getchar();
	printf("입력한 문자: ");
	putchar(ch);
	putchar('\n');

	return 0;
}
*/
/*
int main()
{
	int ch;
	ch = getchar();
	printf("입력한 문자: ");
	printf("문자의 아스키 코드 값: %d\n", ch);
	putchar(ch);
	putchar('\n');

	return 0;
}
*/
/*
int main()
{
	int ch;
	ch = getchar();
	printf("입력한 문자: ");
	printf("문자의 아스키 코드 값: %d\n", ch);
	putchar('\n');

	return 0;
}
*/
/*
int main()
{
	char ch;
	int i;
	for (i = 0; i < 3; i++)
	{
		scanf("%c", &ch);
		printf("%c", ch);

	}
	return 0;
}
*/
/*
int main()
{
	int res;
	char ch;
	while (1) 
	{
		res = scanf("%c", &ch);
		if (res == -1) break;
		printf("%d\n", ch);

	}
	return 0;
}
*/
/*
int main()
{
	int ch;
	int cnt = 0;
	int max = 0;
	ch = getchar();
	//printf("EOF: %d\n", EOF);
	while (1)
	{
		ch = getchar();
		if (ch == EOF) break;
		cnt = 0;
		while (ch != '\n')
		{
			cnt++;
			ch = getchar();
		}
		printf("현재 단어의 길이: %d\n", cnt);
		if (cnt > max) max = cnt;
	}
	printf("가장 긴 단어의 길이: %d\n", max);
}
*/
/*
int main()
{
	printf("aplle이 저장된 시작 주소값: %p\n", "apple");
	printf("두 번째 문자의 주소값: %p\n", "apple" + 1);
	printf("첫 번째 분자 : %c\n",*"apple");
	printf("첫 번째 분자 : %c\n", *("apple" + 1));
	printf("배열로 표현한 세 번째 문자: %c\n", "apple"[2]);

	return 0;
}
*/
/*
int main()
{
	char str[80];
	printf("문자열 입력: ");
	scanf("%s", str);
	printf("첫 번째 단어:%s\n", str);
	scanf("%s", str);
	printf("버퍼에 남아있는 두 번째 단어: %s\n", str);

	return 0;
}
*/

/*
int main()
{
	int age;
	char name[20];
	printf("나이 입력: ");
	scanf("%d", &age);
	printf("이름 입력: ");
	gets(name);
	printf("나이: %d,이름: %s\n", age, name);

	return 0;
}
*/
/*
int main()
{
	char str1[80] = "strawberry";
	char str2[80] = "apple";
	char* ps1 = "banana";
	char* ps2 = str2;
	printf("최초 문자열: %s\n", str1);
	strcpy(str1, str2);
	printf("바뀐 문자열 %s\n", str1);

	strcpy(str1, ps1);
	printf("바뀐 문자열 %s\n", str1);

	strcpy(str1, ps2);
	printf("바뀐 문자열 %s\n", str1);

	strcpy(str1, "banana");
	printf("바뀐 문자열 %s\n", str1);

	return 0;
}
*/
/*
int main()
{
	char str[20] = "mango tree";
	strncpy(str, "apple-pin", 5);
	printf("%s\n", str);
	return 0;
}
*/

/*
int main()
{
	char str[80] = "straw";
	strcat(str, "berry");
	printf("%s\n", str);
	strncat(str, "piece", 3);
	printf("%s\n", str);
	return 0;
}
*/
/*
int main()
{
	char str1[80], str2[80];
	char* resp;
	printf("과일 2개 입력: ");
	scanf("%s%s", str1, str2);
	if (strlen(str1) > strlen(str2))

		resp = str2;

	else 
		resp = str2;
		printf("이름이 가장긴 과일은: %s\n", resp);
		return 0;
}
*/

/*
int main()
{
	char str1[80] = "pear";
	char str2[80] = "pear";

	printf("사전에 나중에 나오는 과일이름: ");

	if (strcmp(str1, str2) > 0)
	printf("%s\n", str1);
	else
		printf("%s\n", str2);
	return 0;
}
*/

/*
char* my_strcpy(char* dest, const char* src);
int my_strlen(const char* str);
int my_strcmp(const char* str1, const char* str2);
char* my_strcat(char* str1, const char* str2);

int main(void)
{
	char str[80] = "strawberry";// &"strawberry"[0]

	printf(&"바꾸기 전 문자열 : %s\n"[0], &str[0]); // &str[0]
	my_strcpy(&str[0], &"apple"[0]); // char *, const char *
	printf("바꾼 후 문자열 : %s\n", str);
	printf("다른 문자열 대입 : %s\n", my_strcpy(str, "kiwi"));
	printf("my_strlen(str)=%d\n", my_strlen(str));
	printf("my_strlen(\"hello\")=%d\n", my_strlen("hello"));
	my_strcmp(&"abC"[0], &"abc"[0]); //const char *, const char *
	my_strcat(&str[0], &"hello"[0]); // char *, const char *
}

char* my_strcpy(char* dest, const char* src)
{
	char* dest_0 = dest;
	/*while (*src != '\0')
	{
	   *dest = *src;
	   dest++;
	   src++;
	}
	*dest = *src;
	return dest_0; //&dest_0[0]
	int i;
	for (i = 0; src[i] != '\0'; i++)
	{
		dest[i] = src[i];
	}
	dest[i] = src[i];
	return dest_0;
}

int my_strlen(const char* str)
{
	/*int cnt = 0;
	while(*str!='\0')
	{
	   str++;
	   cnt++;
	}
	return cnt;

	int i;
	for (i = 0; str[i] != '\0'; i++);
	return i;
}

int my_strcmp(const char* str1, const char* str2)
{
	while (*str1 != '\0' && *str2 != '\0') {
		if (*str1 == *str2)
		{
			str1++;
			str2++;
		}
		else {
			if (*str1 < *str2) return -1;
			else return 1;
		}
	}
	if (*str1 == '\0' && *str2 == '\0') return 0;
	else if (*str1 == '\0') return -1;
	else return 1;
}

char* my_strcat(char* str1, const char* str2)
{
	char* str1_0 = str1;
	while (*str1 != '\0') str1++;
	while (*str2 != '\0')
	{
		*str1++ = *str2++;
		//str1++;
		//str2++;
	}
	*str1 = *str2;
	return str1_0;
}

*/
/*
int main()
{
	char str[16];
	char str_star[16];
	printf("단어 입력 : ");
	scanf("%s", str);

	if (strlen(str) <= 5)
		strcpy(str_star, str);
	else
	{
		strncpy(str_star, str, 5);
		int i;
		for (i = 5; str[i] != '\0'; i++)
		{
			str_star[i] = '*';
		}
		str_star[i] = '\0';
	}
	printf("입력한 단어 : %s, 생략한 단어 : %s", str, str_star);
}
*/
/*
#include <stdio.h>
#include <string.h>

void strswap(char* str1, char* str2) {
	char temp[80];
	strcpy(temp, str1);
	strcpy(str1, str2);
	strcpy(str2, temp);
}
int main() {
	char word1[80];
	char word2[80];
	char word3[80];

	printf("세 단어 입력 : ");
	scanf("%s%s%s", word1, word2, word3);

	if (strcmp(word1, word2) > 0) strswap(word1, word2);
	if (strcmp(word1, word3) > 0) strswap(word1, word3);
	if (strcmp(word2, word3) > 0) strswap(word2, word3);
	printf("%s %s %s\n", word1, word2, word3);
}

*/
/*
void add_ten(int a);
int main()
{
	int a = 10;
	add_ten(a);
	printf("a:%d\n", a);
	return 0;
}

void add_ten(int a)
{
	a = a + 10;
}

*/

/*
void add_ten(int* pa);

int main(void)
{
	int a = 10;
	add_ten(&a);
	printf("a:%d\n", a);
	return 0;
}

void add_ten(int* pa)
{
	*pa = *pa + 10;
}

*/
/*
int* sum(int a, int b);

void main()
{
	int *resp;

	resp = sum(10, 20);
	printf("두정수의 합: %d\n", *resp);

	return 0;
}

int* sum(int a, int b)
{
	static int res;
	res = a + b;
	return &res;

}

*/
/*
int main(void)
{
	int score[3][4];
	int total;
	double avg;
	int i, j;

	for (i = 0; i < 3; i++)
	{
		printf("4과목 점수 입력: ");
		for (j = 0; j < 4; j++)
		{
		scanf("%d", score[i][j]);
		}
	}

	for (i = 0; i < 3; i++)
	{
	total = 0;
	for (j = 0; j < 4; j++)
		{
		total += score[i][j];
		}
	avg = total / 4.0;
	printf("총점:%d, 평균:%.2lf\n", total, avg);
	}
	return 0;
}

*/

/*
void get_scores(int(*score)[4]);
void prt_scores(int score[3][4]);
int main(void)
{
	//int iar[3]; // iar[0] <=> int, &iar[0] <=> int *ip
	int score[3][4]; // score[0] <=> int[4], &score[0] <=> int(*sp)[4]  
	int total;
	double avg;

	get_scores(score); // &score[0] => int[4] * => int(*)[4]
	prt_scores(score);
}

//void get_scores(int score[3][4]);
//void get_scores(int score[][4]);
void get_scores(int(*score)[4])
{
	for (int i = 0; i < 3; i++)
	{
		printf("4과목의 점수 입력: ");
		for (int j = 0; j < 4; j++)
		{
			scanf("%d", &score[i][j]);
		}
	}
}

void prt_scores(int score[3][4]) // int score[][4] => int (*score)[4]
{
	for (int i = 0; i < 3; i++)
	{
		int total = 0;
		for (int j = 0; j < 4; j++)
		{
			total += score[i][j];
		}
		double avg = total / 4.0;
		printf("총점 : %d, 평균 : %.2lf\n", total, avg);
	}
}

*/
/*
int main()
{
	int score[2][3][4] =
	{
		{{72,80,95,60},{68,98,83,90},{75,72,84,90}},
		{{66,85,90,88},{95,92,88,85},{43,72,56,75}}
	};
	int i, j, k;
	for (i = 0; i < 2; i++)
	{
		printf("d반의 점수....\n", i + 1);
		for (j = 0; j < 3; j++)
		{
			for (k = 0; k < 4; k++)
			{
				printf("%d", score[i][j][k]);
			}
			printf("\n");
		}
		printf("\n");
	}
}

*/
/*

#include <stdio.h>

//void get_scores(int(*score)[4]);
void get_scores(int* score);
void prt_scores(int score[3][4]);
int main(void)
{
	//int iar[3]; // iar[0] <=> int, &iar[0] <=> int *ip
	int score[3][4]; // score[0] <=> int[4], &score[0] <=> int(*sp)[4]  
	int total;
	double avg;

	get_scores((int*)score); // &score[0] => int[4] * => int(*)[4]
	prt_scores(score);
}

//void get_scores(int score[3][4]);
//void get_scores(int score[][4]);
//void get_scores(int(*score)[4])
void get_scores(int* score)
{
	for (int i = 0; i < 3; i++)
	{
		printf("4과목의 점수 입력: ");
		for (int j = 0; j < 4; j++)
		{
			//scanf("%d", &score[i][j]);
			scanf("%d", &score[i * 4 + j]);
		}
	}
}

void prt_scores(int score[3][4]) // int score[][4] => int (*score)[4]
{
	for (int i = 0; i < 3; i++)
	{
		int total = 0;
		for (int j = 0; j < 4; j++)
		{
			total += score[i][j];
		}
		double avg = total / 4.0;
		printf("총점 : %d, 평균 : %.2lf\n", total, avg);
	}
}


int main()
{
	char stat[5][5] = {
		{'x',' ',' ',' ','x'},
		{' ','x',' ','x',' '},
		{' ',' ','x',' ',' '},
		{' ','x',' ','x',' '},
		{'x',' ',' ',' ','x'},
	};
	int i, j;
	for (i = 0; i < 5; i++) {
		for (j = 0; j < 5; j++) {
			printf("% c", stat[i][j]);
		}
		printf("\n");
	}
}


*/
/*
int main()
{
	char* pary[5];
	int i;

	
	pary[0] = "dog";
	pary[1] = "elephant";
	pary[2] = "hores";
	pary[3] = "tiger";
	pary[4] = "lion";
	for (i = 0; i < 4; i++)
	{
		printf("%s\n", pary[i]);
	}

	return 0;
}
*/
/*
#include <stdio.h>
void print_ary(int** pary);
int main(void)
{
	int ary1[4] = { 1,2,3,4 };
	int ary2[4] = { 11,12,13,14 };
	int ary3[4] = { 21,22,23,24 };
	int* pary[3] = { ary1,ary2,ary3 };
	// |&ary1[0]|&ary2[0]|&ary3[0]| => |int *|int *|int *|
	// => int *pary[3]

	print_ary(pary); // &pary[0] => * => int* *
}
void print_ary(int** pary)
{
	for (int i = 0; i < 3; i++)
	{
		for (int j = 0; j < 4; j++)
		{
			printf("%5d", pary[i][j]);// *(*(pary+i)+j)
		}
		printf("\n");
	}
}
*/

/*
int main()
{
	char a[4][10] = { "horse","fox","hippo","tiger" };
	char* pa[] = { &a[0][0],&a[1][0],&a[2][0],&a[3][0] };
	int count;
	count = sizeof(pa) / sizeof(pa[0]);
	printf_hope(pa, count);
}

void print_hope(char **pa, int count)
{
	for (int i = 0; i < count; i++)
	{
		printf("%c", pa[i][i]);
	}
	return 0;
}

*/
/*
int main()
{
	int iaa[5][6] = {
	   {1,2,3,4,5},
	   {6,7,8,9,10},
	   {11,12,13,14,15},
	   {16,17,18,19,20}
	};

	for (int row = 0; row < 5; row++) {
		for (int col = 0; col < 6; col++) {
			printf("%5d", iaa[row][col]);
		}
		printf("\n");
	}

	for (int row = 0; row < 4; row++)
	{
		int sum = 0;
		for (int col = 0; col < 5; col++)
		{
			sum += iaa[row][col];
		}
		iaa[row][5] = sum;
	}
	for (int col = 0; col < 5; col++)
	{
		int sum = 0;
		for (int row = 0; row < 4; row++)
		{
			sum += iaa[row][col];
		}
		iaa[4][col] = sum;
	}

}
*/

/*
int main()
{
	int a = 10;
	int* pi;
	int** ppi;

	pi = &a;
	ppi = &pi;
	
	printf("-------------------------------------\n");
	printf("변수		변수값		&연산		**연산\n");
	printf("-------------------------------------\n");
	printf("a%12d%12u\n", a, &a);
	printf("pi%12u%12u%12d\n",pi, &pi,*pi);
	printf("ppi%12u%12u%12u%12d\n", ppi, &ppi, *ppi,**ppi);
	printf("-------------------------------------\n");
}

*/
/*
void swap_ptr(char** ppa, char** ppb);

int main()
{
	char* pa = "success";
	char* pb = "failure";

	printf("pa ->%s, pb -> %s\n", pa, pb);
	swap_ptr(&pa, &pb);
	printf("pa ->%s, pb -> %s\n", pa, pb);
	return 0;
}

void swap_ptr(char** ppa, char** ppb)
{
	char* pt;

	pt = *ppa;
	*ppa = *ppb;
	*ppb = pt;
}

*/


/*
void print_str(char** pps, int cnt);

int main()
{
	char* ptr_ary[] = { "eagle","tiger","lion","squirrle" };
	int count;

	count = sizeof(ptr_ary) / sizeof(ptr_ary[0]);
	prit_str(ptr_ary, count);
	return 0;
}
void print_str(char** pps, int cnt)
{
	int i;
	for (i = 0; i < cnt; i++)
	{
		printf("%s\n", pps[i]);
	}
}

*/

/*
void print_ary(int(*)[4]);

int main()
{
	int ary[3][4] = { {1,2,3,4},{5,6,7,8},{9,10,11,12} };
	print_ary(ary);
	return 0;
}
void print_ary(int(*pa)[4])
{
	int i, j;
	for (i = 0; i < 3; i++)
	{
		for (j = 0; j < 4; j++)
		{
			printf("%5d",pa[i][j]);
		}
		prinf("\n");
	}
}

*/

/*
int main()
{
	double grade = 4.5;
	double* pg =&grade;
	double** ppg = &pg;

	printf("%.1lf\n", **ppg);
	printf("%u\n", &ppg);
	printf("%u\n", *&pg);
	printf("%u\n", **ppg);
	printf("%u\n", &*ppg);
}
*/


/*
int main()
{
	int a = 10, b = 20;
	int* pa = &a, * pb = &b;
	int** ppa = &pa, ** ppb = &pb;
	int *pt;
	
	pt = *ppa;
	*ppa = *ppb;
	*ppb = pt;

	printf("a:%d, b:%d\n", a, b);
	printf("*pa:%d, *pb:%d\n", *pa, *pb);
}
*/

//오눌운 컨디션아 별로 좋자 얺어 누어있습니다

/*
int main()
{
	int* pi;
	int i, sum = 0;
	pi = (int*)malloc(5 * sizeof(int));
	if (pi == NULL)
	{
		printf("메모리가 부족합니다\n");
		exit(1);
	}
	printf("다섯명의 나이를 입력하시오: ");
	for (i = 0; i < 5; i++)
	{
		scanf("%d", &pi[i]);
		sum += pi[i];
	}
	printf("다섯명의 평균 나이:%.1lf\n", (sum / 5.0));
	free(pi);

	return 0;

}



//-------------------------------------------------------------------------
int main()
{
	int* pi;
	int size = 5;
	int count = 0;
	int num;
	int i;

	pi = (int*)calloc(size, sizeof(int));
	while (1)
	{
		printf("양수만 입력하세요 => ");
		scanf("%d", &num);
		if (num <= 0)break;
		if (count == size)
		{

		}
	}
}
*/
/*
int main()
{
	int** matrix;
	int(*iap)[5];
	iap = (int(*)[5])malloc(sizeof(int) * 4 * 5);//int iaa[4][5]
		for (int i = 0; i < 4; i++)
	{
		for (int j = 0; j < 5; j++)
		{
			iap[i][j] = i * j;
		}
	}
		for (int i = 0; i < 4; i++)
		{
			printf("%3d", iap[i][j]);
		}
		printf("\n");
}

*/
/*
struct student
{
	int num;
	double grade;
};

int main()
{
	struct student s1;
	s1.num = 2;
	s1.grade = 2.7;
	printf("학번: %d\n",s1.num);
	printf("학점: %.1lf\n", s1.grade);
	return 0;

}
*/
/*
struct profile
{
	char name;
	int age;
	double height;
	char* intro;
};
int main()
{
	struct  profile yuni;
	strcpy(yuni.name, "서하윤");
	yuni.age = 17;
	yuni.height = 164.5;

	yuni.intro = (char*)malloc(80);
	printf("자기소개: ");
	gest(yuni.intro);

	printf("이름:%s\n", yuni.name);
	printf("나이:%d\n", yuni.age);
	printf("키: %.1lf\n", yuni.height);
	printf("자기소개: %s\n", yuni.intro);

	return 0;
}

*/
/*
struct profile
{
	int age;
	double height
};

struct student
{
	struct profile pf;
	int id;
	double grade;
};
int main()
{
	struct studnt y;
	y.pf.g = 17;
	y.pf.h = 164.5;
	y.id = 315;
	y.g = 4.3;
}
*/
/*
struct student
{
	int id;
	char name;
	double grade;
};
int main()
{
	struct student s1 = { 315,"홍길동",2.4 }, s2 = { 316,"이순신",3.7 }, s3 = { 317,"새종대왕",4.4 };

	struct student max;
	
	max = s1;
	if (s2.grade > max.grade)max = s2;
	if (s3.grade > max.grade)max = s3;

	printf("학번:%d\n", max.id);
	printf("이름:%s\n", max.name);
	printf("학점:%.1lf\n", max.grade);
}
*/
/*
struct vision
{
	double left;
	double right;
};

struct vision exchange(struct vision robot);

int main()
{
	struct vision robot;

	printf
}

*/

/*
int main()
{
	char buffer[1024];
	const char* file_name = "C:\\visdyC\\first\\교보문고_종합_베스트셀러_상품리스트.csv";
	FILE* fbook = fopen(file_name, "r");
	while (1)
	{
	char *ret=fgets(buffer, 1024, fbook);
	if (ret == NULL) break;
	}
	fclose(fbook);
	printf("%s", buffer);
	char* 순위, *상품코드,*판매상품ID,*상품명,*정가,*판매가,*할인율,*적립율,*적립예정포인트,*인물,*출판사,*발행일자,*분야;
	printf("siezof(상품코드)=%d\n", sizeof(상품코드));
	순위 = buffer;
	상품코드 = buffer + 4;
	printf("%s", 상품코드);
	char* postit[13];
	postit[0] = &buffer[0];
	int cnt;
	for (int i = 0; i < 13; i++)
	{
		while (buffer[cnt]!=',')
		{
			cnt++;
		}
		buffer[cnt] = '\0';
		cnt++;
		postit[i] = &buffer[cnt];		
	}
	printf("%s%s%s\n", postit[0], postit[1], postit[2]);
	printf("%s%s%s\n", postit[3], postit[4], postit[5]);
}
*/





//--------------------------------



/*

int main()
{
	// 1 단계 - 파일 읽어 보기
	
	char buffer[1024];// 3
	const char* file_name= "C:\\Users\\main\\Downloads\\교보문고_종합_베스트셀러_상품리스트.txt";
	FILE* fbook=fopen(file_name, "r");// 1
	fgets(buffer, 1024, fbook);// 2
	printf("%s", buffer);// 4
	fgets(buffer, 1024, fbook);// 2
	printf("%s", buffer);// 4
	fclose(fbook); //5
	

	// 2. 파일 전체 읽어 보기
	
	char buffer[1024];// 3
	const char* file_name = "C:\\Users\\main\\Downloads\\교보문고_종합_베스트셀러_상품리스트.txt";
	FILE* fbook = fopen(file_name, "r");// 1
	while (1) {
	   char * ret=fgets(buffer, 1024, fbook);
	   if (ret == NULL) break;
	   printf("%s", buffer);// 4
	}
	fclose(fbook); //5
	
	// 3. parsing

	char buffer[1024];// 3
	const char* file_name = "C:\\Users\\main\\Downloads\\교보문고_종합_베스트셀러_상품리스트.txt";
	FILE* fbook = fopen(file_name, "r");// 1
	while (1) {
		char* ret = fgets(buffer, 1024, fbook);
		if (ret == NULL) break;
	}
	fclose(fbook); //5
	printf("%s", buffer);// 4
	buffer[strlen(buffer) - 1] = '\0';
	// 순위, 상품코드, 판매상품ID, 상품명, 정가, 판매가, 할인율, 
	// 적립율, 적립예정포인트, 인물, 출판사, 발행일자, 분야   
	char* postit[13];
	postit[0] = &buffer[0];
	int cnt = 0;
	for (int i = 1; i < 13; i++) {
		while (buffer[cnt] != '\t') {
			cnt++;
		}
		buffer[cnt] = '\0';
		cnt++;
		postit[i] = &buffer[cnt];
	}
	for (int i = 0; i < 13; i++)
		printf("%s\n", postit[i]);
}

*/

/*
int main()
{
	FILE* fp;
	double max;
	max = 100000;
	fp = fopen ("C:\\visdyC\\first\\2024년5월기준_그래픽카드_성능순위.txt","r");
	char bufffer[max] = { 0, };


	printf("%s\n", fp);
}
*/

/*
struct list
{
	int num;
	struct list *next;
};
int main()
{
	struct list a ={10,0}
}
*/

/*
typedef struct list {
	int num;
	struct list* next;
} list_t;

int main(void) {

	list_t* head = NULL;
	list_t* prev_node = NULL;
	for (int i = 0; i < 100; i++) {
		list_t* node = (list_t*)malloc(sizeof(list_t) * 1);
		node->num = i;
		node->next = NULL;
		if (i == 0) {
			head = node;
			prev_node = node;
		}
		else {
			prev_node->next = node;
			prev_node = node;
		}
	}

	list* current;
	current = head;
	while (current != NULL) {
		printf("%d->", current->num);
		current = current->next;
	}
	printf("NULL\n");
}
*/

/*
typedef struct list {
   int num;
   struct list* next;
} list_t;

int main(void) {

   list_t* head=NULL;
   list_t* prev_node = NULL;
   for (int i = 0; i < 50000000; i++) {
      list_t * node = (list_t *)malloc(sizeof(list_t) * 1);
      node->num = i;
      node->next = NULL;
      if (i == 0) {
         head = node;
         prev_node = node;
      }
      else {
         prev_node->next = node;
         prev_node = node;
      }
   }

   list_t* current;
   current = head;
   while (current != NULL) {
      if(current->next==NULL)
         printf("%d->", current->num);
      current = current->next;
   }
   printf("NULL\n");
}
*/

/*

typedef char byte_t;
typedef union int_byte {
   int i;
   byte_t byte[4];
} int_byte_ut;

typedef union double_int {
   double d;
   int i[2];
   byte_t b[8];
} double_int_ut;

typedef union str_int {
   char msg[32];// "hello world~";
   int data[8];
} str_int_ut;

int main()
{
   int i = 0xabcdef01;
   int_byte_ut iu = { 0xabcdef01 };
   printf("iu:%x\n", iu.i);
   printf("%x %x %x %x\n", iu.byte[0], iu.byte[1],
      iu.byte[2], iu.byte[3]);

   double_int_ut du = { 3.14 };
   printf("%x %x\n", du.i[0], du.i[1]);

   str_int_ut su = { "aabbccddeeff" };
   printf("%x %x %x %x\n", su.data[0], su.data[1], 
      su.data[2], su.data[3]);
}
*/

/*
struct student
{
	int num;
	double grade;
};

typedef struct student student;

void print_data(student* ps);

int main()
{
	student s1=(315, 4.2);
	print_data(&s1);
	return 0;
}
void print_data(student* ps)
{
	printf("학번: %d\n", ps->num);
	printf("학점: %.1lf\n", ps->grade);
}

*/

/*
int main()
{
	FILE* fp;
	fp = fopen("a.txt", "r");
	if (fp == NULL)
	{
		printf("파일이 열리지 않았습니다.\n");
		return 0;
	}
	printf("파일이 열렸습니다.\n");
	fclose(fp);

	return 0;
}

*/

/*
int main()
{
	FILE* fp;
	const char* letters = "abcdefghizklmnopqrstuvw";
	srand(time(NULL));

	for (int i = 0; i < 1000000; i++)
	{
		int index = rand() % 27;
		printf("%c", letters[index]);
	}
	fp = fopen("a.txt", "w");
	fclose(fp);
}
*/


/*int main()
{
	FILE* fp;
	int ch;

	fp = fopen("a.txt", "r");
	if (fp == NULL)
	{
		printf("파일이 열리지 않았습니다.\n");
		return 1;
	}
	while (1)
	{
		ch = fgetc(fp);
		if (ch == EOF)
		{
			break;
		}
		putchar(ch);
	}
	fclose(fp);
	return 0;
*/

/*
int main()
{
	FILE* fp;
	char str[] = "banana";
	int i;
	fp = fopen("b.txt", "w");
	if (fp == NULL)
	{
		printf("파일을 만들지 못했습니다");
		return 0;
	}
	i = 0;
	while (str[i] != '\0')
	{
		fputc(str[i], fp);
		i++;
	}
	fputc('\n', fp);
	fclose(fp);
}
*/


/*
int main()
{
	int ch;
	
	while (1)
	{
		ch = getchar();
		if (ch == EOF)
		{
			break;
		}
		putchar;
	}
	return 0;
}
*/
/*
int main()
{
	int ch;
	while (1)
	{
		ch = fgetc(stdin);
		if (ch == EOF)
		{
			break;
		}
		fputc(ch, stdout);
	}
	return 0;
}
*/


 /*
int main()
{
	FILE* fp;
	int ary[10] = { 13,10.13,13,10,26,13,10,13,10 };
	int i, res;

	fp = fopen("a.txt", "wb");
	for (i = 0; i < 10; i++)
	{
		fqutc(ary[i], fp);
	}
	fclose(fp);

	fp = fopen("a.txt", "rt");
	while (1)
	{
		res = fgect(fp);
		if (res == EOF)break;
		printf("%4d", res);
	}
	fclose(fp);
	return 0;
}
*/

/*
int main()
{
	FILE* fp;
	char str[20];

	fp = fopen("a.txt", "a+");
	if (fp == NULL)
	{
		printf("파일을 만들지 못했습니다");
		return 1;
	}
	while (1)
	{
		printf("과일이름: ");
		scanf('%s', str);
		if (strcmp(str, "end") == 0)
		{
			break;
		}
		else if (strcmp(str, "list") == 0)
		{
			fseek(fp, 0,SEEK_SET);
			while (1)
			{
				fgetc(str, sizeof(str), fp);
				if (feof(fp))
				{
					break;
				}
				printf("%d", str);
			}
		}
		else
		{
			fprintf(fp, "%s\n", str);
		}
	}
	fclose(fp);

	return 0;
}
*/

/*
int main()
{
	FILE* fp;
	int age;
	char name[20];

	fp = fopen("a.txt", "r");

	fscanf(fp, % d, &age);
	fgets(name, sizeof(name), fp);

	printf("나이:%d 이름:%s,age,name");
	fclose(fp);

	return 0;
}
*/


/*
int main(int argc, char** argv)
{
	//mycopy.exe screen.png screen.bk.png
	printf("%s %s %s\n", argv[0], argv[1], argv[2]);
	FILE* fsrc = fopen(argv[1], "rb");
	if (fsrc == NULL) return -1;
	FILE* fdst = fopen(argv[2], "wb");
	fseek(fsrc, 0, SEEK_END);
	long flen = ftell(fsrc);
	fseek(fsrc, 0, SEEK_SET);
	char* buffer = (char*)malloc(sizeof(char) * flen);
	for (int i = 0; i < flen; i++) {
		fread(&buffer[i], sizeof(char), 1, fsrc);
	}
	fclose(fsrc);
	for (int i = 0; i < flen; i++) {
		fwrite(&buffer[i], sizeof(char),1, fdst);
	}
	fclose(fdst);
	return 0;
}

*/
/*
int main()
{
	FILE* fp;
	char str[20] = "empty";
	int ch;

	fp = fopen("a.txt", "r");
	ch = fgetc(fp);
	while (fgetc(fp) != EOF);

	fgets(str, sizeof(str), fp);
	printf("%s", str);
	fclose(fp);

	return 0;
}

*/
/*
int main() {

	FILE* afp;
	char buffer[256] ;
	
	afp = fopen("C:\\visdyC\\first\\a_test.txt", "r");
	if (afp == NULL)
	{
		printf("파일이 열리지 않습니다");
		return 1;
	}
	while (fgets(buffer, sizeof(buffer), afp))
	{
		printf("%s", buffer);
	}
	fclose(afp);

	return 0;
}	
*/

/*
#define MAX_LINES 256
#define MAX_LENGTH 256

int main() {
	FILE* fileA, * fileB, * fileC;
	char bufferA[MAX_LENGTH];
	char bufferB[MAX_LENGTH];
	char* linesA[MAX_LINES];
	int lineCountA = 0;
	int i, found;

	// 첫 번째 파일 열기
	fileA = fopen("C:\\visdyC\\first\\a_test.txt", "r");
	if (fileA == NULL) {
		printf("파일 a_test.txt을 열 수 없습니다.\n");
		return 1;
	}

	// 두 번째 파일 열기
	fileB = fopen("C:\\visdyC\\first\\b_test.txt", "r");
	if (fileB == NULL) {
		printf("파일 b_test.txt을 열 수 없습니다.\n");
		fclose(fileA);
		return 1;
	}

	// 세 번째 파일 쓰기 모드로 열기
	fileC = fopen("C:\\visdyC\\first\\c_test.txt", "w");
	if (fileC == NULL) {
		printf("파일 c_test.txt을 생성할 수 없습니다.\n");
		fclose(fileA);
		fclose(fileB);
		return 1;
	}

	// a_test.txt의 모든 줄을 읽어서 메모리에 저장
	while (fgets(bufferA, sizeof(bufferA), fileA) != NULL) {
		bufferA[strcspn(bufferA, "\r\n")] = 0;  // 개행 문자 제거
		linesA[lineCountA] = strdup(bufferA);   // 줄을 복사하여 저장
		if (linesA[lineCountA] == NULL) {
			printf("메모리 할당 실패\n");
			fclose(fileA);
			fclose(fileB);
			fclose(fileC);
			return 1;
		}
		lineCountA++;
	}

	// b_test.txt의 각 줄을 읽어서 a_test.txt에 있는지 확인하고 없으면 c_test.txt에 기록
	while (fgets(bufferB, sizeof(bufferB), fileB) != NULL) {
		bufferB[strcspn(bufferB, "\r\n")] = 0;  // 개행 문자 제거
		found = 0;
		for (i = 0; i < lineCountA; i++) {
			if (strcmp(bufferB, linesA[i]) == 0) {
				found = 1;
				break;
			}
		}
		if (!found) {
			fprintf(fileC, "%s\n", bufferB);
		}
	}

	// 메모리 해제
	for (i = 0; i < lineCountA; i++) {
		free(linesA[i]);
	}

	// 모든 파일 닫기
	fclose(fileA);
	fclose(fileB);
	fclose(fileC);

	return 0;
}

*/
//---------------------------------------------------------------------------------------------------------580p
/*

int main()
{
	// 1. 파일 읽어보기 테스트
	/*FILE* fpa = fopen("a1.txt", "r");
	char buffer[21];
	fgets(buffer, 21, fpa);
	printf("%s\n", buffer);
	fclose(fpa);*/

	// 2. 파일 직접 만들기
	/*fpa = fopen("a1.txt", "w");
	fputs("dog\ntiger\nhorse\nmonkey\nlion\nkoala\n", fpa);
	fputs("giraffe\nowl\n", fpa);
	fclose(fpa);*/

	// 3. a.txt 파일 다 읽어보기
	/*FILE* fpa = fopen("a.txt", "r");
	char buffer[21];
	while (1) {
	   if (fgets(buffer, 21, fpa) == NULL) break;
	   printf("%s\n", buffer);
	}
	fclose(fpa);*/

	// 4. fgets '\n' 제거하기
	/*FILE* fpa = fopen("a.txt", "r");
	char buffer[21];
	while (1) {
	   if (fgets(buffer, 21, fpa) == NULL) break;
	   buffer[strlen(buffer) - 1] = '\0';
	   printf("%s\n", buffer);
	}
	fclose(fpa);*/

	// 5. 등록된 단어 개수 세기
	/*FILE* fpa = fopen("a.txt", "r");
	char buffer[21];
	int cnt = 0;
	while (1) {
	   if (fgets(buffer, 21, fpa) == NULL) break;
	   cnt++;
	   buffer[strlen(buffer) - 1] = '\0';
	   printf("%s\n", buffer);
	}
	printf("cnt=%d\n", cnt);
	fclose(fpa);*/

	// 6. 등록 단어 2차 배열 만들고 채우기
	// char regs[cnt][21];
	/*FILE* fpa = fopen("a.txt", "r");
	char buffer[21];
	int cnt = 0;
	while (1) {
	   if (fgets(buffer, 21, fpa) == NULL) break;
	   cnt++;
	   buffer[strlen(buffer) - 1] = '\0';
	   printf("%s\n", buffer);
	}
	printf("cnt=%d\n", cnt);
	char (*regs)[21]=(char(*)[21])malloc(sizeof(char) * cnt * 21);
	// char regs[8][21];
	// &regs[0] => char(*)[21]
	fseek(fpa, 0, SEEK_SET);
	for (int i = 0; i < cnt; i++) {
	   fgets(regs[i], 21, fpa);
	   regs[i][strlen(regs[i]) - 1] = '\0';
	   printf("regs[%d]:%s\n", i , regs[i]);
	}
	fclose(fpa);*/

	// 7. 등록 단어 2차 배열을 1차 배열로 처리하기
	// char regs[cnt*21];// 수정 0
	/*FILE* fpa = fopen("a.txt", "r");
	char buffer[21];
	int cnt = 0;
	while (1) {
	   if (fgets(buffer, 21, fpa) == NULL) break;
	   cnt++;
	   buffer[strlen(buffer) - 1] = '\0';
	   printf("%s\n", buffer);
	}
	printf("cnt=%d\n", cnt);
	char *regs=(char *)malloc(sizeof(char) * cnt * 21); // 수정 1
	// char regs[8*21]; // 수정 2
	// &regs[0] => char * // 수정 3
	fseek(fpa, 0, SEEK_SET);
	char* pword=NULL; // 추가
	for (int i = 0; i < cnt; i++) {
	   pword = &regs[i * 21]; // 추가
	   fgets(pword, 21, fpa); // 수정
	   pword[strlen(pword) - 1] = '\0'; // 수정
	   printf("regs[%d*21]:%s\n", i , &regs[i*21]); // 수정
	}
	fclose(fpa);*/
/*
	// 8. read_word_list 함수 만들기
	// word_list = read_word_list("a.txt", &word_cnt);
	// char *word_list;
	char* read_word_list(const char*, int*);
	char* alist;
	int acnt;
	alist = read_word_list("a.txt", &acnt);
	//printf("rcnt=%d\n", rcnt);
	//printf("%s %s %s\n", rlist, rlist+21, rlist+42);
	char* blist;
	int bcnt;
	blist = read_word_list("b.txt", &bcnt);
	//printf("icnt=%d\n", icnt);
	//printf("%s %s %s\n", ilist, ilist+21, rlist+42);
*/
	// 9. 검출 하기
	/*for (int b = 0; b < bcnt; b++) {
	   //printf("%s\n", &blist[b * 21]);
	   int a;
	   char* bstr=NULL;
	   for (a = 0; a < acnt; a++) {
		  //printf("%s\n", &alist[a * 21]);
		  bstr = &blist[b * 21];
		  char* astr = &alist[a * 21];
		  if (strcmp(bstr, astr) == 0) {
			 //printf("%s\n", bstr);
			 break;
		  }
	   }
	   //printf("a:%d\n", a);
	   if (a == acnt) printf("%s\n", bstr);
	}*/
/*
	// 10. c.txt 파일 출력하기
	FILE* fpc = fopen("c.txt", "w");
	for (int b = 0; b < bcnt; b++) {
		int a;
		char* bstr = NULL;
		for (a = 0; a < acnt; a++) {
			bstr = &blist[b * 21];
			char* astr = &alist[a * 21];
			if (strcmp(bstr, astr) == 0) {
				break;
			}
		}
		if (a == acnt) fprintf(fpc, "%s\n", bstr);
	}
	fclose(fpc);
}

char* read_word_list(const char* fname, int* wcnt) {
	FILE* fpa = fopen(fname, "r");
	char buffer[21];
	int cnt = 0;
	while (1) {
		if (fgets(buffer, 21, fpa) == NULL) break;
		cnt++;
		buffer[strlen(buffer) - 1] = '\0';
		//printf("%s\n", buffer);
	}
	//printf("cnt=%d\n", cnt);
	char* regs = (char*)malloc(sizeof(char) * cnt * 21); // 수정 1
	// char regs[8*21]; // 수정 2
	// &regs[0] => char * // 수정 3
	fseek(fpa, 0, SEEK_SET);
	char* pword = NULL; // 추가
	for (int i = 0; i < cnt; i++) {
		pword = &regs[i * 21]; // 추가
		fgets(pword, 21, fpa); // 수정
		pword[strlen(pword) - 1] = '\0'; // 수정
		//printf("regs[%d*21]:%s\n", i, &regs[i * 21]); // 수정
	}
	fclose(fpa);
	*wcnt = cnt;// 추가
	return regs; // &regs[0] => char * , 추가
}

*/


#include "studnt.h"
/*
int main()
{
	student a = { 315,"홍길동" };
	printf("학번:%d, 이름:%s\n", a.num, a.name);
}



#define PI 3.14159
#define LIMIT 100.0
#define MSG "passed!"
#define ERR_PRN printf("허용 범위를 벗어 났습니다!\n")
*/


/*
int input_data(void);
double average(void);
void print_data(double);

int count = 0;
static int total = 0;
*/
/*
#define SUM(a,b) ((a)+(b))
#define SUB(a,b) ((a)-(b))
#define MUL(a,b) ((a)*(b))
#define DIV(a,b) ((a)/(b))
int main()
{
	while (1) {
		// 1. 메뉴 보여주기
		printf("수식 입력(종료 Ctrl+Z) : ");
		int a, b;
		char op;
		int res;
		// 2. 명령 받기
		if (scanf("%d %c%d", &a, &op, &b) == EOF) break;

		// 3. 명령 처리
		switch (op) {
		case '+':
			res = SUM(a, b);
			printf("%d %c %d = %d\n", a, op, b, res);
			break;
		case '-':
			res = SUB(a, b);
			printf("%d %c %d = %d\n", a, op, b, res);
			break;
		case '*':
			res = MUL(a, b);
			printf("%d %c %d = %d\n", a, op, b, res);
			break;
		case '/':
			res = DIV(a, b);
			printf("%d %c %d = %d\n", a, op, b, res);
			break;
		default: break;
		}
	}
}


*/


/*
메뉴 기반도서 관리 프로그렘을 만드려한다
book의 구조체(도서명,작가)를 선언하려 구조체 배열로 도서 목록을 관리 하여라

char*title 도서명
char*author 작가

정수형 전역변수를 사용하여 입력된 도서수를 관리
기능(메뉴):1도서 목록출력 도서 추가 9총료
프로그럼 시작시 txt파일의 데이터를읽어와서  구조체 배열에 셋팅
정수형메뉴를 입력받아 각 기능수행
프로그렘 종료 9번시 모든 파일에 wtite하고프로그렘 시작시 파일에서도서 목록을 불러와 배열에 저장

파일명 book_list은 다음과 같은 형태로 저장

파입 입출력및 각기성의 별도 함수 작성
메뉴를 출력하는 함수 void_dispaly_menu()
파일을 읽어 도서 배열에 저장하는 함수 void_read_file(book*book)
도서 목록을 출력하는 함수 void add_book(book*book)
문자배열을 매개변수로 받아 동적할당&문자열을 복사하여 변환하는 함수
char*make_string(char*str)
*/

/*
#include <stdio.h>
int main()

{
	int a;
	// book 리스트 읽기

 	FILE* fp = fopen("book.txt", "r");
	char buffer[255];
	int cnt = 0;
	while (1) {
   if (fgets(buffer, 255, fp) == NULL) break;
   cnt++;
   buffer[strlen(buffer) - 1] = '\0';
   printf("%s\n", buffer);
}
	printf("cnt=%d\n", cnt);
	fclose(fp);
	

	printf("< 도서 관리 프로그렘 >\n");
	printf("1.도서목록 추가\n");
	printf("2.도서 관리\n");
	printf("9.종료\n");

	printf("메뉴 입력: ");
	scanf("%d", &a);

	printf("입력한 번호는: %d\n 입니다", a);
}*/

/*
int main() {
	int a;
	int running = 1; // 프로그램이 실행 중임을 나타내는 변수

	while (running) {
		// 선택지 출력
		printf("< 도서 관리 프로그렘 >\n");
		printf("1.도서목록 추가\n");
		printf("2.도서 관리\n");
		printf("9.종료\n");

		// 사용자로부터 선택지 입력 받기
		printf("선택할 번호를 입력하세요: ");
		scanf("%d", &a);

		// 선택지에 따른 동작 수행
		switch (a) {
		case 1:
			printf("1번을 선택했습니다.\n");
			FILE* fp = fopen("book.txt", "r");
			char buffer[255];
			int cnt = 0;
			while (1) {
				if (fgets(buffer, 255, fp) == NULL) break;
				cnt++;
				buffer[strlen(buffer) - 1] = '\0';
				printf("%s\n", buffer);
			}
			printf("cnt=%d\n", cnt);
			fclose(fp);
			break;
		case 2:
			printf("2번을 선택했습니다.\n");
			// 2번 선택 시 실행할 코드
			break;
		case 9:
			printf("9번을 선택했습니다.\n");
			// 9번 선택 시 실행할 코드
			break;
		case 0:
			printf("프로그램을 종료합니다.\n");
			running = 0; // 프로그램 종료
			break;
		default:
			printf("잘못된 선택입니다.\n");
			break;
		}
	}

	return 0;
}
*/


/*

#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MAX_LINE_SIZE 1024
#define MAX_COLS 10

int main() {
	int a;
	int running = 1; // 프로그램이 실행 중임을 나타내는 변수

	while (running) {
		// 선택지 출력
		printf("< 도서 관리 프로그램 >\n");
		printf("1. 도서 목록 추가\n");
		printf("2. 도서 관리\n");
		printf("9. 종료\n");

		// 사용자로부터 선택지 입력 받기
		printf("선택할 번호를 입력하세요: ");
		scanf("%d", &a);

		// 선택지에 따른 동작 수행
		switch (a) {
		case 1: {
			printf("1번을 선택했습니다.\n");
			FILE* fp = fopen("book_list.csv", "r");
			if (fp == NULL) {
				perror("파일을 열 수 없습니다");
				break;
			}

			char buffer[MAX_LINE_SIZE];
			int cnt = 0;
			while (fgets(buffer, sizeof(buffer), fp) != NULL) {
				// 각 줄을 파싱하여 원하는 열의 데이터만 출력
				char temp_buffer[MAX_LINE_SIZE];
				strcpy(temp_buffer, buffer); // 버퍼를 복사하여 사용
				char* token = strtok(temp_buffer, ","); // , 을 기준으로 분리
				int col_count = 0;
				while (token != NULL) {
					col_count++;
					if (col_count == 4 || col_count == 10) {
						printf("%s\n", token);
					}
					token = strtok(NULL, ",");
				}
				cnt++;
			}
			printf("총 %d개의 항목이 있습니다.\n", cnt);
			fclose(fp);
			break;
		}
		case 2:
			printf("2번을 선택했습니다.\n");
			// 2번 선택 시 실행할 코드
			break;
		case 9:
			printf("프로그램을 종료합니다.\n");
			running = 0; // 프로그램 종료
			break;
		default:
			printf("잘못된 선택입니다.\n");
			break;
		}
	}

	return 0;
}
*/


/*
#include <stdio.h>
#include <string.h>
#include <malloc.h>
typedef struct _Book { // 3-1
	char* title;
	char* author;
} Book;
void read_file(Book* book);
void display_menu(void);
int get_odrder(void);
void print_books(Book* book);
void add_book(Book* book);
void write_file(Book* book);

Book book[200];
int book_cnt = 0;
int main() {
	read_file(book); // 3-2 &book[0]=>Book * book
	while (1) {
		display_menu(); // 1
		int order = get_odrder(); // 2
		switch (order) {
		case 1: print_books(book); break; // 4 &book[0]
		case 2: add_book(book); break; // 5 &book[0]
		case 9: write_file(book); return 0; // 6 &book[0]
		}
	}
}
char* make_string(char* str) {
	int mlen = strlen(str) + 1;
	char* tbuf = (char*)malloc(sizeof(char) * mlen);
	strcpy(tbuf, str);
	return tbuf;
}
void read_file(Book* book) {
	FILE* fp = fopen("book_list.txt", "r");
	char buffer[1024];
	int bi = 0;
	while (1) {
		// 1. 제목 읽기
		char* res = fgets(buffer, sizeof(buffer), fp);
		if (res == NULL) break;
		buffer[strlen(buffer) - 1] = '\0';
		book[bi].title = make_string(buffer);

		// 2. 작가명 읽기
		fgets(buffer, sizeof(buffer), fp);
		buffer[strlen(buffer) - 1] = '\0';
		book[bi].author = make_string(buffer);

		bi++;
	}
	book_cnt = bi;
	fclose(fp);
}
void display_menu(void) {
	printf("<< 도서관리 프로그램 >>\n");
	printf("1. 도서목록 출력\n");
	printf("2. 도서 추가\n");
	printf("9. 종료\n");
}
int get_odrder(void) {
	int order;
	printf("메뉴 입력 => ");
	scanf("%d", &order);
	return order;
}
void print_books(Book* book) {
	printf("%-10s %-30s %-30s\n", "번호", "책제목", "저자");
	for (int bi = 0; bi < book_cnt; bi++) {
		printf("%-10d %-30s %-30s\n",
			bi + 1, book[bi].title, book[bi].author);
	}
}
void add_book(Book* book) {
	printf("책 제목 입력 : ");
	char buffer[1024];
	while (fgetc(stdin) != '\n') {}
	fgets(buffer, sizeof(buffer), stdin);
	buffer[strlen(buffer) - 1] = '\0';
	book[book_cnt].title = make_string(buffer);
	printf("책 저자 입력 : ");
	fgets(buffer, sizeof(buffer), stdin);
	buffer[strlen(buffer) - 1] = '\0';
	book[book_cnt].author = make_string(buffer);
	book_cnt++;
}
void write_file(Book* book) {
	FILE* fout = fopen("book_list_out.txt", "w");
	for (int bi = 0; bi < book_cnt; bi++) {
		fprintf(fout, "%s\n%s\n",
			book[bi].title, book[bi].author);
	}
	fclose(fout);
}




*/

/*
#include <stdio.h>
#include <string.h>

typedef struct book { // book.h 로 옮길 수 있다.
   char* 상품코드;
   char* 판매상품ID;
} book_t;
void read_file(book_t* book); // book.h로

book_t book[200];

int main() {
   read_file(book); //&book[0] => book_t * book
}

void read_file(book_t* book) {
   FILE* fin=fopen("book_list.csv", "r");
   char buffer[1024];
   char* 순위=NULL, * 상품코드 = NULL, * 판매상품ID = NULL, * 상품명 = NULL, * 정가 = NULL, * 판매가 = NULL;
   char* 할인율 = NULL, * 적립율 = NULL, * 적립예정포인트 = NULL, * 인물 = NULL, * 출판사 = NULL;
   char* 발행일자 = NULL, * 분야 = NULL;
   int bi = 0;
   while (1) {
	  char* res=fgets(buffer, sizeof(buffer), fin);
	  if (res == NULL) break;

	  buffer[strlen(buffer)-1] = '\0';//

	  int bpos, tcnt = 0;
	  순위 = buffer;
	  for (bpos = 0; buffer[bpos] != '\0'; bpos++) {
		 if (buffer[bpos] == '\t') {
			tcnt++;
			buffer[bpos] = '\0';
			switch (tcnt) {
			case 1: 상품코드 = &buffer[bpos + 1];
			   //book[bi].상품코드 = make_string(상품코드);
			   break;
			case 2:
			   판매상품ID = &buffer[bpos + 1];
			   //book[bi].판매상품ID = make_string(판매상품ID);
			   break;
			case 3: 상품명 = &buffer[bpos + 1]; break;
			case 4: 정가 = &buffer[bpos + 1]; break;
			case 5: 판매가 = &buffer[bpos + 1]; break;
			case 6: 할인율 = &buffer[bpos + 1]; break;
			case 7: 적립율 = &buffer[bpos + 1]; break;
			case 8: 적립예정포인트 = &buffer[bpos + 1]; break;
			case 9: 인물 = &buffer[bpos + 1]; break;
			case 10: 출판사 = &buffer[bpos + 1]; break;
			case 11: 발행일자 = &buffer[bpos + 1]; break;
			case 12:
			   분야 = &buffer[bpos + 1];
			   break;
			default: break;
			}
		 }
	  }
   }
   fclose(fin);
}
}
*/


/*
#include <stdio.h>
#include <string.h>
#include <malloc.h>

typedef struct book { // book.h 로 옮길 수 있다.
	char* 순위;
	char* 상품코드;
	char* 판매상품ID;
	char* 상품명;
	char* 정가;
	char* 판매가;
	char* 할인율;
	char* 적립율;
	char* 적립예정포인트;
	char* 인물;
	char* 출판사;
	char* 발행일자;
	char* 분야;
} book_t;
void read_file(book_t* book); // book.h로 
void print_books(book_t* book);
void search_book(book_t* book);

book_t book[200];

int main() {
	read_file(book); //&book[0] => book_t * book

	print_books(book); //&book[0] => book_t * book

	search_book(book); //&book[0] => book_t * book
}

char* make_string(char* str) {
	int slen = strlen(str) + 1;
	char* sbuf = (char*)malloc(sizeof(char) * slen);
	strcpy(sbuf, str);
	return sbuf;
}

void read_file(book_t* book) {
	FILE* fin = fopen("교보문고_종합_베스트셀러_상품리스트.txt", "r");
	char buffer[1024];
	char* 순위 = NULL, * 상품코드 = NULL, * 판매상품ID = NULL, * 상품명 = NULL, * 정가 = NULL, * 판매가 = NULL;
	char* 할인율 = NULL, * 적립율 = NULL, * 적립예정포인트 = NULL, * 인물 = NULL, * 출판사 = NULL;
	char* 발행일자 = NULL, * 분야 = NULL;
	int bi = 0;
	fgets(buffer, sizeof(buffer), fin);
	while (1) {
		char* res = fgets(buffer, sizeof(buffer), fin);
		if (res == NULL) break;

		buffer[strlen(buffer) - 1] = '\0';//

		int bpos, tcnt = 0;
		순위 = buffer;
		for (bpos = 0; buffer[bpos] != '\0'; bpos++) {
			if (buffer[bpos] == '\t') {
				tcnt++;
				buffer[bpos] = '\0';
				switch (tcnt) {
				case 1: 상품코드 = &buffer[bpos + 1]; break;
				case 2: 판매상품ID = &buffer[bpos + 1]; break;
				case 3: 상품명 = &buffer[bpos + 1]; break;
				case 4: 정가 = &buffer[bpos + 1]; break;
				case 5: 판매가 = &buffer[bpos + 1]; break;
				case 6: 할인율 = &buffer[bpos + 1]; break;
				case 7: 적립율 = &buffer[bpos + 1]; break;
				case 8: 적립예정포인트 = &buffer[bpos + 1]; break;
				case 9: 인물 = &buffer[bpos + 1]; break;
				case 10: 출판사 = &buffer[bpos + 1]; break;
				case 11: 발행일자 = &buffer[bpos + 1]; break;
				case 12: 분야 = &buffer[bpos + 1]; break;
				default: break;
				}
			}
		}
		book[bi].순위 = make_string(순위);
		book[bi].상품코드 = make_string(상품코드);
		book[bi].판매상품ID = make_string(판매상품ID);
		book[bi].상품명 = make_string(상품명);
		book[bi].정가 = make_string(정가);
		book[bi].판매가 = make_string(판매가);
		book[bi].할인율 = make_string(할인율);
		book[bi].적립율 = make_string(적립율);
		book[bi].적립예정포인트 = make_string(적립예정포인트);
		book[bi].인물 = make_string(인물);
		book[bi].출판사 = make_string(출판사);
		book[bi].발행일자 = make_string(발행일자);
		book[bi].분야 = make_string(분야);
		bi++;
	}
	fclose(fin);
}

void print_books(book_t* book) {
	for (int bi = 0; bi < 200; bi++) {
		printf("%s %s %s %s\n", book[bi].순위,
			book[bi].상품명, book[bi].정가, book[bi].인물);
	}
}
void search_book(book_t* book) {
	printf("검색할 책 제목 : ");
	char buffer[1024];
	fgets(buffer, sizeof(buffer), stdin);
	buffer[strlen(buffer) - 1] = '\0';

	for (int bi = 0; bi < 200; bi++) {
		char* title = book[bi].상품명;
		int tlen = strlen(title);
		int blen = strlen(buffer);
		int tpos;
		for (tpos = 0; tpos < tlen - blen + 1; tpos++) {
			if (strncmp(&title[tpos], buffer, blen) == 0) {
				printf("%s\n", book[bi].상품명);
				break;
			}
		}
	}

}
*/
/*
int main()
{
	char 정가[] = "\"14,000\"";
	printf("%s\n", 정가);

	int 정가길이 = strlen(정가);
	printf("정가길이=%d\n", 정가길이);

	char* 정가수정 = (char*)malloc(sizeof(char) * 정가길이);
	int pos2 = 0;
	for (int pos = 0; pos < 정가길이; pos++)
	{
		if (정가[pos] >= '0' && 정가[pos] <= '9');
		{
			정가수정[pos2] = 정가[pos];
			pos2++;
		}
	}
	int price;
	sscanf(정가수정, "%d", &price);
	pirintf("price=%d\n", (int)(price * 0.9));
}
*/

/*
#include <stdio.h>
#include <string.h>
#include <malloc.h>
int make_price(char* sprice);
int main()
{
	char 정가[] = "\"14,000\"";
	int price = make_price(정가); // &정가[0] => char * sprice   
	printf("price=%d\n", price);
}

int make_price(char* sprice) {
	//printf("%s\n", sprice);
	int 정가길이 = strlen(sprice);
	//printf("정가길이=%d\n", 정가길이);
	char* 정가수정 = (char*)calloc(sizeof(char), 정가길이);
	int pos2 = 0;
	for (int pos = 0; pos < 정가길이; pos++) {
		if (sprice[pos] >= '0' && sprice[pos] <= '9') {
			정가수정[pos2] = sprice[pos];
			pos2++;
		}
	}
	//printf("%s(%d)\n", 정가수정, strlen(정가수정));
	// scanf, fscanf, sscanf
	int price;
	sscanf(정가수정, "%d", &price);
	return price;
}

*/
