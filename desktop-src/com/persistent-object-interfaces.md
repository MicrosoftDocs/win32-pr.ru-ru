---
title: Интерфейсы постоянных объектов (COM)
description: Постоянный объект реализует один или несколько интерфейсов постоянного объекта.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df8920f1242d077044654d1090adcc0e3f3f05c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987941"
---
# <a name="persistent-object-interfaces"></a>Постоянные интерфейсы объектов

Постоянный объект реализует один или несколько *интерфейсов постоянного объекта*. Клиенты используют интерфейсы постоянных объектов, чтобы сообщить этим объектам, когда и где сохранять их состояние. Все объекты постоянного объекта являются производными от [**IPersist**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist), поэтому любой объект, реализующий любой интерфейс постоянного объекта, также реализует **IPersist**.

В настоящее время определены следующие интерфейсы постоянных объектов:

-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [иперсистмемори](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Разработчики выбирают, какие постоянные объекты будут поддерживаться объектом в зависимости от того, как объект будет использоваться. Если не поддерживаются какие-либо постоянные интерфейсы объектов, разработчик фактически говорит: «состояние этого объекта не может храниться постоянно». Благодаря поддержке одного или нескольких постоянных объектных интерфейсов средство реализации фактически говорит: «состояние этого объекта может храниться в одном или нескольких средних хранилищах данных».

Например, в следующей таблице перечислены несколько типов объектов, которые позволяют поддерживать различные интерфейсы постоянных объектов.



| Категория                            | Обычно поддерживаются интерфейсы постоянных объектов                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Моникеров<br/>                 | [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| Внедряемые объекты OLE<br/>   | [**Иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| Элементы управления ActiveX<br/>         | [**Иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), Иперсистмемори, IPersistPropertyBag, [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| Объекты документов ActiveX<br/> | [**Иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Разработчики клиентов могут также выбирать, какие объекты постоянных объектов может использовать клиент. Интерфейсы, используемые клиентом, обычно определяются в том месте, где клиент может хранить свои данные. Клиент, который может хранить свои данные только в неструктурированном файле, вероятно, будет использовать только [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))и IPersistPropertyBag. (**Иперсистстреаминит** может заменить [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) в большинстве приложений, так как в нем содержится это определение и добавлен метод инициализации.) Клиент, который может сохранить свои данные в структурированном файле хранилища, также будет использовать [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инициализация постоянных объектов](initializing-persistent-objects.md)
</dt> </dl>

 

