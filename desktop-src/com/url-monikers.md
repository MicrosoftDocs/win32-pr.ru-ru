---
title: Моникеры URL-адресов
description: Архитектура моникера OLE предоставляет удобную модель программирования для работы с URL-адресами.
ms.assetid: 8e0e2bad-9275-4b96-a96b-35d9c933ae31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2a63f63d14dfe51c0b8c5c3727637e12a51356
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/03/2021
ms.locfileid: "104273163"
---
# <a name="url-monikers"></a>Моникеры URL-адресов

Архитектура моникера OLE предоставляет удобную модель программирования для работы с URL-адресами. Архитектура моникера поддерживает расширяемый и полный анализ имени с помощью функции [**мкпарседисплайнаме**](/windows/desktop/api/Objbase/nf-objbase-mkparsedisplayname) и интерфейсов [**ипарседисплайнаме**](/windows/desktop/api/OleIdl/nn-oleidl-iparsedisplayname) и [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , а также печатаемые имена с помощью метода [**IMoniker::-DisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) . Интерфейс **IMoniker** — это способ фактически использовать URL-адреса, а создание компонентов, которые помещаются в архитектуре моникера, — это способ фактически расширить пространства имен URL-адресов на практике.

Предоставляемый системой класс моникера, моникер URL-адреса, предоставляет платформу для создания и использования определенных URL-адресов. Так как URL-адреса часто видят ресурсы в сетях с высокой задержкой, моникер URL-адреса поддерживает асинхронную и синхронную привязку. Моникер URL-адреса в настоящее время не поддерживает [асинхронное хранилище](/windows/desktop/Stg/asynchronous-storage).

На следующей диаграмме показаны компоненты, участвующие в использовании моникеров URL-адресов. Все эти компоненты должны быть знакомы. (См. раздел [асинхронные моникеры](asynchronous-monikers.md).)

![Схема, на которой показаны компоненты, участвующие в использовании моникеров U R L.](images/bb10975a-9cb5-418e-872e-1e1add0b58ed.png)

Как и все клиенты моникера, пользователь с моникерами URL обычно создает и хранит ссылку на моникер, а также контекст привязки, используемый во время привязки ([**IMoniker:: биндтостораже**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) или [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)). Для поддержки асинхронной привязки клиент может реализовать объект обратного вызова состояния привязки, который реализует интерфейс [**метода интерфейса IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) , и зарегистрировать его в контексте привязки с помощью функции [**регистербиндстатускаллбакк**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) . Этот объект будет принимать интерфейс [**ибиндинг**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) транспорта во время вызовов [**метода интерфейса IBindStatusCallback:: онстартбиндинг**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)).

Моникер URL-адреса определяет протокол, используемый путем синтаксического анализа префикса URL-адреса, а затем извлекает интерфейс [**ибиндинг**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) из транспортного уровня. Клиент использует **ибиндинг** для поддержки приостановки, отмены и приоритета операции привязки. Объект обратного вызова также получает уведомление о ходе выполнения через [**метода интерфейса IBindStatusCallback:: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), уведомление о доступности данных через [**метода интерфейса IBindStatusCallback:: ондатааваилабле**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))и различные другие уведомления транспортного уровня о состоянии привязки. Моникер URL-адреса или определенные транспортные уровни могут также запросить расширенные сведения от клиента через **метода интерфейса IBindStatusCallback:: QueryInterface**, позволяя клиенту предоставлять сведения, относящиеся к протоколу, которые влияют на операцию привязки.

Дополнительные сведения см. в следующих разделах:

-   [Синхронизация обратного вызова](callback-synchronization.md)
-   [Согласование типа носителя](media-type-negotiation.md)
-   [Функции моникера URL-адреса](url-moniker-api-functions.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Асинхронные моникеры](asynchronous-monikers.md)
</dt> <dt>

[О моникерах URL-адресов](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775149(v=vs.85))
</dt> </dl>

 

 