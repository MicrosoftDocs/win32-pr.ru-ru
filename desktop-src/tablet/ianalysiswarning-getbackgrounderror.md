---
description: Возвращает код ошибки для фоновой операции анализа рукописного ввода, если произошла ошибка.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'Метод Ианалисисварнинг:: Жетбаккграундеррор (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263156"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a>Метод Ианалисисварнинг:: Жетбаккграундеррор

Возвращает код ошибки для фоновой операции анализа рукописного ввода, если произошла ошибка.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Если ошибка возникает в фоновой операции анализа, [**иинканализер**](iinkanalyzer.md) не может вернуть код ошибки, так как он происходит в другом потоке. Вместо этого обработчик событий [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) получает [**ианалисисстатус**](ianalysisstatus.md) , содержащий [**ианалисисварнинг**](ianalysiswarning.md) с [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) **аналисисварнингкоде \_** BackgroundException. Этот **ианалисисварнинг** содержит код ошибки для фоновой операции анализа. В общем случае обработчик событий **\_ ианалисисевентс:: Results** вернет этот код ошибки, чтобы его можно было обработать в любом расположении приложения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ианалисисварнинг**](ianalysiswarning.md)
</dt> <dt>

[**ианалисисстатус**](ianalysisstatus.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_Ианалисисевентс:: Results**](-ianalysisevents-results.md)
</dt> <dt>

[**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

