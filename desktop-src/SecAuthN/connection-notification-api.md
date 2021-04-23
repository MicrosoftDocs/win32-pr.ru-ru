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
# <a name="connection-notification-api"></a><span data-ttu-id="8969f-104">API уведомления о соединении</span><span class="sxs-lookup"><span data-stu-id="8969f-104">Connection Notification API</span></span>

<span data-ttu-id="8969f-105">[*Маршрутизатор нескольких поставщиков*](/windows/desktop/SecGloss/m-gly) (MPR) вызывает функции уведомления о соединении при подключении или отключении сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="8969f-105">The [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the connection notification functions when it connects or disconnects a network resource.</span></span> <span data-ttu-id="8969f-106">Чтобы получать такие уведомления, можно реализовать эти функции в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="8969f-106">To receive such notifications, you can implement these functions in a DLL.</span></span>

<span data-ttu-id="8969f-107">Многопротокольный маршрутизатор вызывает функцию [**аддконнектнотифи**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) до и после выполнения каждой операции добавления подключения ([**внетаддконнектион**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)или [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span><span class="sxs-lookup"><span data-stu-id="8969f-107">The MPR calls the [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) function before and after attempting each add-connection operation ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a), or [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span></span> <span data-ttu-id="8969f-108">Эта функция не вызывается, когда многопротокольный маршрутизатор автоматически восстанавливает сетевые подключения.</span><span class="sxs-lookup"><span data-stu-id="8969f-108">This function is not called when the MPR is automatically restoring network connections.</span></span>

<span data-ttu-id="8969f-109">Многопротокольный маршрутизатор вызывает функцию [**канцелконнектнотифи**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) до и после выполнения каждой операции отмены соединения ([**внетканцелконнектион**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) или [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span><span class="sxs-lookup"><span data-stu-id="8969f-109">The MPR calls the [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) function before and after attempting each cancel-connection operation ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) or [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span></span>

<span data-ttu-id="8969f-110">Дополнительные сведения о функциях Внет см. в разделе [Сетевые подключения Windows](/windows/desktop/WNet/windows-networking-wnet-).</span><span class="sxs-lookup"><span data-stu-id="8969f-110">For more information about WNet functions, see [Windows Networking](/windows/desktop/WNet/windows-networking-wnet-).</span></span>

<span data-ttu-id="8969f-111">Дополнительные сведения о создании и регистрации приложения, которое получает уведомления о сетевом подключении, см. в разделе [Получение уведомлений о подключениях](receiving-connection-notifications.md) и [Регистрация для получения уведомлений о подключениях](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="8969f-111">For more information about how to create and register an application that receives network connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md) and [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 
