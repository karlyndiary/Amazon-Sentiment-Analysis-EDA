**Sentiment First**
Returns the earliest sentiment for each product based on multiple sentiments.
```
{ FIXED [Product Title]: MIN([Sentiment]) }
```

**Review First**
Returns the earliest review star rating for each product based on multiple review star ratings.
```
{ FIXED [Product Title]: MIN([Review Star Rating]) }
```

**Sentiment Score**
Converts review sentiments into numerical values to quantify overall sentiment for each product. Positive = 1, Neutral = 0, Negative = -1.
```
IF [Sentiment] = 'Positive' THEN 1
ELSEIF [Sentiment] = 'Neutral' THEN 0
ELSEIF [Sentiment] = 'Negative' THEN -1
END
```
