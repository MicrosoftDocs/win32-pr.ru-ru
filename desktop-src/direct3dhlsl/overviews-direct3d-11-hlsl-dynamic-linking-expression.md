---
title: Ограничения использования интерфейса
description: Текущее оборудование GPU не поддерживает различные сведения о слотах во время выполнения шейдера. Как следствие, ссылки на интерфейс нельзя изменять в условных выражениях, таких как оператор if или switch.
ms.assetid: 95a505d8-3ec4-49b7-bb2b-f29a655e4225
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae44bbdb93ab2b3ffa0d09385c56b463192cc68c17e0454f9edd3326f722d29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672564"
---
# <a name="interface-usage-restrictions"></a>Ограничения использования интерфейса

Текущее оборудование GPU не поддерживает различные сведения о слотах во время выполнения шейдера. Как следствие, ссылки на интерфейс нельзя изменять в условных выражениях, таких как оператор if или switch.

Следующий код шейдера показывает, когда будет происходить это ограничение и возможный альтернативный подход.

С учетом следующих объявлений интерфейса:


```
interface A
{
    float GetRatio();
    bool IsGood();
};

interface B
{
    float GetValue();
};

A arrayA[6];
B arrayB[6];
```



Учитывая следующие объявления классов:


```
class C1 : A
{
    float var;
    float GetRatio() { return 1.0f; }
    bool IsGood() { return true; }
};

class C2 : C1, B
{
    float GetRatio() { return C1::GetRatio() * 0.33f; }
    float GetValue() { return 5.0f; }
    bool IsGood() { return false; }
};

class C3 : B
{
    float var;
    float GetValue() { return -1.0f; }
};

class C4 : A, B
{
    float var;
    float GetRatio() { return var; }
    float GetValue() { return var * 2.0f; }
    bool IsGood() { return var > 0.0f; }
};
```



Невозможно изменить ссылку на интерфейс в условном выражении (оператор if):


```
float main() : wicked
{
    float rev;
    {
        A a = arrayA[0];
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                // This forces the loop to be unrolled, 
                // since the slot information is changing.
                a = arrayA[i]; 
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                // This causes an error since the compiler is
                // unable to determine the interface slot
                rev += arrayB[i].GetValue() + a.GetRatio(); 
            }
        }
    }
    return rev;
}
```



С помощью одного и того же объявления интерфейса и класса можно использовать индекс, чтобы предоставить те же функциональные возможности и избежать недоступности принудительного цикла.


```
float main() : wicked
{
    float rev;
    {
        uint index = 0;
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                index = i;
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                rev += arrayB[i].GetValue() + arrayA[index].GetRatio();
            }
        }
    }
    return rev;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Динамическая компоновка](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




