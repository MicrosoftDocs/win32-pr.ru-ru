---
title: Интерфейсы составных документов
description: Интерфейсы составных документов
ms.assetid: 3192ee58-55fd-43cb-b7d5-7270e91b8131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e146bf26ef8d0c5c2fc189255389982a7e737a0556343cb095217c55ff8d712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410514"
---
# <a name="compound-document-interfaces"></a>Интерфейсы составных документов

В следующих таблицах перечислены интерфейсы, реализованные в контейнерах OLE, серверах OLE и объектах составных документов. Необходимые интерфейсы должны быть реализованы в компонентах, для которых они перечислены. Все остальные функции являются необязательными. Однако если вы хотите включить в приложение определенную функцию, необходимо реализовать интерфейсы, показанные для этой функции, в таблице ниже. Все остальные интерфейсы необходимы только в том случае, если включен определенный компонент.

В следующей таблице перечислены необходимые и необязательные поведения для контейнеров OLE, а также интерфейсы, которые необходимо реализовать для каждого из них.



| Поведение                               | Интерфейсы                                                                                                                                                              |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Требуемые поведения<br/>          | [**иолеклиентсите**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/> [**иадвисесинк**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                                                       |
| Фильтрация сообщений<br/>           | [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                                                     |
| Компоновка<br/>                     | нет<br/>                                                                                                                                                         |
| Связывание с внедренными объектами<br/> | [**иолеитемконтаинер**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/> [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>             |
| Активация на месте<br/>         | [**иолеинплацесите**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/> [**иолеинплацефраме**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/> [**иолеинплацеобжект**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> |
| Перетаскивание<br/>               | [**идропсаурце**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**Интерфейс IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                               |



 

В следующей таблице перечислены необходимые и необязательные поведения для серверов OLE и их объектов составного документа, а также интерфейсы, которые необходимо реализовать для каждого из них. В таблице различаются серверы OLE и их объекты, чтобы уточнить, какой компонент реализует интерфейс. В таблице также приводятся различные требования к объектам, предоставляемым вне процесса и на серверах обработки.



| Компонент                        | Сервер OLE                                                                                                                                | Объект (вне процесса)                                                                                                                         | Объект (внутрипроцессный)                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Требуемые поведения             | [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)<br/>                                                                                         | [**иолеобжект**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> | [**иолеобжект**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/> [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)<br/> [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2)<br/> |
| Фильтрация сообщений<br/>   | [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter)<br/>                                                                                       |                                                                                                                                                 |                                                                                                                                                                                                                                             |
| Компоновка<br/>             | [**иолеитемконтаинер**](/windows/desktop/api/OleIdl/nn-oleidl-ioleitemcontainer)<br/> [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                 |                                                                                                                                                 | [**иолелинк**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)<br/> [**иекстерналконнектион**](/windows/win32/api/objidlbase/nn-objidlbase-iexternalconnection)<br/>                                                                                                                                       |
| Активация на месте<br/> |                                                                                                                                           | [**иолеинплацеобжект**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**Метода IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                 | [**иолеинплацеобжект**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceobject)<br/> [**Метода IOleInPlaceActiveObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceactiveobject)<br/>                                                                                                             |
| Перетаскивание<br/>       | [**идропсаурце**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> [**Интерфейс IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/> |                                                                                                                                                 |                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Составные документы](compound-documents.md)
</dt> </dl>

 

