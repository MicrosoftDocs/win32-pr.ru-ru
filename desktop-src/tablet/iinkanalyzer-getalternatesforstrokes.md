---
description: Извлекает варианты анализа для штрихов с указанными идентификаторами Stroke.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'Метод Иинканализер:: Жеталтернатесфорстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145463"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a>Метод Иинканализер:: Жеталтернатесфорстрокес

Извлекает варианты анализа для штрихов с указанными идентификаторами Stroke.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*улстрокеидскаунт* \[ окне\]
</dt> <dd>

Число идентификаторов Stroke в *плстрокес*.

</dd> <dt>

*плстрокес* \[ окне\]
</dt> <dd>

Массив идентификаторов Stroke.

</dd> <dt>

*улмаксимумалтернатес* \[ окне\]
</dt> <dd>

Максимальное число возвращаемых вариантов анализа.

</dd> <dt>

*ппалтернатес* \[ заполняет\]
</dt> <dd>

Объект [**ианалисисалтернатес**](ianalysisalternates.md) , содержащий альтернативные варианты анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппалтернатес* , когда больше не нужно использовать объект.

 

Top [**ианалисисалтернате**](ianalysisalternate.md) возвращается в качестве первой альтернативы коллекции.

Указанные штрихи не должны представлять смежные области документа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**ианалисисалтернате**](ianalysisalternate.md)
</dt> <dt>

[**ианалисисалтернатес**](ianalysisalternates.md)
</dt> <dt>

[**Метод Иинканализер:: Alternate**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Метод Иинканализер:: Жеталтернатесфорконтекстнодес**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Метод Иинканализер:: Модифитопалтернате**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Метод Иинканализер:: Модифитопалтернатевисконфирматион**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

