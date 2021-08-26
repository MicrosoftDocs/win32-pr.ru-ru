---
description: Маршрутизатор нескольких поставщиков (MPR) вызывает функции уведомления о соединении при подключении или отключении сетевого ресурса. Чтобы получать такие уведомления, можно реализовать эти функции в библиотеке DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: API уведомления о соединении
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afaa2e08e6a88f101e8914d9d98a40d6024bdf942ed4bcb0fd1924bc5800213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883314"
---
# <a name="connection-notification-api"></a>API уведомления о соединении

[*Маршрутизатор нескольких поставщиков*](/windows/desktop/SecGloss/m-gly) (MPR) вызывает функции уведомления о соединении при подключении или отключении сетевого ресурса. Чтобы получать такие уведомления, можно реализовать эти функции в библиотеке DLL.

Многопротокольный маршрутизатор вызывает функцию [**аддконнектнотифи**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) до и после выполнения каждой операции добавления подключения ([**внетаддконнектион**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)или [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). Эта функция не вызывается, когда многопротокольный маршрутизатор автоматически восстанавливает сетевые подключения.

Многопротокольный маршрутизатор вызывает функцию [**канцелконнектнотифи**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) до и после выполнения каждой операции отмены соединения ([**внетканцелконнектион**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) или [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).

дополнительные сведения о функциях внет см. в разделе [Windows networking](/windows/desktop/WNet/windows-networking-wnet-).

Дополнительные сведения о создании и регистрации приложения, которое получает уведомления о сетевом подключении, см. в разделе [Получение уведомлений о подключениях](receiving-connection-notifications.md) и [Регистрация для получения уведомлений о подключениях](registering-to-receive-connection-notifications.md).

 

 
