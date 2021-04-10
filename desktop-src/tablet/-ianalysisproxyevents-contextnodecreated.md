---
description: Происходит после того, как Иинканализер создает объект Иконтекстноде.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: 'Событие _IAnalysisProxyEvents:: Контекстнодекреатед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104000001"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_Событие Ианалисиспроксевентс:: Контекстнодекреатед

Происходит после того, как [**иинканализер**](iinkanalyzer.md) создает объект [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканализер* \[ окне\]
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) , создающий объект [**иконтекстноде**](icontextnode.md) .

</dd> <dt>

*пконтекстнодекреатед* \[ окне\]
</dt> <dd>

Новый объект [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализа рукописного ввода, создающий [**иконтекстноде**](icontextnode.md).

Когда [**иинканализер**](iinkanalyzer.md) создает [**Иконтекстноде**](icontextnode.md), новый **иконтекстноде** не содержит штрихов, не содержит ссылок на другие объекты **иконтекстноде** и может иметь не все заданные свойства. Кроме того, новый **иконтекстноде** добавляется в конец коллекции подузлов его родительского узла (см. раздел [**Иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md) and [**иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)). После этого события **иинканализер** может вызвать следующие события.

-   Событие [**\_ ианалисиспроксевентс:: строкерепарентед**](-ianalysisproxyevents-strokereparented.md) при перемещении штриха из одного контекстного узла в другой.
-   Событие [**\_ ианалисиспроксевентс:: контекстноделинкаддинг**](-ianalysisproxyevents-contextnodelinkadding.md) при добавлении [**иконтекстлинк**](icontextlink.md) в [**иконтекстноде**](icontextnode.md).
-   Событие [**\_ ианалисиспроксевентс:: контекстнодемовингтопоситион**](-ianalysisproxyevents-contextnodemovingtoposition.md) при изменении порядка [**иконтекстноде**](icontextnode.md) в коллекции подузлов его родительского узла.
-   [**Иинканализер**](iinkanalyzer.md) вызывает событие [**\_ ианалисиспроксевентс:: контекстнодепропертиесупдатед**](-ianalysisproxyevents-contextnodepropertiesupdated.md) после того, как оно разрешит состояние [**иконтекстноде**](icontextnode.md) для этого этапа анализа.

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

 

 




