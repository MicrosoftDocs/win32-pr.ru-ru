---
title: Объект Geometry-Shader
description: Объект Geometry-Shader обрабатывает все примитивы. Используйте следующий синтаксис, чтобы объявить объект Geometry-Shader.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- максвертекскаунт (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b95f0bb99bd3a225afb7a63824b301b102030a4f132caa7a2a4ff1743eefb58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120148"
---
# <a name="geometry-shader-object"></a>Объект Geometry-Shader

Объект Geometry-Shader обрабатывает все примитивы. Используйте следующий синтаксис, чтобы объявить объект Geometry-Shader.

\[максвертекскаунт (*нумвертс*) \] void *Шадернаме* ( *тип PrimitiveType DataType Name \[ нумелементс \]*, InOut *стреамаутпутобжект* );



 

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[максвертекскаунт (*нумвертс*)\]
</dt> <dd>

\[в \] объявлении для максимального числа создаваемых вершин.

-   \[максвертекскаунт () \] — обязательное ключевое слово; квадратные скобки и круглые скобки являются обязательными символами для правильного синтаксиса.
-   *Нумвертс* — целое число, представляющее количество вершин.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*шадернаме*
</dt> <dd>

\[в \] строке ASCII, содержащей уникальное имя для функции Geometry-Shader.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*Имя типа данных тип PrimitiveType \[ нумелементс \]*
</dt> <dd>

*Тип PrimitiveType* -примитивный тип, который определяет порядок примитивных данных.



| Тип-примитив | Описание                                                   |
|----------------|---------------------------------------------------------------|
| *точки*        | Список точек                                                    |
| *line*         | Линейный список или полоса строк                                       |
| *значок*     | Список треугольников или полоса треугольников                               |
| *линеадж*      | Список линий с соседкой или линейной полосой с соседкой         |
| *трианглеадж*  | Список треугольников с соседкой или треугольной полосой с соседкой |



 

*Тип данных*  -  \[ в \] типе входных данных аргумент может иметь любой [тип данных HLSL](dx-graphics-hlsl-data-types.md).

*Name* — имя аргумента; Это строка ASCII.

*Нумелементс* — размер массива входных данных, который зависит от *тип PrimitiveType* , как показано в следующей таблице.

| Тип-примитив | нумелементс                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *точки*        | \[1\]<br/> Вы действуете только на один момент времени.<br/>                                         |
| *line*         | \[2\]<br/> Для линии требуется две вершины.<br/>                                                    |
| *значок*     | \[3\]<br/> Для треугольника требуется три вершины.<br/>                                              |
| *линеадж*      | \[4\]<br/> У линеадж есть две конечные точки; Поэтому требуется четыре вершины.<br/>                    |
| *трианглеадж*  | \[6\]<br/> Трианглеадж границы еще три треугольника; Поэтому для него требуется шесть вершин.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*стреамаутпутобжект*
</dt> <dd>

Объявление [объекта потока вывода](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет

## <a name="remarks"></a>Remarks

На следующей диаграмме показаны различные типы-примитивы для объекта шейдера Geometry.

![Иллюстрация различных типов-примитивов для объекта шейдера Geometry](images/d3d11-gsinputs1.png)

На следующей диаграмме показаны вызовы шейдера Geometry.

![Иллюстрация вызовов шейдера Geometry](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Примеры

В этом примере из упражнения 1 в [семинаре по модели шейдера Direct3D 10 4,0](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Этот объект поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                        | Поддерживается |
|---------------------------------------------------------------------|-----------|
| [Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров | Да       |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Модель шейдера 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





