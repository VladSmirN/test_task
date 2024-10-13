### Задание 1
Код с решением - [Tank_filling_assessment.ipynb](https://github.com/VladSmirN/test_task/blob/master/Tank_filling_assessment.ipynb) .

Для решения задачи была оценена высота стены, которая  не погружена в жидкость. Для этого была выделена стена резервуара  и жидкости на фото при помощи sam2. Выделение жидкости на фото  требовалось для определения нижней точки стены,  не погруженной в воду (граница между стеной  и жидкостью более явная).  Для определения верхней границы стены выделялась сама стена.

### Задание 2

С записи камеры видеонаблюдения детектируются животные, эти детекты сопоставляются с данными тепловизора для оценки температуры животных. Отклонения от нормальной температуры может свидетельствовать о болезни. 

Детекты животных можно подать в классификатор для классификации больного животного (сложно реализуемо, если нет размеченного датасета). Также эти детекты животных  можно анализировать на поиск аномалий, аномалии могут выражаться в неестественном цвете кожи, наличие повреждений итд. 
  
Детекты можно объединить в трек для оценки подвижности животного, если животное долго не двигается, то возможно оно больно.
 
Звук можно классифицировать на наличие громких визгов, или других звуков, которые могут свидетельствовать о травме животного. 	
	
Финальное решение зависит от выделенного времени. Стоит выполнять проект поэтапно, последнии этапы можно отбросить в случае недостатка времени.   В первую очередь стоит реализовать детектирование животных и сопоставление детектов с данными тепловизора. Далее стоит реализовать трекинг для оценки подвижности животных. В конце стоит реализовать классификацию/поиск аномалии по детекту/отрезку записи звука.
