---
description: Задает функцию обратного вызова, используемую при распознавании строк.
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: Функция Сетлинерекокаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265065"
---
# <a name="setlinerecocallback-function"></a>Функция Сетлинерекокаллбакк

Задает функцию обратного вызова, используемую при распознавании строк.

Эта вспомогательная функция не предназначена для использования в коде приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдивидер* \[ окне\]
</dt> <dd>

Маркер объекта [**инкдивидер**](inkdivider-class.md) .

</dd> <dt>

*PFN* 
</dt> <dd>

Указатель на функцию, которая вызывается при распознавании в переданном [**инкдивидер**](inkdivider-class.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция может возвращать одно из этих значений.



| Код возврата                                                                                  | Описание                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Функция выполнена успешно.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *пдивидер* .<br/> |



 

## <a name="remarks"></a>Комментарии

Ниже приведен синтаксис функции обратного вызова.

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                         |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Библиотека<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




