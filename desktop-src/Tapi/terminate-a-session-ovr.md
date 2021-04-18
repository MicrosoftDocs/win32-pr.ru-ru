---
description: Завершение сеанса может поступать с запросом пользователя, удаленным соединением с другой стороной или по причинам, зависящим от приложения.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Завершение сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684655"
---
# <a name="terminate-a-session"></a><span data-ttu-id="77e99-103">Завершение сеанса</span><span class="sxs-lookup"><span data-stu-id="77e99-103">Terminate a Session</span></span>

<span data-ttu-id="77e99-104">Завершение сеанса может поступать с запросом пользователя, удаленным соединением с другой стороной или по причинам, зависящим от приложения.</span><span class="sxs-lookup"><span data-stu-id="77e99-104">Session termination may originate with a user request, remote disconnection by the other party, or for application-specific reasons.</span></span> <span data-ttu-id="77e99-105">После завершения сеанса [идентификатор сеанса](session-identifier-ovr.md) остается действительным до тех пор, пока он не будет освобожден и не сможет использоваться для сбора данных после подключения.</span><span class="sxs-lookup"><span data-stu-id="77e99-105">When a session is terminated, the [session identifier](session-identifier-ovr.md) remains valid until specifically released and can be used to gather post-connection data.</span></span>

<span data-ttu-id="77e99-106">Завершение сеанса завершается путем отмены выделения и освобождения ресурсов, связанных с сеансом.</span><span class="sxs-lookup"><span data-stu-id="77e99-106">Session termination is completed by deallocating and releasing the resources associated with the session.</span></span> <span data-ttu-id="77e99-107">Если сеанс просто удаляется или отключается, но ресурсы не освобождаются, это приводит к утечке памяти в приложении и, возможно, также в поставщике услуг.</span><span class="sxs-lookup"><span data-stu-id="77e99-107">If a session is merely dropped or disconnected but resources are not released, the result is a memory leak in the application and possibly in the service provider as well.</span></span>

<span data-ttu-id="77e99-108">**Интерфейс TAPI 2. x:** См. раздел [**линедроп**](/windows/win32/api/tapi/nf-tapi-linedrop), [**линедеаллокатекалл**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span><span class="sxs-lookup"><span data-stu-id="77e99-108">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).</span></span>

<span data-ttu-id="77e99-109">**Интерфейс TAPI 3. x:** См. раздел [**итбасиккаллконтрол::D-Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect). выполните стандартный выпуск com для указателя на объект call.</span><span class="sxs-lookup"><span data-stu-id="77e99-109">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), perform a standard COM release on the Call object pointer.</span></span>

 

 
