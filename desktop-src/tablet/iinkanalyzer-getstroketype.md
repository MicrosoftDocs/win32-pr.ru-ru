---
description: Извлекает тип указанного штриха.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'Метод Иинканализер:: Жетстрокетипе (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 71bf3775be1c21e59cf41a51fa5a6140e86e44ac81a2863892c1f252666e0f3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092144"
---
# <a name="iinkanalyzergetstroketype-method"></a>Метод Иинканализер:: Жетстрокетипе

Извлекает тип указанного штриха.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лстрокеид* \[ окне\]
</dt> <dd>

Идентификатор штриха.

</dd> <dt>

*пстрокетипе* \[ заполняет\]
</dt> <dd>

Классификация указанного штриха.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

Если тип штриха — [**строкетипе**](stroketype.md) значение строкетипе \_ неклассифицировано, [**иинканализер**](iinkanalyzer.md) классифицирует штрих во время анализа рукописного ввода. В противном случае **иинканализер** использует тип, заданный для штриха.

[**Иинканализер**](iinkanalyzer.md) не задает значение типа Stroke как часть анализа рукописного ввода. Чтобы указать или изменить тип обводки, используйте метод [**иинканализер:: сетстрокетипе**](iinkanalyzer-setstroketype.md) или [**метод Иинканализер:: сетстрокестипе**](iinkanalyzer-setstrokestype.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Сетстрокетипе**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[**Метод Иинканализер:: Сетстрокестипе**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




