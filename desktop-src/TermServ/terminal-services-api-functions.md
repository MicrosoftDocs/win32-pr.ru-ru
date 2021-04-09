---
title: Функции API службы удаленных рабочих столов
description: Для службы удаленных рабочих столов используются следующие функции.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792133"
---
# <a name="remote-desktop-services-api-functions"></a><span data-ttu-id="7b674-103">Функции API службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="7b674-103">Remote Desktop Services API Functions</span></span>

<span data-ttu-id="7b674-104">Для службы удаленных рабочих столов используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="7b674-104">The following functions are used with Remote Desktop Services.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7b674-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="7b674-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="7b674-106">**процессидтосессионид**</span><span class="sxs-lookup"><span data-stu-id="7b674-106">**ProcessIdToSessionId**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

<span data-ttu-id="7b674-107">Извлекает службы удаленных рабочих столов сеанс, связанный с указанным процессом.</span><span class="sxs-lookup"><span data-stu-id="7b674-107">Retrieves the Remote Desktop Services session associated with a specified process.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-108">**тлсконнекттолссервер**</span><span class="sxs-lookup"><span data-stu-id="7b674-108">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dd>

<span data-ttu-id="7b674-109">Открывает маркер указанного сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="7b674-109">Opens a handle to the specified Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-110">**тлсдисконнектфромсервер**</span><span class="sxs-lookup"><span data-stu-id="7b674-110">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> <dd>

<span data-ttu-id="7b674-111">Закрывает открытый маркер для сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="7b674-111">Closes an open handle to a Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-112">**тлсжетсерверцертификате**</span><span class="sxs-lookup"><span data-stu-id="7b674-112">**TLSGetServerCertificate**</span></span>](tlsgetservercertificate.md)
</dt> <dd>

<span data-ttu-id="7b674-113">Возвращает сертификат сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="7b674-113">Returns the certificate of the Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-114">**тлскэйпаккенумбегин**</span><span class="sxs-lookup"><span data-stu-id="7b674-114">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dd>

<span data-ttu-id="7b674-115">Начинает перечисление всех ключевых пакетов, установленных на сервере лицензий удаленный рабочий стол на основе условий поиска.</span><span class="sxs-lookup"><span data-stu-id="7b674-115">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-116">**тлскэйпаккенуменд**</span><span class="sxs-lookup"><span data-stu-id="7b674-116">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> <dd>

<span data-ttu-id="7b674-117">Переходит от предыдущего вызова функции [**тлскэйпаккенумбегин**](tlskeypackenumbegin.md) и завершает перечисление.</span><span class="sxs-lookup"><span data-stu-id="7b674-117">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-118">**тлскэйпаккенумнекст**</span><span class="sxs-lookup"><span data-stu-id="7b674-118">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dd>

<span data-ttu-id="7b674-119">Переходит от предыдущего вызова функции [**тлскэйпаккенумбегин**](tlskeypackenumbegin.md) и возвращает следующий пакет ключей, установленный на сервере лицензирования удаленный рабочий стол, который соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="7b674-119">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-120">**тлслиценсинумбегин**</span><span class="sxs-lookup"><span data-stu-id="7b674-120">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dd>

<span data-ttu-id="7b674-121">Начинает перечисление лицензий, выданных сервером лицензий удаленный рабочий стол на основе условий поиска.</span><span class="sxs-lookup"><span data-stu-id="7b674-121">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-122">**тлслиценсинуменд**</span><span class="sxs-lookup"><span data-stu-id="7b674-122">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> <dd>

<span data-ttu-id="7b674-123">Переходит от предыдущего вызова функции [**тлслиценсинумбегин**](tlslicenseenumbegin.md) и завершает перечисление.</span><span class="sxs-lookup"><span data-stu-id="7b674-123">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and terminates the enumeration.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-124">**тлслиценсинумнекст**</span><span class="sxs-lookup"><span data-stu-id="7b674-124">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dd>

<span data-ttu-id="7b674-125">Продолжение предыдущего вызова функции [**тлслиценсинумбегин**](tlslicenseenumbegin.md) и возврат следующей лицензии, установленной на сервере лицензирования удаленный рабочий стол, соответствующем условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="7b674-125">Continues from a previous call to the [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) function and returns the next license that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-126">**виртуалчаннелклосе**</span><span class="sxs-lookup"><span data-stu-id="7b674-126">**VirtualChannelClose**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

<span data-ttu-id="7b674-127">Закрывает клиентский узел виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="7b674-127">Closes the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-128">**виртуалчаннелентри**</span><span class="sxs-lookup"><span data-stu-id="7b674-128">**VirtualChannelEntry**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

<span data-ttu-id="7b674-129">Определяемая приложением точка входа для клиентской библиотеки DLL приложения, использующего службы удаленных рабочих столов виртуальные каналы.</span><span class="sxs-lookup"><span data-stu-id="7b674-129">An application-defined entry point for the client-side DLL of an application that uses Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-130">**виртуалчаннелинит**</span><span class="sxs-lookup"><span data-stu-id="7b674-130">**VirtualChannelInit**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

<span data-ttu-id="7b674-131">Инициализирует доступ клиентской библиотеки DLL к службы удаленных рабочих столов виртуальным каналам.</span><span class="sxs-lookup"><span data-stu-id="7b674-131">Initializes a client DLL's access to Remote Desktop Services virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-132">*виртуалчаннелинитевент*</span><span class="sxs-lookup"><span data-stu-id="7b674-132">*VirtualChannelInitEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

<span data-ttu-id="7b674-133">Определяемая приложением функция обратного вызова, службы удаленных рабочих столов вызовов для уведомления клиентской библиотеки о событиях виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="7b674-133">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of virtual channel events.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-134">**виртуалчаннелопен**</span><span class="sxs-lookup"><span data-stu-id="7b674-134">**VirtualChannelOpen**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

<span data-ttu-id="7b674-135">Открывает клиентский узел виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="7b674-135">Opens the client end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-136">*виртуалчаннелопеневент*</span><span class="sxs-lookup"><span data-stu-id="7b674-136">*VirtualChannelOpenEvent*</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

<span data-ttu-id="7b674-137">Определяемая приложением функция обратного вызова, которая службы удаленных рабочих столов вызовы для уведомления клиентской библиотеки событий для определенного виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="7b674-137">An application-defined callback function that Remote Desktop Services calls to notify the client DLL of events for a specific virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-138">**виртуалчаннелврите**</span><span class="sxs-lookup"><span data-stu-id="7b674-138">**VirtualChannelWrite**</span></span>](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

<span data-ttu-id="7b674-139">Отправляет данные с клиентской стороны виртуального канала в приложение-партнер на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="7b674-139">Sends data from the client end of a virtual channel to a partner application on the server end.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-140">**втсклосесервер**</span><span class="sxs-lookup"><span data-stu-id="7b674-140">**WTSCloseServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

<span data-ttu-id="7b674-141">Закрывает открытый маркер на сервере узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="7b674-141">Closes an open handle to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-142">**втсконнектсессион**</span><span class="sxs-lookup"><span data-stu-id="7b674-142">**WTSConnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

<span data-ttu-id="7b674-143">Подключает сеанс службы удаленных рабочих столов к существующему сеансу на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="7b674-143">Connects a Remote Desktop Services session to an existing session on the local computer.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-144">**втскреателистенер**</span><span class="sxs-lookup"><span data-stu-id="7b674-144">**WTSCreateListener**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

<span data-ttu-id="7b674-145">Создает новый прослушиватель службы удаленных рабочих столов или настраивает существующий прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="7b674-145">Creates a new Remote Desktop Services listener or configures an existing listener.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-146">**втсдисконнектсессион**</span><span class="sxs-lookup"><span data-stu-id="7b674-146">**WTSDisconnectSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

<span data-ttu-id="7b674-147">Отключает вошедшего в систему пользователя из указанного сеанса службы удаленных рабочих столов, не закрывая сеанс.</span><span class="sxs-lookup"><span data-stu-id="7b674-147">Disconnects the logged-on user from the specified Remote Desktop Services session without closing the session.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-148">**втсенаблечилдсессионс**</span><span class="sxs-lookup"><span data-stu-id="7b674-148">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

<span data-ttu-id="7b674-149">Включает или отключает [дочерние сеансы](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="7b674-149">Enables or disables [Child Sessions](child-sessions.md).</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-150">**втсенумерателистенерс**</span><span class="sxs-lookup"><span data-stu-id="7b674-150">**WTSEnumerateListeners**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

<span data-ttu-id="7b674-151">Перечисление всех прослушивателей службы удаленных рабочих столов на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-151">Enumerates all the Remote Desktop Services listeners on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-152">**втсенумератепроцессес**</span><span class="sxs-lookup"><span data-stu-id="7b674-152">**WTSEnumerateProcesses**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

<span data-ttu-id="7b674-153">Извлекает сведения об активных процессах на указанном сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-153">Retrieves information about the active processes on a specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-154">**втсенумератепроцессесекс**</span><span class="sxs-lookup"><span data-stu-id="7b674-154">**WTSEnumerateProcessesEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

<span data-ttu-id="7b674-155">Извлекает сведения об активных процессах на указанном сервере узла сеансов удаленных рабочих столов или на сервере узла виртуализации удаленных рабочих столов (Узел виртуализации удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="7b674-155">Retrieves information about the active processes on the specified RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-156">**втсенумератесерверс**</span><span class="sxs-lookup"><span data-stu-id="7b674-156">**WTSEnumerateServers**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

<span data-ttu-id="7b674-157">Возвращает список всех серверов узлов сеансов удаленных рабочих столов в указанном домене.</span><span class="sxs-lookup"><span data-stu-id="7b674-157">Returns a list of all RD Session Host servers within the specified domain.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-158">**втсенумератесессионс**</span><span class="sxs-lookup"><span data-stu-id="7b674-158">**WTSEnumerateSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

<span data-ttu-id="7b674-159">Получает список сеансов на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-159">Retrieves a list of sessions on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-160">**втсенумератесессионсекс**</span><span class="sxs-lookup"><span data-stu-id="7b674-160">**WTSEnumerateSessionsEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

<span data-ttu-id="7b674-161">Получает список сеансов на указанном сервере узла сеансов удаленных рабочих столов или сервере узла виртуализации удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-161">Retrieves a list of sessions on a specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-162">**втсфримемори**</span><span class="sxs-lookup"><span data-stu-id="7b674-162">**WTSFreeMemory**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

<span data-ttu-id="7b674-163">Освобождает память, выделенную функцией службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-163">Frees memory allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-164">**втсфримеморекс**</span><span class="sxs-lookup"><span data-stu-id="7b674-164">**WTSFreeMemoryEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

<span data-ttu-id="7b674-165">Освобождает память, содержащую [**сведения о \_ процессе \_ \_ ВТС**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) , а также структуры [**\_ сеанса \_ \_ 1 ВТС**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) , выделенные функцией службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-165">Frees memory that contains [**WTS\_PROCESS\_INFO\_EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) or [**WTS\_SESSION\_INFO\_1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) structures allocated by a Remote Desktop Services function.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-166">**втсжетактивеконсолесессионид**</span><span class="sxs-lookup"><span data-stu-id="7b674-166">**WTSGetActiveConsoleSessionId**</span></span>](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

<span data-ttu-id="7b674-167">Возвращает идентификатор сеанса консоли.</span><span class="sxs-lookup"><span data-stu-id="7b674-167">Retrieves the session identifier of the console session.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-168">**втсжетчилдсессионид**</span><span class="sxs-lookup"><span data-stu-id="7b674-168">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

<span data-ttu-id="7b674-169">Возвращает идентификатор дочернего сеанса, если он есть.</span><span class="sxs-lookup"><span data-stu-id="7b674-169">Retrieves the child session identifier, if present.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-170">**втсжетлистенерсекурити**</span><span class="sxs-lookup"><span data-stu-id="7b674-170">**WTSGetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="7b674-171">Возвращает дескриптор безопасности прослушивателя службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-171">Retrieves the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-172">**втсисчилдсессионсенаблед**</span><span class="sxs-lookup"><span data-stu-id="7b674-172">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

<span data-ttu-id="7b674-173">Определяет, включены ли дочерние сеансы.</span><span class="sxs-lookup"><span data-stu-id="7b674-173">Determines whether child sessions are enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-174">**втслогоффсессион**</span><span class="sxs-lookup"><span data-stu-id="7b674-174">**WTSLogoffSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

<span data-ttu-id="7b674-175">Записывает в журнал указанный сеанс службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-175">Logs off a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-176">**втсопенсервер**</span><span class="sxs-lookup"><span data-stu-id="7b674-176">**WTSOpenServer**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

<span data-ttu-id="7b674-177">Открывает обработчик для указанного сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-177">Opens a handle to the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-178">**втсопенсерверекс**</span><span class="sxs-lookup"><span data-stu-id="7b674-178">**WTSOpenServerEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

<span data-ttu-id="7b674-179">Открывает обработчик для указанного сервера узла сеансов удаленных рабочих столов или сервера узла виртуализации удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-179">Opens a handle to the specified RD Session Host server or RD Virtualization Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-180">**втскуерилистенерконфиг**</span><span class="sxs-lookup"><span data-stu-id="7b674-180">**WTSQueryListenerConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

<span data-ttu-id="7b674-181">Извлекает сведения о конфигурации для прослушивателя службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-181">Retrieves configuration information for a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-182">**втскуерисессионинформатион**</span><span class="sxs-lookup"><span data-stu-id="7b674-182">**WTSQuerySessionInformation**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

<span data-ttu-id="7b674-183">Извлекает сведения о сеансе для указанного сеанса на указанном сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-183">Retrieves session information for the specified session on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-184">**втскуерюсерконфиг**</span><span class="sxs-lookup"><span data-stu-id="7b674-184">**WTSQueryUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

<span data-ttu-id="7b674-185">Извлекает сведения о конфигурации указанного пользователя на указанном контроллере домена или сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-185">Retrieves configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-186">**втскуерюсертокен**</span><span class="sxs-lookup"><span data-stu-id="7b674-186">**WTSQueryUserToken**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

<span data-ttu-id="7b674-187">Получает основной маркер доступа пользователя, выполнившего вход в систему, заданный ИДЕНТИФИКАТОРом сеанса.</span><span class="sxs-lookup"><span data-stu-id="7b674-187">Obtains the primary access token of the logged-on user specified by the session ID.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-188">**втсрегистерсессионнотификатион**</span><span class="sxs-lookup"><span data-stu-id="7b674-188">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

<span data-ttu-id="7b674-189">Регистрирует указанное окно для получения уведомлений об изменениях сеанса.</span><span class="sxs-lookup"><span data-stu-id="7b674-189">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-190">**втсрегистерсессионнотификатионекс**</span><span class="sxs-lookup"><span data-stu-id="7b674-190">**WTSRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="7b674-191">Регистрирует указанное окно для получения уведомлений об изменениях сеанса.</span><span class="sxs-lookup"><span data-stu-id="7b674-191">Registers the specified window to receive session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-192">**втссендмессаже**</span><span class="sxs-lookup"><span data-stu-id="7b674-192">**WTSSendMessage**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

<span data-ttu-id="7b674-193">Отображает окно сообщения на клиентском компьютере указанного сеанса службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-193">Displays a message box on the client desktop of a specified Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-194">**втссетлистенерсекурити**</span><span class="sxs-lookup"><span data-stu-id="7b674-194">**WTSSetListenerSecurity**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

<span data-ttu-id="7b674-195">Настраивает дескриптор безопасности прослушивателя службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-195">Configures the security descriptor of a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-196">**втссетусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="7b674-196">**WTSSetUserConfig**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

<span data-ttu-id="7b674-197">Изменяет сведения о конфигурации для указанного пользователя на указанном контроллере домена или на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-197">Modifies configuration information for the specified user on the specified domain controller or RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-198">**втсшутдовнсистем**</span><span class="sxs-lookup"><span data-stu-id="7b674-198">**WTSShutdownSystem**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

<span data-ttu-id="7b674-199">Завершает работу (и при необходимости перезапускает) указанного сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-199">Shuts down (and optionally restarts) the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-200">**втсстартремотеконтролсессион**</span><span class="sxs-lookup"><span data-stu-id="7b674-200">**WTSStartRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

<span data-ttu-id="7b674-201">Запускает Удаленное управление другим сеансом службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-201">Starts the remote control of another Remote Desktop Services session.</span></span> <span data-ttu-id="7b674-202">Эту функцию необходимо вызывать из удаленного сеанса.</span><span class="sxs-lookup"><span data-stu-id="7b674-202">You must call this function from a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-203">**втсстопремотеконтролсессион**</span><span class="sxs-lookup"><span data-stu-id="7b674-203">**WTSStopRemoteControlSession**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

<span data-ttu-id="7b674-204">Останавливает сеанс удаленного управления.</span><span class="sxs-lookup"><span data-stu-id="7b674-204">Stops a remote control session.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-205">**втстерминатепроцесс**</span><span class="sxs-lookup"><span data-stu-id="7b674-205">**WTSTerminateProcess**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

<span data-ttu-id="7b674-206">Завершает указанный процесс на указанном сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7b674-206">Terminates the specified process on the specified RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-207">**втсунрегистерсессионнотификатион**</span><span class="sxs-lookup"><span data-stu-id="7b674-207">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

<span data-ttu-id="7b674-208">Отменяет регистрацию указанного окна, чтобы он не получал дальнейшие уведомления об изменении сеанса.</span><span class="sxs-lookup"><span data-stu-id="7b674-208">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-209">**втсунрегистерсессионнотификатионекс**</span><span class="sxs-lookup"><span data-stu-id="7b674-209">**WTSUnRegisterSessionNotificationEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

<span data-ttu-id="7b674-210">Отменяет регистрацию указанного окна, чтобы он не получал дальнейшие уведомления об изменении сеанса.</span><span class="sxs-lookup"><span data-stu-id="7b674-210">Unregisters the specified window so that it receives no further session change notifications.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-211">**втсвиртуалчаннелклосе**</span><span class="sxs-lookup"><span data-stu-id="7b674-211">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="7b674-212">Закрывает открытый маркер виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="7b674-212">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-213">**втсвиртуалчаннелопен**</span><span class="sxs-lookup"><span data-stu-id="7b674-213">**WTSVirtualChannelOpen**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

<span data-ttu-id="7b674-214">Открывает обработчик для указанного виртуального канала на сервере.</span><span class="sxs-lookup"><span data-stu-id="7b674-214">Opens a handle to the server end of a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-215">**втсвиртуалчаннелопенекс**</span><span class="sxs-lookup"><span data-stu-id="7b674-215">**WTSVirtualChannelOpenEx**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

<span data-ttu-id="7b674-216">Создает виртуальный канал таким же образом, как и [**втсвиртуалчаннелопен**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span><span class="sxs-lookup"><span data-stu-id="7b674-216">Creates a virtual channel in a manner similar to [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-217">**втсвиртуалчаннелпуржеинпут**</span><span class="sxs-lookup"><span data-stu-id="7b674-217">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="7b674-218">Удаляет из указанного виртуального канала все входные данные очереди, отправленные с клиента на сервер.</span><span class="sxs-lookup"><span data-stu-id="7b674-218">Deletes all queued input data sent from the client to the server on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-219">**втсвиртуалчаннелпуржеаутпут**</span><span class="sxs-lookup"><span data-stu-id="7b674-219">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="7b674-220">Удаляет из указанного виртуального канала все выходные данные в очереди, отправленные с сервера клиенту.</span><span class="sxs-lookup"><span data-stu-id="7b674-220">Deletes all queued output data sent from the server to the client on a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-221">**втсвиртуалчаннелкуери**</span><span class="sxs-lookup"><span data-stu-id="7b674-221">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="7b674-222">Возвращает сведения об указанном виртуальном канале.</span><span class="sxs-lookup"><span data-stu-id="7b674-222">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-223">**втсвиртуалчаннелреад**</span><span class="sxs-lookup"><span data-stu-id="7b674-223">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="7b674-224">Считывает данные с конца виртуального канала на сервере.</span><span class="sxs-lookup"><span data-stu-id="7b674-224">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-225">**втсвиртуалчаннелврите**</span><span class="sxs-lookup"><span data-stu-id="7b674-225">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="7b674-226">Записывает данные на серверный конец виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="7b674-226">Writes data to the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="7b674-227">**втсваитсистемевент**</span><span class="sxs-lookup"><span data-stu-id="7b674-227">**WTSWaitSystemEvent**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

<span data-ttu-id="7b674-228">Ожидает события службы удаленных рабочих столов перед возвратом вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="7b674-228">Waits for a Remote Desktop Services event before returning to the caller.</span></span>

</dd> </dl>

 

 