---
description: Происходит после завершения заключительного этапа анализа.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: 'Событие _IAnalysisEvents:: Results (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 22d9ac16976b1cd61d5d2e403424fc9ed08b8da0cbfcced213decc512a1f1e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047396"
---
# <a name="_ianalysiseventsresults-event"></a>\_Событие Ианалисисевентс:: Results

Происходит после завершения заключительного этапа анализа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканализер* \[ окне\]
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) , создающая результаты анализа.

</dd> <dt>

*паналисисстатус* \[ окне\]
</dt> <dd>

Объект [**ианалисисстатус**](ianalysisstatus.md) , представляющий состояние анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Remarks

[**Иинканализер**](iinkanalyzer.md) создает это событие после того, как оно выверят результаты для этапа окончательного анализа.

Если приложение вызывает [**метод иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md), это событие сигнализирует о готовности результатов анализа.

Если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md), это событие указывает, что **иинканализер** завершил внесение изменений во внутренние данные для этого этапа анализа.

Заблокируйте структуру данных, когда [**иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисиспроксевентс:: инканализерстатечангинг**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . Внесение изменений в структуру данных на этом этапе анализа может привести к ошибкам при анализе и синхронизации рукописного ввода. Разблокируйте структуру данных, когда **иинканализер** вызывает событие [**\_ ианалисисевентс:: интермедиатересултс**](-ianalysisevents-intermediateresults.md) или **\_ ианалисисевентс:: Results** .

Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ианалисисевентс**](-ianalysisevents.md)
</dt> <dt>

[**\_ианалисиспроксевентс**](-ianalysisproxyevents.md)
</dt> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**ианалисисстатус**](ianalysisstatus.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




