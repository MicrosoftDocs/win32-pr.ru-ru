---
title: ключевое слово UNION (RPC)
description: Для объединения требуются специальные ключевые слова MIDL для поддержки их использования с удаленным вызовом процедур (RPC).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337617"
---
# <a name="union-keyword-rpc"></a>ключевое слово UNION (RPC)

Некоторые функции языка C, такие как объединения, занимают специальные ключевые слова MIDL для поддержки их использования в удаленных вызовах процедур. Объединение в языке C представляет собой переменную, которая содержит объекты различных типов и размеров. Разработчик обычно создает переменную для наблюдения за типами, хранящимися в объединении. Для правильной работы в распределенной среде переменная, указывающая тип объединения или *discriminant*, также должна быть доступна удаленному компьютеру. MIDL предоставляет \[ [**\_ тип параметра**](/windows/desktop/Midl/switch-type) \] и \[ [**параметр \_ —**](/windows/desktop/Midl/switch-is) \] Ключевые слова для задания типа и имени discriminant.

MIDL требует, чтобы discriminant передавался вместе с объединением одним из двух способов:

-   Union и discriminant должны быть указаны в качестве параметров.
-   Объединение и discriminant должны быть упакованы в структуру.

Два фундаментальных типа размеченных объединений предоставляются MIDL: [**неинкапсулированное \_ объединение**](/windows/desktop/Midl/nonencapsulated-unions) и [**инкапсулированное \_ объединение**](/windows/desktop/Midl/encapsulated-unions). Discriminant неинкапсулированного объединения является другим параметром, если объединение является параметром. Это еще одно поле, если объединение является полем структуры. Определение инкапсулированного объединения преобразуется в определение структуры, первым полем которого является discriminant, а второе и Последнее поля — объединение. В следующем примере показано, как указать параметры Union и discriminant в качестве параметров:

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

Объединение в предыдущем примере может содержать одно значение: **Short**, **float** или **char**. Определение типа для объединения включает в себя атрибут **\_ типа параметра** MIDL, указывающий тип discriminant. Здесь \[ тип параметра \_ (Short) \] указывает, что discriminant имеет тип **Short**. Параметр должен быть целочисленным типом.

Если объединение является членом структуры, то discriminant должен быть членом той же структуры. Если Union является параметром, discriminant должен быть другим параметром. Прототип для функции **унионпарампрок** в предыдущем примере показывает discriminant *сутипе* в качестве последнего параметра вызова. (Discriminant может находиться в любом месте вызова.) Тип параметра, указанного в **\[ \_ \] параметре, должен** соответствовать типу, указанному в атрибуте **\[ \_ типа \] переключателя** .

В следующем примере демонстрируется использование одной структуры, которая упаковывает discriminant с объединением:

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

Компилятор Microsoft RPC MIDL позволяет объявлять Union за пределами конструкций [**typedef**](/windows/desktop/Midl/typedef) . Эта функция является расширением для устройства DCE IDL. Дополнительные сведения см. в разделе [**Union**](/windows/desktop/Midl/union).

 

 