---
description: Происходит перед тем, как Иинканализер удаляет объект Иконтекстноде.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: 'Событие _IAnalysisProxyEvents:: Контекстнодеделетинг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703501"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a>\_Событие Ианалисиспроксевентс:: Контекстнодеделетинг

Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) удаляет объект [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканализер* \[ окне\]
</dt> <dd>

Объект [**иинканализер**](iinkanalyzer.md) , удаляющий объект [**иконтекстноде**](icontextnode.md) .

</dd> <dt>

*пконтекстнодетобеделетед* \[ окне\]
</dt> <dd>

Удаляемый объект [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализа рукописного ввода, который удаляет [**иконтекстноде**](icontextnode.md).

Перед тем как [**иинканализер**](iinkanalyzer.md) удалит [**иконтекстноде**](icontextnode.md), **иинканализер** удаляет все штрихи из контекстного узла и удаляет все ссылки на другие контекстные узлы. Перед удалением узла контекста **иинканализер** может вызвать следующие события.

-   Событие [**\_ ианалисиспроксевентс:: строкерепарентед**](-ianalysisproxyevents-strokereparented.md) при перемещении штриха из [**иконтекстноде**](icontextnode.md).
-   Событие [**\_ ианалисиспроксевентс:: контекстноделинкделетинг**](-ianalysisproxyevents-contextnodelinkdeleting.md) перед удалением [**иконтекстлинк**](icontextlink.md) из [**иконтекстноде**](icontextnode.md).
-   Событие **\_ ианалисиспроксевентс:: контекстнодеделетинг** перед удалением родительского узла контекста, у которого больше нет дочерних узлов.

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

[**\_ианалисиспроксевентс**](-ianalysisproxyevents.md)
</dt> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




