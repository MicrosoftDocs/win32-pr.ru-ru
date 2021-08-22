---
title: Асинхронная и синхронная привязка
description: Асинхронная и синхронная привязка
ms.assetid: 9852df19-5ae4-4425-9ce0-cac160d68456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb498d083260db087e9f32cd3f24b67f03f9a788c0add2592dde36fe7a7905e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048862"
---
# <a name="asynchronous-and-synchronous-binding"></a>Асинхронная и синхронная привязка

Клиент может проверить, является ли моникер асинхронным, вызвав функцию [**исасинкмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775110(v=vs.85)) . Если клиент возвращает \_ асинхронный флаг биндф, вместо того чтобы возвращать указатель на объект или указатель хранилища из последующих вызовов [**IMoniker:: Биндтостораже**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) или [**IMoniker:: биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject), моникер ВОЗВРАЩАЕТ для указателя на \_ объект MK \_ , а не **значение NULL** вместо указателя на хранилище. В ответ клиент должен подождать получения запрошенного объекта или хранилища во время реализации [**метода интерфейса IBindStatusCallback:: ондатааваилабле**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) и [**метода интерфейса IBindStatusCallback:: онобжектаваилабле**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775063(v=vs.85)).

Объект обратного вызова также получает уведомление о ходе выполнения через [**метода интерфейса IBindStatusCallback:: OnProgress**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775064(v=vs.85)), уведомление о доступности данных через [**ондатааваилабле**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))и различные другие уведомления от моникера о состоянии операции привязки.

Если клиент не возвращает \_ асинхронный флаг биндф из вызова моникера [**метода интерфейса IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)), операция привязки будет выполняться синхронно, а требуемый объект или хранилище будут возвращены при последующих вызовах [**биндтубжект**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) или [**биндтостораже**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage). Аналогичным образом, если клиент хочет выполнить синхронную операцию и не хочет получать уведомления о ходе выполнения или обратные вызовы, он может запросить асинхронное моникер, чтобы вести себя синхронно, не реализовав [**метода интерфейса IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)). В таких случаях асинхронное моникер будет вести себя как стандартное синхронное моникер.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Асинхронные моникеры](asynchronous-monikers.md)
</dt> </dl>

 

 