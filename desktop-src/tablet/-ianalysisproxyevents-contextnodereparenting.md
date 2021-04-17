---
description: Происходит перед тем, как Иинканализер перемещает объект Иконтекстноде, изменяя его родительский узел.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: 'Событие _IAnalysisProxyEvents:: Контекстнодерепарентинг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703511"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a>\_Событие Ианалисиспроксевентс:: Контекстнодерепарентинг

Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) перемещает объект [**иконтекстноде**](icontextnode.md) , изменяя его родительский узел.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинканализер* \[ окне\]
</dt> <dd>

Объект [**иинканализер**](iinkanalyzer.md) , перемещающий объект [**иконтекстноде**](icontextnode.md) .

</dd> <dt>

*пневпарентконтекстноде* \[ окне\]
</dt> <dd>

Новый родительский объект [**иконтекстноде**](icontextnode.md) .

</dd> <dt>

*пконтекстнодетоберепарентед* \[ окне\]
</dt> <dd>

Перемещаемый объект [**иконтекстноде**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод, который перемещает [**иконтекстноде**](icontextnode.md) из одной коллекции подузлов в другую (см. [**Иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md) и [**иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)).

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

[**Иконтекстноде:: Жетпарентноде**](icontextnode-getparentnode.md)
</dt> <dt>

[**Иконтекстноде:: Жетсубнодес**](icontextnode-getsubnodes.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




