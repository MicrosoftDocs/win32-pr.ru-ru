---
title: Сведения о проверке подлинности пользователя
description: Служба диспетчера подключений удаленного доступа на клиентском компьютере отправляет имя пользователя и пароль на сервер удаленного доступа на удаленном компьютере.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890717"
---
# <a name="user-authentication-information"></a><span data-ttu-id="53a85-103">Сведения о проверке подлинности пользователя</span><span class="sxs-lookup"><span data-stu-id="53a85-103">User Authentication Information</span></span>

<span data-ttu-id="53a85-104">Служба диспетчера подключений удаленного доступа на клиентском компьютере отправляет имя пользователя и пароль на сервер удаленного доступа на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="53a85-104">The Remote Access Connection Manager service on the client computer sends a user name and password to the RAS server on the remote computer.</span></span> <span data-ttu-id="53a85-105">Прежде чем установить соединение, удаленный сервер использует эти сведения для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="53a85-105">Before it establishes a connection, the remote server uses this information to authenticate the user.</span></span> <span data-ttu-id="53a85-106">По умолчанию диспетчер подключений удаленного доступа отправляет имя пользователя и пароль пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="53a85-106">By default, the Remote Access Connection Manager sends the user name and password of the currently logged-on user.</span></span> <span data-ttu-id="53a85-107">Клиент RAS может использовать структуру [**расдиалпарамс**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) , указанную в вызове [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , чтобы указать другое имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="53a85-107">The RAS client can use the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure specified in the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call to specify a different user name and password.</span></span>

<span data-ttu-id="53a85-108">Если удаленный сервер не может проверить подлинность пользователя с указанными сведениями, он может разрешить операции подключения войти в [приостановленное состояние](paused-states.md) , чтобы разрешить клиенту RAS получать от пользователя различные данные проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="53a85-108">If the remote server cannot authenticate the user with the specified information, it can allow the connection operation to enter a [paused state](paused-states.md) to enable the RAS client to collect different authentication data from the user.</span></span>

 

 