---
description: Объясняет использование токенов олицетворения в контроле доступа.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Токены олицетворения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664305"
---
# <a name="impersonation-tokens"></a><span data-ttu-id="9479e-103">Токены олицетворения</span><span class="sxs-lookup"><span data-stu-id="9479e-103">Impersonation Tokens</span></span>

<span data-ttu-id="9479e-104">Поток олицетворения имеет два [*маркера доступа*](/windows/desktop/SecGloss/a-gly):</span><span class="sxs-lookup"><span data-stu-id="9479e-104">An impersonating thread has two [*access tokens*](/windows/desktop/SecGloss/a-gly):</span></span>

-   <span data-ttu-id="9479e-105">[*Основной маркер доступа*](/windows/desktop/SecGloss/p-gly) , описывающий [*контекст безопасности*](/windows/desktop/SecGloss/s-gly) сервера.</span><span class="sxs-lookup"><span data-stu-id="9479e-105">A [*primary access token*](/windows/desktop/SecGloss/p-gly) that describes the [*security context*](/windows/desktop/SecGloss/s-gly) of the server.</span></span> <span data-ttu-id="9479e-106">Чтобы получить маркер для этого маркера, вызовите функцию [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .</span><span class="sxs-lookup"><span data-stu-id="9479e-106">To get a handle to this token, call the [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) function.</span></span>
-   <span data-ttu-id="9479e-107">Маркер доступа олицетворения, описывающий контекст безопасности олицетворенного клиента.</span><span class="sxs-lookup"><span data-stu-id="9479e-107">An impersonation access token that describes the security context of the client being impersonated.</span></span> <span data-ttu-id="9479e-108">Чтобы получить маркер для этого маркера, вызовите функцию [**опенсреадтокен**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .</span><span class="sxs-lookup"><span data-stu-id="9479e-108">To get a handle to this token, call the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function.</span></span>

<span data-ttu-id="9479e-109">Сервер может использовать [*токен олицетворения*](/windows/desktop/SecGloss/i-gly) в следующих функциях:</span><span class="sxs-lookup"><span data-stu-id="9479e-109">A server can use the [*impersonation token*](/windows/desktop/SecGloss/i-gly) in the following functions:</span></span>

-   <span data-ttu-id="9479e-110">В функциях [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**акцессчеккбитипе**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)и [**акцессчеккбитипересултлист**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) , чтобы определить, позволяет ли [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly) клиента использовать набор прав доступа.</span><span class="sxs-lookup"><span data-stu-id="9479e-110">In the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype), and [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) functions to determine whether a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows the client a set of access rights.</span></span>
-   <span data-ttu-id="9479e-111">В функции [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , чтобы включить или отключить права клиента.</span><span class="sxs-lookup"><span data-stu-id="9479e-111">In the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable or disable the client's privileges.</span></span>
-   <span data-ttu-id="9479e-112">В функции [**привилежечекк**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) , чтобы определить, включен ли набор привилегий в маркере клиента.</span><span class="sxs-lookup"><span data-stu-id="9479e-112">In the [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) function to determine whether a set of privileges are enabled in the client's token.</span></span>
-   <span data-ttu-id="9479e-113">В функциях, создающих записи в журнале событий безопасности, например [**обжектопенаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) или [**привилежедсервицеаудиталарм**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span><span class="sxs-lookup"><span data-stu-id="9479e-113">In functions that generate entries in the security event log, such as [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) or [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span></span> <span data-ttu-id="9479e-114">Эти функции используют токен олицетворения для получения сведений о клиенте для записи журнала.</span><span class="sxs-lookup"><span data-stu-id="9479e-114">These functions use an impersonation token to get information about the client for the log entry.</span></span>

 

 
