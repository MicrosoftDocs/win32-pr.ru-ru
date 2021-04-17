---
description: Указывает события, связанные с шагами прокси-сервера данных для объекта Иинканализер.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: Интерфейс _IAnalysisProxyEvents (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674567"
---
# <a name="_ianalysisproxyevents-interface"></a>\_Интерфейс Ианалисиспроксевентс

Указывает события, связанные с шагами прокси-сервера данных для объекта [**иинканализер**](iinkanalyzer.md) .

-   [События](/windows)

### <a name="events"></a>События

Интерфейс **\_ ианалисиспроксевентс** содержит следующие события.



| Событие                                                                                      | Описание                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**контекстнодекреатед**](-ianalysisproxyevents-contextnodecreated.md)                     | Происходит после того, как [**иинканализер**](iinkanalyzer.md) создает объект [**иконтекстноде**](icontextnode.md) .<br/>                                                                  |
| [**контекстнодеделетинг**](-ianalysisproxyevents-contextnodedeleting.md)                   | Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) удаляет объект [**иконтекстноде**](icontextnode.md) .<br/>                                                                 |
| [**контекстноделинкаддинг**](-ianalysisproxyevents-contextnodelinkadding.md)               | Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) добавляет объект [**иконтекстлинк**](icontextlink.md) между двумя объектами [**иконтекстноде**](icontextnode.md) .<br/>           |
| [**контекстноделинкделетинг**](-ianalysisproxyevents-contextnodelinkdeleting.md)           | Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) удаляет объект [**иконтекстлинк**](icontextlink.md) между двумя объектами [**иконтекстноде**](icontextnode.md) .<br/>         |
| [**контекстнодемовингтопоситион**](-ianalysisproxyevents-contextnodemovingtoposition.md)   | Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) перемещает объект [**иконтекстноде**](icontextnode.md) в новую точку в коллекции подузлов родительского узла.<br/> |
| [**контекстнодепропертиесупдатед**](-ianalysisproxyevents-contextnodepropertiesupdated.md) | Происходит после того, как [**иинканализер**](iinkanalyzer.md) обновляет одно или несколько свойств объекта [**иконтекстноде**](icontextnode.md) .<br/>                                        |
| [**контекстнодерепарентинг**](-ianalysisproxyevents-contextnodereparenting.md)             | Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) перемещает объект [**иконтекстноде**](icontextnode.md) , изменяя его родительский узел.<br/>                                       |
| [**инканализерстатечангинг**](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) согласовывает результаты анализа, чтобы приложение могла синхронизировать данные с **иинканализер**.<br/>                      |
| [**популатеконтекстноде**](-ianalysisproxyevents-populatecontextnode.md)                   | Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) выполняет анализ внутри региона частично заполненного объекта [**иконтекстноде**](icontextnode.md) .<br/>               |
| [**строкерепарентед**](-ianalysisproxyevents-strokereparented.md)                         | Происходит, когда [**иинканализер**](iinkanalyzer.md) перемещает штрих из одного объекта [**иконтекстноде**](icontextnode.md) в другой.<br/>                                           |



 

## <a name="remarks"></a>Комментарии

Используйте эти события, если приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md). Дополнительные сведения о синхронизации данных приложения с помощью **иинканализер** см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**иконтекстноде**](icontextnode.md)
</dt> <dt>

[**Метод Иинканализер:: Analyze**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Метод Иинканализер:: Баккграунданализе**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[\_ианалисисевентс](-ianalysisevents.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

