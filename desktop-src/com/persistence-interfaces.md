---
title: Интерфейсы сохраняемости
description: Интерфейсы сохраняемости
ms.assetid: a93582b3-bdbf-430d-b4a6-c0df7bc35dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4894ccb1cc5d17747739e78918da9a5b48e2cca13a9f36078d752fceeaef011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120424"
---
# <a name="persistence-interfaces"></a>Интерфейсы сохраняемости

Объекты, имеющие постоянное состояние любого типа, должны реализовывать по крайней мере один \* интерфейс IPersist и, что предпочтительнее, несколько интерфейсов, чтобы предоставить контейнеру наиболее гибкий способ сохранения состояния элемента управления.

Если у элемента управления есть устойчивое состояние, он должен как минимум реализовать либо [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) , либо [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) (два являются взаимоисключающими и не должны реализовываться в большинстве случаев). Второй вариант используется, когда элемент управления должен иметь представление о создании нового, а не на перезагрузку из существующего постоянного состояния (в **IPersistStream** нет созданной новой возможности). Существование любого интерфейса указывает, что элемент управления может сохранить и загрузить его постоянное состояние в поток, то есть экземпляр [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Помимо этих двух интерфейсов, основанных на потоках, интерфейсы IPersist, \* перечисленные в следующей таблице, можно дополнительно предоставить для поддержки сохранения в расположениях, отличных от развертываемого [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).

Определен набор категорий компонентов, чтобы охватить поддержку интерфейсов сохраняемости, см. [категории компонентов](component-categories.md).



| Интерфейс                                                              | Использование                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иперсистмемори**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))<br/>           | Объект может сохранять и загружать свое состояние в последовательный массив байтов фиксированной длины (в памяти).<br/>                                                                                                                                                                                                                                                    |
| [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)<br/>                  | Объект может сохранить и загрузить его состояние в экземпляр [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) . Элементы управления, которые необходимо пометить как вставляемые как другие объекты составного документа (для вставки в контейнеры, не поддерживающие управление), должны поддерживать этот интерфейс.<br/>                                                                                               |
| [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)<br/> | Объект может сохранять и загружать свое состояние как отдельные свойства, записываемые в Ипропертибаг, реализуемые контейнером. Он используется для функции Сохранить как текст в некоторых контейнерах.<br/>                                                                                                                                                          |
| [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/>  | Объект может сохранять и загружать свое состояние в расположение с именем моникера. Элемент управления вызывает [**IMoniker:: биндтостораже**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) для получения требуемого интерфейса хранилища, например [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/objidl/nn-objidl-ilockbytes), [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)и т. д.<br/> |



 

Хотя поддержка [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) является необязательной, настоятельно рекомендуется использовать ее в качестве оптимизации для контейнеров с функциями "Сохранить как текст", например Visual Basic.

За исключением [**IPersistStream:: жетсиземакс**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax), [**Иперсистстреаминит:: жетсиземакс**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-getsizemax)и [**иперсистмемори:: жетсиземакс**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768208(v=vs.85)), все методы каждого интерфейса должны быть полностью реализованы.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Элементы управления](controls.md)
</dt> </dl>

 

