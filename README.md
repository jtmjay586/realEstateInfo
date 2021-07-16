#python 공부 및 활용을 위한 작은 프로젝트
[requests]


[pandas]      
<https://myjamong.tistory.com/125?category=877809>
<https://myjamong.tistory.com/161>   
<https://3months.tistory.com/292> 참조사이트  
python data analysis library   
dataframe?   
ndarray, dictionary, dataframe, series, list    
Series는 테이블 형식의 데이터로 봤을때 하나의 레코드 즉, 행 값   
s1 = pd.Series([5000,30000,20000,15000])
s1 = pd.Series([5000,30000,20000,15000],
              index=['2020-03-03','2020-03-04','2020-03-05', '2020-03-06'],
              name='durian')
s1.index.name = 'dates'

Dataframe은 Series들의 집합   
index 값과 column 값 없이 생성하게 되면 숫자형태로 0 부터 자동으로 채번  
 
df = pd.DataFrame({
    "2020-03-03" : [4000,5000,6000],
    "2020-03-04" : [20000,8000,9000],
    "2020-03-05" :[10000,11000,12000]
}, index=['apple','bannana','cherry']
)   
다른 방식으로도 표현 가능   
df = pd.DataFrame(
    [
        [4000,20000,10000],
        [5000,8000,11000],
        [6000,9000,12000]
    ], 
)
df.index = [['apple','bannana','cherry']]
df.columns = [['2020-03-03','2020-03-04','2020-03-05']];

컬럼   
로우   
인덱스   

Dataframe 읽기   
* 1 정보 읽기 -> df.index / df.columns / df.values / df.describe()
* 2 행 읽기   -> df['2020-03-03']
* 3 열 읽기   -> df.loc['apple']
* 4 행 숫자 index 읽기 -> df.iloc[0]
* 5 복합 읽기 -> df.loc['apple':'cherry', '2020-03-04':'2020-03-05'] / df.loc[df['2020-03-03']>4000,:] / df[df['2020-03-03':]>4000] 


[python 자료형]   
참조사이트   
<https://dojang.io/mod/page/view.php?id=2205>
* list
<br>
<code>
    a = [] # 빈 리스트 생성 method 1   
    a = list() # 빈 리스트 생성 method 2   
    여러 자료형을 저장 가능함   
    ex) person = ['james', 17, 175.3, True]
</code>

* tuple   
읽기 전용 리스트
<br>
<code>
    a = tuple() # 튜플 생성   
    튜플을 리스트로 만들고 리스트를 튜플로 만들수 있다.   
    tuple 안에 리스트를 넣으면 새 튜플이 생깁니다.
    ex) a = [1, 2, 3]   
        tuple(a)   
        (1, 2, 3)   
    list 안에 튜플을 넣으면 새 리스트가 생성   
    ex) b = (4, 5, 6)   
        list(b)   
        [4, 5, 6]   
    패킹 언패킹       
    ex)
        input().split()   
        10 20   
        ['10', '20']   
        x = input().split()   
        10 20   
        a, b = x   
        a, b = input().split()과 같음   
        print(a, b)   
        10 20   
</code>

* dictionary   
키: 값 형식 // 키-값 쌍(key-value pair)이라 부릅니다(키-값은 1:1 대응)   
중복되는 키는 저장 X   
키에는 리스트와 딕셔너리를 사용할 수 없음
<br>
<code>   
    x = {}      #딕셔너리 생성1   
    y = dict()  #딕셔너리 생성2  
    딕셔너리 = dict(키1=값1, 키2=값2)   
    딕셔너리 = dict(zip([키1, 키2], [값1, 값2]))   
    딕셔너리 = dict([(키1, 값1), (키2, 값2)])   
    딕셔너리 = dict({키1: 값1, 키2: 값2})   
    키에 접근할 대는 [] 사용 안에 키를 지정   
    ex) lux = {'health': 490, 'mana': 334, 'melee': 550, 'armor': 18.72}   
    lux['health']   
</code>   

* set   
{ }(중괄호) 안에 값을 저장하며 각 값은 ,(콤마)로 구분   
중복 허용 X
<br>
<code>
</code>

