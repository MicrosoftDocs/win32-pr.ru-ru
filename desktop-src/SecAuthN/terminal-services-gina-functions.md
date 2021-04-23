---
description: Если службы терминалов включены, GINA должен вызывать функции поддержки Winlogon для завершения установки каждого пользователя, для запроса учетных данных сеанса клиента служб терминалов и для отключения от сетевого сеанса служб терминалов. Примечание. библиотеки DLL GINA не учитываются в Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Функции GINA служб терминалов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897166"
---
# <a name="terminal-services-gina-functions"></a><span data-ttu-id="ee4a2-103">Функции GINA служб терминалов</span><span class="sxs-lookup"><span data-stu-id="ee4a2-103">Terminal Services GINA Functions</span></span>

<span data-ttu-id="ee4a2-104">Если службы терминалов включены, [*GINA*](../secgloss/g-gly.md) должен вызывать функции поддержки [*Winlogon*](../secgloss/w-gly.md) для завершения установки каждого пользователя, для запроса [*учетных данных*](../secgloss/c-gly.md) сеанса клиента служб терминалов и для отключения от сетевого сеанса служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-104">When Terminal Services are enabled, the [*GINA*](../secgloss/g-gly.md) must call [*Winlogon*](../secgloss/w-gly.md) support functions to complete the setup for each user, to query the [*credentials*](../secgloss/c-gly.md) of a Terminal Services client session, and to disconnect from a Terminal Services network session.</span></span>

> [!Note]  
> <span data-ttu-id="ee4a2-105">Библиотеки DLL GINA не учитываются в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="ee4a2-106">В число этих функций поддержки входят следующие.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-106">These support functions include the following.</span></span>



| <span data-ttu-id="ee4a2-107">Функция</span><span class="sxs-lookup"><span data-stu-id="ee4a2-107">Function</span></span>                                                                     | <span data-ttu-id="ee4a2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ee4a2-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee4a2-109">**WlxWin31Migrate**</span><span class="sxs-lookup"><span data-stu-id="ee4a2-109">**WlxWin31Migrate**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | <span data-ttu-id="ee4a2-110">Завершает установку пользователя.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-110">Completes the setup of the user.</span></span>                                                                    |
| [<span data-ttu-id="ee4a2-111">**влкскуериклиенткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="ee4a2-111">**WlxQueryClientCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | <span data-ttu-id="ee4a2-112">Вызывается для запроса учетных данных удаленных клиентов, не использующих лицензию подключателя к Интернету.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-112">Called to query the credentials of remote clients that are not using an Internet connector license.</span></span> |
| [<span data-ttu-id="ee4a2-113">**влкскуеринетконнекторкредентиалс**</span><span class="sxs-lookup"><span data-stu-id="ee4a2-113">**WlxQueryInetConnectorCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | <span data-ttu-id="ee4a2-114">Вызывается для запроса учетных данных удаленных клиентов, использующих лицензию подключателя к Интернету.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-114">Called to query the credentials of remote clients that are using an Internet connector license.</span></span>     |
| [<span data-ttu-id="ee4a2-115">**влкскуеритерминалсервицесдата**</span><span class="sxs-lookup"><span data-stu-id="ee4a2-115">**WlxQueryTerminalServicesData**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | <span data-ttu-id="ee4a2-116">Вызывается для получения сведений о конфигурации пользователя служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-116">Called to retrieve Terminal Services user configuration information.</span></span>                                |
| [<span data-ttu-id="ee4a2-117">**влксдисконнект**</span><span class="sxs-lookup"><span data-stu-id="ee4a2-117">**WlxDisconnect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | <span data-ttu-id="ee4a2-118">Вызывается для отключения от сетевого сеанса служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-118">Called to disconnect from a Terminal Services network session.</span></span>                                      |



 

<span data-ttu-id="ee4a2-119">Чтобы получить доступ к этим функциям поддержки Winlogon, Библиотека DLL GINA должна использовать структуру [**влкс \_ Dispatch \_ версии \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) .</span><span class="sxs-lookup"><span data-stu-id="ee4a2-119">In order to access these Winlogon support functions, the GINA DLL must use the [**WLX\_DISPATCH\_VERSION\_1\_3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) structure.</span></span> <span data-ttu-id="ee4a2-120">В функции [**ВЛКСНЕГОТИАТЕ**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) GINA оба параметра должны быть не ниже влкс \_ версии \_ 1 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-120">In the GINA's [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) function, both parameters must be at least WLX\_VERSION\_1\_3.</span></span>

 

 
