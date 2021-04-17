---
description: Происходит после того, как Иинканализер обновляет одно или несколько свойств объекта Иконтекстноде.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: 'Событие _IAnalysisProxyEvents:: Контекстнодепропертиесупдатед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703493"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a>\_Событие Ианалисиспроксевентс:: Контекстнодепропертиесупдатед

Происходит после того, как [**иинканализер**](iinkanalyzer.md) обновляет одно или несколько свойств объекта [**иконтекстноде**](icontextnode.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканализер* \[ окне\]
</dt> <dd>

Объект [**иинканализер**](iinkanalyzer.md) , обновляющий свойства.

</dd> <dt>

*пконтекстнодеупдатед* \[ окне\]
</dt> <dd>

Объект [**иконтекстноде**](icontextnode.md) , свойства которого обновляются.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализатора рукописного ввода, который изменяет свойства [**иконтекстноде**](icontextnode.md) (см. [**Иконтекстноде:: жетпропертидата**](icontextnode-getpropertydata.md)).

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

[Свойства узла контекста](context-node-properties.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




