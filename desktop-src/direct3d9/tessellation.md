---
description: Тесселяция (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Тесселяция (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806352"
---
# <a name="tessellation-direct3d-9"></a>Тесселяция (Direct3D 9)

## <a name="tessellator-unit"></a>Блок тесселяции

Модуль тесселяции улучшен. Теперь его можно использовать для:

-   Выполните адаптивную тесселяцию всех примитивов более высокого порядка.
-   Поиск значений смещения по вершинам на карте смещения и их передача в шейдер вершин.
-   Поддержка тесселяции исправлений прямоугольника. Это указывается через объявление вершины с помощью D3DDECLMETHOD \_ партиалу или D3DDECLMETHOD \_ партиалв. Если объявление вершины, содержащее эти методы, используется для прорисовки исправления треугольника, [**IDirect3DDevice9::D равтрипатч**](/windows/desktop/api) не удастся. Дополнительные сведения об объявлениях вершин см. в разделе [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

В DirectX 8. x то, что называлось ORDER, было действительно степенью. В Direct3D 9 уровень теперь определяется [**D3DDEGREETYPE**](./d3ddegreetype.md).


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



Изменение типа градуса затронуло две другие структуры.


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



Драйверы должны исправить ошибки компиляции, которые будут вызваны этим изменением при компиляции с новыми заголовками. Функциональность не требуется изменять.

## <a name="adaptive-tessellation"></a>Адаптивная тесселяция

Адаптивную тесселяцию можно применять к примитивам высокого порядка, включая N-исправления, прямоугольники и исправления треугольников. Эта функция включена D3DRS \_ енаблеадаптиветесселлатион и адаптирует исправление на основе значения глубины вершины элемента управления в области глаз.

Координаты z (Zi) элементов управления (VI), которые преобразуются в область видимости (Зиэйе), выполняя точку с 4 векторами, используются в качестве значений глубины. Объект 4D Vector (MDM) задается приложением, использующим четыре состояния отрисовки (D3DRS \_ адаптиветесс \_ X, D3DRS \_ АДАПТИВЕТЕСС \_ Y, D3DRS \_ адаптиветесс \_ Z и D3DRS \_ адаптиветесс \_ W). Этот 4-вектор может быть третьим столбцом объединенного мира и матрицами представления. Его также можно использовать для применения шкалы к Зиэйе.

Функция для расчета уровня тесселяции Ti из Зиэйе предполагается (Макстесселлатионлевел/Зиэйе), что означает, что Макстесселлатионлевел является уровнем тесселяции Z = 1 в пространстве глаз. Макстесселлатионлевел равно значению, заданному параметром [**IDirect3DDevice9:: сетнпатчмоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) для N-патчей и, для обновлений RT-патчей, он равен пнумсегс. Затем уровень тесселяции копируется в значения, определенные двумя дополнительными состояниями отрисовки D3DRS \_ минтесселлатионлевел и D3DRS \_ макстесселлатионлевел, которые определяют минимальный и максимальный уровни тесселяции, на которые будут относиться. Для каждой вершины, расположенной вдоль края исправления, вычисляется среднее значение, чтобы получить уровень тесселяции для этого края. Алгоритм вычисления TI для обновления прямоугольников, исправлений треугольников и N-патчей отличается в зависимости от того, какие вершины управления используются для вычисления уровня тесселяции.

Для исправлений прямоугольника с использованием B-сплайна используются четыре внешних вершины элемента управления. Например, с D3DORDER \_ кубическим порядком: вершины (1, 1) и (1, Width-2) используются с пнумсегс \[ 0 \] , вершинами (1, Width-2) и (высота-2, высота-2) с пнумсегс \[ 1 \] , вершинами (высота-2, Width-2) и (1, Width-2) с пнумсегс \[ 2 \] , а вершины (2, 1) и (1, 1) используются с пнумсегс \[ 3 \] .

Для исправлений треугольника используются вершины углов исправлений. С D3DORDER \_ кубическим порядком: вершины (0) и (9) используются с пнумсегс \[ 0 \] , вершинами (9) и (6) с пнумсегс \[ 1 \] и вершинами (6) и (0) используются с пнумсегс \[ 3 \] .

Для N-патчей используются вершины треугольника.

Для исправлений прямоугольника и треугольника с учетом Безье используются вершины угловой панели.

Управление скоростью тесселяции на вершину. Приложение может дополнительно предоставить одно положительное значение с плавающей запятой на вершину, которое можно использовать для управления частотой тесселяции. Он предоставляется с помощью D3DDECLUSAGE \_ тессфактор, для которого индекс использования должен быть равен 0, а тип входных данных должен быть D3DDECLTYPE \_ FLOAT1. Это умножается на уровень тесселяции на вершину.

### <a name="math"></a>Математический

Уровень тесселяции (TE) для пограничной e, представленный двумя вершинами управления (Ve1, Ve2), вычисляются, как показано ниже:


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



Если D3DRS \_ енаблеадаптиветесселлатион имеет **значение true**, примитивы треугольника (списки треугольников, вентиляторы, полосы) рисуются как N-патчs, [**IDirect3DDevice9:: сетнпатчмоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) имеет значение меньше 1,0.

### <a name="api-changes"></a>Изменения API

Новые состояния рендеринга:


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



И их значения по умолчанию:


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



Новые ограничения оборудования:


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Конвейер вершин](vertex-pipeline.md)
</dt> </dl>

 

 
