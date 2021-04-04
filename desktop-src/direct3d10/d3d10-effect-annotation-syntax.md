---
description: Заметка — это определяемая пользователем часть данных, объявленная с помощью следующего синтаксиса.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Синтаксис аннотации (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896534"
---
# <a name="annotation-syntax-direct3d-10"></a>Синтаксис аннотации (Direct3D 10)

Заметка — это определяемая пользователем часть данных, объявленная с помощью следующего синтаксиса.



| <*Имя типа данных*   =  ;...; > |
|--------------------------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                                                                   | Описание                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Заданий*<br/> | \[в \] типе данных, который включает любой [скалярный тип HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) , а также [строковый тип](../direct3dhlsl/dx-graphics-hlsl-scalar.md).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*<br/>                 | \[в \] строке ASCII, представляющей имя заметки.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Значений*<br/>             | \[в \] начальном значении заметки.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[в \] дополнительных аннотациях (пар "имя-значение").<br/>                                                                                                                     |



 

## <a name="remarks"></a>Комментарии

В угловые скобки можно добавить несколько аннотаций, каждое из которых отделяется точкой с запятой. Интерфейсы API платформы эффектов распознавать заметки в глобальных переменных. все остальные заметки игнорируются.

## <a name="example"></a>Пример

Вот несколько примеров.


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Синтаксис переменной Effect](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
