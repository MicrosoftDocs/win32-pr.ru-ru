---
description: Извлекает 10 альтернативных вариантов анализа для всех рукописных данных, связанных с Иинканализер.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: Метод Иинканализер::-alternate (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: deb430c7573abc4e0964e83d508b98813e29e90d0185c6a9ff9a49bc529d1f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043731"
---
# <a name="iinkanalyzergetalternates-method"></a>Метод Иинканализер:: Alternate

Извлекает 10 альтернативных вариантов анализа для всех рукописных данных, связанных с [**иинканализер**](iinkanalyzer.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппалтернатес* \[ заполняет\]
</dt> <dd>

Указатель на 10 лучших объектов [**ианалисисалтернате**](ianalysisalternate.md) для всех рукописных данных, связанных с [**иинканализер**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

> [!Caution]  
> Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппалтернатес* , когда больше не нужно использовать объект.

 

Верхний альтернативный вариант возвращается в качестве первого альтернативы коллекции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**ианалисисалтернате**](ianalysisalternate.md)
</dt> <dt>

[**ианалисисалтернатес**](ianalysisalternates.md)
</dt> <dt>

[**Метод Иинканализер:: Жеталтернатесфорконтекстнодес**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Метод Иинканализер:: Жеталтернатесфорстрокес**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Модифитопалтернате**](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[**Метод Иинканализер:: Модифитопалтернатевисконфирматион**](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

