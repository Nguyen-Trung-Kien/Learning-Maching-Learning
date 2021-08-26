# ở phần này mình sẽ thực hành sử dụng naive bayes để phân loại thư rác


CountVectorizer được sử dụng để đếm số lần xuất hiện trong 1 lớp duy nhất

ở bài này sẽ nói về thư viện scikit learn , ở đây nó cho phép chuyển đổi định dạng text thành vector 

*Tại sao là vector? vì maching learning làm việc với số*

# Mình sẽ nói về phần CountVectorizer

mình sẽ lấy ví dụ luôn là ví dụ trong document của sklearn

```
>>> from sklearn.feature_extraction.text import CountVectorizer
>>> corpus = [
...     'This is the first document.',
...     'This document is the second document.',
...     'And this is the third one.',
...     'Is this the first document?',
... ]
>>> vectorizer = CountVectorizer()
>>> X = vectorizer.fit_transform(corpus)
>>> print(vectorizer.get_feature_names())
['and', 'document', 'first', 'is', 'one', 'second', 'the', 'third', 'this']
>>> print(X.toarray())
[[0 1 1 1 0 0 1 0 1]
 [0 2 0 1 0 1 1 0 1]
 [1 0 0 1 1 0 1 1 1]
 [0 1 1 1 0 0 1 0 1]]
>>> vectorizer2 = CountVectorizer(analyzer='word', ngram_range=(2, 2))
>>> X2 = vectorizer2.fit_transform(corpus)
>>> print(vectorizer2.get_feature_names())
['and this', 'document is', 'first document', 'is the', 'is this',
'second document', 'the first', 'the second', 'the third', 'third one',
 'this document', 'this is', 'this the']
 >>> print(X2.toarray())
 [[0 0 1 1 0 0 1 0 0 0 0 1 0]
 [0 1 0 1 0 1 0 1 0 0 1 0 0]
 [1 0 0 1 0 0 0 0 1 1 0 1 0]
 [0 0 1 0 1 0 1 0 0 0 0 0 1]]
```
Như này mình có một mảng các string corpus, mình sẽ transform mảng này sao mỗi string sẽ chuyển đổi thành 1 vector có độ dài d (số từ xuất hiện ít nhất 1 lần trong corpus), giá trị của thành phần thứ i trong vector chính là số lần từ đó xuất hiện trong string.

1. Đầu tiên import thư viện
2. corpus chính là ma trận chữ trong ví dụ
3. đoạn này : vectorizer = CountVectorizer() , nếu bạn từng code c# hay đại loại thì sẽ hiểu cái này
4. X = vectorizer.fit_transform(corpus) , ờ thì load vào ý mn, kiểu kiểu vậy
5. print(vectorizer.get_feature_names()) ở đây như mình đã nói trên là sẽ lấy những từ xuất hiện ít nhất 1 lần , xem nó ra cái gì
6. print(X2.toarray()) nhìn phát biết liền




