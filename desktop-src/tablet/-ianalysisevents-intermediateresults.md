---
description: Происходит при завершении текущего промежуточного этапа анализа.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: 'Событие _IAnalysisEvents:: Интермедиатересултс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9efead00094fdcd773c3ac90b0d626e2036030171bcf3be011323b6da70fb665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857200"
---
# <a name="_ianalysiseventsintermediateresults-event"></a>\_Событие Ианалисисевентс:: Интермедиатересултс

Происходит при завершении текущего промежуточного этапа анализа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканализер* \[ окне\]
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) , выполняющий анализ.

</dd> <dt>

*паналисисстатус* \[ окне\]
</dt> <dd>

Объект [**ианалисисстатус**](ianalysisstatus.md) , представляющий состояние промежуточных результатов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

[**Иинканализер**](iinkanalyzer.md) создает это событие после того, как оно выверят промежуточные результаты для текущего этапа анализа.

Если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md), это событие указывает, что **иинканализер** завершил внесение изменений во внутренние данные для этого этапа анализа.

Заблокируйте структуру данных, когда [**иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисиспроксевентс:: инканализерстатечангинг**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . Внесение изменений в структуру данных на этом этапе анализа может привести к ошибкам при анализе и синхронизации рукописного ввода. Вы можете разблокировать структуру данных, когда **иинканализер** вызывает событие **\_ ианалисисевентс:: интермедиатересултс** или [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .

Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

[**Иинканализер**](iinkanalyzer.md) создает промежуточные результаты только в том случае, если в его режимах анализа установлен флаг **аналисисмодес \_ Интермедиатересултс** (см. [**метод иинканализер:: жетаналисисмодес**](iinkanalyzer-getanalysismodes.md)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ианалисисевентс**](-ianalysisevents.md)
</dt> <dt>

[**аналисисмодес**](analysismodes.md)
</dt> <dt>

[**\_Ианалисисевентс:: Results**](-ianalysisevents-results.md)
</dt> <dt>

[**\_ианалисиспроксевентс**](-ianalysisproxyevents.md)
</dt> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>
