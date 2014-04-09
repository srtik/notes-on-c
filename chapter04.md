# Զրույց IV

Հարգելի՛ ընթերցող։

Նախորդ զրույցներում իմ բերած օրինակները շատ պարզ էին․ ծրագիրը սկսվում էր `main` ֆունկցիայից, կանչվում էր այս կամ այն ֆունկցիան, կատարվում էին հաջորդական գործողություններ ու ծրագրի կատարումն ավարտվում էր։ Իսկ ի՛նչ անել, երբ պետք է ծրագրի տրամաբանությունը ղեկավարել ներմուծված կամ ձևավորված տվյալներից կախված։ Օրինակ, ինչպե՞ս սահմանեմ թվի նշանը որոշող `sign` ֆունկցիան։ Այն պետք է արգումենտում ստացած դրականների թվերի համար վերադարձնի՝ `1`, բացասականների համար՝ `-1`, իսկ զրոյի համար՝ `0`։ Պարզ է, որ ֆունկցիայի այդպիսի վարքը մոդելավորելու համար հարկավոր է *ճյուղավորման* հրաման։

C լեզվում ճյուղավորումները կազմակերպվում են `if` հրամանով.

```
if( ⟨condition⟩ ) <then-block> else <else-block>
```

Եթե *ճշմարիտ* է `<condition>` պայմանը, ապա կատարվում են `<then-block>` հրամանները, հակառակ դեպքում կատարվում են `<else-block>` հրամանները։ Եթե պայմանի *կեղծ* լինելու դեպքում ոչինչ անել պետք չէ, ապա `else` ծառայողական բառը և նրան հաջորդող `<else-block>` հրամանները կարելի է չգրել։ Օրինակ, `f` ֆունկցիան կանչվում է միայն այն դեպքում, երբ `argc` փոփոխականը հավասար է մեկի.

```
if( argc == 1 )
  f();
```c

```c
int sign( double num )
{
  int res = 0;
  if( num < 0 )
    res = -1;
  else if( num > 0 )
    res = 1;
  return res;
}
```