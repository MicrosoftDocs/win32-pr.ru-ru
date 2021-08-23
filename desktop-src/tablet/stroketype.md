---
description: Указывает, следует ли анализировать штрих как часть рисунка или как часть записи.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Перечисление Строкетипе (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 4b02a05582d675f04ad4458b1cb21c6d4a1797bacf15baf5d0851804d1a95d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589584"
---
# <a name="stroketype-enumeration"></a>Перечисление Строкетипе

Указывает, следует ли анализировать штрих как часть рисунка или как часть записи.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**Строкетипе не \_ классифицировано**
</dt> <dd>

Штрих может быть либо частью рисунка, либо частью записи.

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Строкетипе \_ запись**
</dt> <dd>

Штрих является частью записи.

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**\_Рисование строкетипе**
</dt> <dd>

Штрих является частью рисунка.

</dd> </dl>

## <a name="examples"></a>Примеры

В следующем примере показана часть обработчика событий Stroke, реализованная аналогичным образом для [примера приемников событий C++](c---event-sinks-sample.md). Добавленный росчерк проверяется, отображается ли верхняя граница ограничивающего прямоугольника под полем `drawingMargin` . Если это так, то объект [**иинканализер**](iinkanalyzer.md) , `m_spInkAnalyzer` , задается для анализа штриха в виде рисованной черты, а не в виде рукописного штриха. `CheckHResult` — Это функция, которая принимает `HRESULT` и получает строку и создает исключение, созданное со строкой, если `HRESULT` не **выполнено**.


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Метод Иинканализер:: Сетстрокетипе**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




