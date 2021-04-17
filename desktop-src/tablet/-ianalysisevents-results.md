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
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693903"
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

## <a name="remarks"></a>Комментарии

[**Иинканализер**](iinkanalyzer.md) создает это событие после того, как оно выверят результаты для этапа окончательного анализа.

Если приложение вызывает [**метод иинканализер:: баккграунданализе**](iinkanalyzer-backgroundanalyze.md), это событие сигнализирует о готовности результатов анализа.

Если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md), это событие указывает, что **иинканализер** завершил внесение изменений во внутренние данные для этого этапа анализа.

Заблокируйте структуру данных, когда [**иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисиспроксевентс:: инканализерстатечангинг**](-ianalysisproxyevents-inkanalyzerstatechanging.md) . Внесение изменений в структуру данных на этом этапе анализа может привести к ошибкам при анализе и синхронизации рукописного ввода. Разблокируйте структуру данных, когда **иинканализер** вызывает событие [**\_ ианалисисевентс:: интермедиатересултс**](-ianalysisevents-intermediateresults.md) или **\_ ианалисисевентс:: Results** .

Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

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

 

 




