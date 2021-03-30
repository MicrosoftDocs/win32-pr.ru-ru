---
description: Возвращает значение, указывающее уровень достоверности, который Иинканализер имеет точность Ианалисисалтернате.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'Метод Ианалисисалтернате:: Жетрекогнитионконфиденце (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810061"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a>Метод Ианалисисалтернате:: Жетрекогнитионконфиденце

Возвращает значение, указывающее уровень достоверности, который [**иинканализер**](iinkanalyzer.md) имеет точность [**ианалисисалтернате**](ianalysisalternate.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пконфиденце* \[ заполняет\]
</dt> <dd>

Указатель на [**перечисление инкрекогнитионконфиденце**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) , которое указывает уровень достоверности, который [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) имеет точность альтернативного распознавания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисалтернате**](ianalysisalternate.md)
</dt> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)
</dt> <dt>

[**рекогнитионконфиденце**](recognitionconfidence.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




