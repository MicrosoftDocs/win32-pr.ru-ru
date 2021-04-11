---
description: Маршрутизатор нескольких поставщиков (MPR) вызывает функции уведомления о соединении при подключении или отключении сетевого ресурса. Чтобы получать такие уведомления, можно реализовать эти функции в библиотеке DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: API уведомления о соединении
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352d5cb09923a666e3fe1474e9fd2ebe033f05be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155903"
---
# <a name="connection-notification-api"></a>API уведомления о соединении

[*Маршрутизатор нескольких поставщиков*](/windows/desktop/SecGloss/m-gly) (MPR) вызывает функции уведомления о соединении при подключении или отключении сетевого ресурса. Чтобы получать такие уведомления, можно реализовать эти функции в библиотеке DLL.

Многопротокольный маршрутизатор вызывает функцию [**аддконнектнотифи**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) до и после выполнения каждой операции добавления подключения ([**внетаддконнектион**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)или [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). Эта функция не вызывается, когда многопротокольный маршрутизатор автоматически восстанавливает сетевые подключения.

Многопротокольный маршрутизатор вызывает функцию [**канцелконнектнотифи**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) до и после выполнения каждой операции отмены соединения ([**внетканцелконнектион**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) или [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).

Дополнительные сведения о функциях Внет см. в разделе [Сетевые подключения Windows](/windows/desktop/WNet/windows-networking-wnet-).

Дополнительные сведения о создании и регистрации приложения, которое получает уведомления о сетевом подключении, см. в разделе [Получение уведомлений о подключениях](receiving-connection-notifications.md) и [Регистрация для получения уведомлений о подключениях](registering-to-receive-connection-notifications.md).

 

 
