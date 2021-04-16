---
description: Дескрипторы предоставляют эффективные средства для ссылок на методы, передачи, аннотации и параметры с помощью ID3DXEffectCompiler или ID3DXEffect.
ms.assetid: 2494ecf9-88a7-43dc-a75b-ed743b11993a
title: Дескрипторы (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e0dbbcbbc38685cae7c89b334bfb5458bc8386
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537223"
---
# <a name="handles-direct3d-9"></a>Дескрипторы (Direct3D 9)

Дескрипторы предоставляют эффективные средства для ссылок на методы, передачи, аннотации и параметры с помощью [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) или [**ID3DXEffect**](id3dxeffect.md). Они создаются динамически при вызове функций формы получить \[ \| метод функции аннотации аргумента \| \| \| Pass \] \[ бинаме \| бисемантик \| \] .

При выполнении программы многократное создание маркера для одного и того же объекта будет возвращать один и тот же результат каждый раз. Но при многократном запуске программы не полагайтесь на этот обработчик. Также имейте в виду, что дескрипторы, созданные разными экземплярами [**ID3DXEffect**](id3dxeffect.md) и [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) , будут отличаться.

При просмотре файлов заголовков можно заметить, что дескрипторы (D3DXHANDLEs) являются техническими указателями строк.

Дескрипторы, которые передаются в функции, такие как параметр \[ бинаме \| element \| Бисемантик \] или \[ бинаме Annotation, \] могут быть представлены в трех формах следующим образом:

1.  Дескрипторы, которые были возвращены функциями, такими как параметр \[ бинаме \| элемента \| бисемантик \] .
2.  Строки, такие как Мивариабленаме, Митечникуенаме или MyArray \[ 0 \] .
3.  Handle = **null**. Существует четыре варианта.
    -   Если это возвращаемое значение метода, методу не удалось найти этот маркер.
    -   Если в  качестве первого параметра для параметра бинаме элемента бисемантик передается маркер \[ null \| \| \] , функция возвращает параметр верхнего уровня. И наоборот, если маркер не **равен null**, функция возвращает член структуры или элемент, идентифицируемый этим маркером.
    -   Если в качестве первого аргумента Валидатетечникуе или второго аргумента Испараметерусед передается маркер **null** , то проверяется текущий метод.
    -   Если в качестве первого аргумента Финднекствалидтечникуе передается **нулевой** маркер, Поиск допустимого метода начинается с первого метода в результате.

Совет по повышению производительности в начале приложения, выполните этап инициализации для создания дескрипторов из строк. С этого момента используйте только дескрипторы. Передача строк вместо созданных дескрипторов выполняется медленнее.

## <a name="examples"></a>Примеры

Ниже приведено несколько примеров, использующих \[ \| метод функции "получить аннотацию параметра" \| \| \| Pass \] \[ бинаме \| бисемантик \| элементов \] для создания дескрипторов.


```
// Gets handle of second top-level parameter handle in the effect file
h1 = GetParameter(NULL, 1);    

// Gets handle of the third struct member of MyStruct
h2 = GetParameter("MyStruct", 2); 

// Gets handle of the third array element handle of MyArray
h3 = GetParameterElement("MyArray", 2); 

// Gets handle of first member of h1 (that is, the second top-level param)
h4 = GetParameter(h1, 0);    

// Gets handle of MyStruct.Data
h5 = GetParameterByName("MyStruct", "Data");    
// or 
h6 = GetParameterByName(NULL, "MyStruct.Data");    

// Gets handle of MyStruct.Data.SubData
h7 = GetParameterByName("MyStruct.Data", "SubData"); 
// or 
h8 = GetParameterByName(NULL, "MyStruct.Data.SubData");

// Gets handle of fifth annotation of h1 (that is, second top-level param)
h9 = GetAnnotation(h1, 4);    

// Gets handle of MyStruct's annotation, called Author
h10 = GetAnnotationByName("MyStruct", "Author");  
// or
h11 = GetParameterByName(NULL, "MyStruct@Author"); 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Формат эффектов](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



