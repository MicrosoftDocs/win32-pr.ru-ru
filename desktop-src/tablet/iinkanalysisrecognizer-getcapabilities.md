---
description: Получает возможности распознавателя.
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'Метод Иинканалисисрекогнизер:: Capabilities (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145493"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a>Метод Иинканалисисрекогнизер:: Capabilities

Получает возможности распознавателя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкапабилитиес* \[ заполняет\]
</dt> <dd>

Побитовое сочетание значений [**рекогнизеркапабилитиес**](recognizercapabilities.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Это значение является константой для каждого [ **иинканалисисрекогнизер**](iinkanalysisrecognizer.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканалисисрекогнизер**](iinkanalysisrecognizer.md)
</dt> <dt>

[**рекогнизеркапабилитиес**](recognizercapabilities.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




