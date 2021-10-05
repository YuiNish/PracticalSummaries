| | 予測<br>Positivie | 予測<br>Negative |
| :---: | :---: | :---: |
| 正解<br>Positive | 真陽性<br>TP(True Positive) | 偽陰性<br>FN(False Negative) |
| 正解<br>Negative | 偽陽性<br>FP(False Positive) | 真陰性<br>TN(True Negative) |

* Accuracy : 正解率  
全予測および全正解のうち、正解したものの割合

<img alt="formula" src="https://render.githubusercontent.com/render/math?math=\frac{TP%2BTN}{TP%2BTN%2BFP%2BFN}" />


* Precision : 適合率  
Positiveと予測したもののうち、正解した割合
```matn
\frac{TP}{TP+FP}
```

* Recall : 再現率  
正解がpositiveのもののうち、予測したものもPositiveであったときの割合
```math
\frac{TP}{TP+FN}
```
