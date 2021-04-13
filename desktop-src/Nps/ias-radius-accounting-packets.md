---
title: Ведение журнала с помощью сервера политики сети
description: Ведение журнала с помощью сервера политики сети
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338412"
---
# <a name="logging-with-network-policy-server"></a><span data-ttu-id="1b31d-103">Ведение журнала с помощью сервера политики сети</span><span class="sxs-lookup"><span data-stu-id="1b31d-103">Logging With Network Policy Server</span></span>

> [!Note]  
> <span data-ttu-id="1b31d-104">Служба проверки подлинности в Интернете (IAS) переименовала сервер политики сети (NPS), начиная с Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1b31d-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1b31d-105">Содержимое этого раздела относится как к IAS, так и к NPS.</span><span class="sxs-lookup"><span data-stu-id="1b31d-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1b31d-106">По всему тексту NPS используется для ссылки на все версии службы, включая версии, изначально называемые IAS.</span><span class="sxs-lookup"><span data-stu-id="1b31d-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="1b31d-107">В следующей таблице описаны только наиболее важные аспекты пакетов учета RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b31d-107">The following table describes only the most important aspects of the RADIUS accounting packets.</span></span> <span data-ttu-id="1b31d-108">В документе о запросе учета RADIUS для комментариев ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) содержатся подробные сведения об этих пакетах.</span><span class="sxs-lookup"><span data-stu-id="1b31d-108">The RADIUS Accounting Request for Comments document ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) provides detailed information on these packets.</span></span>

<span data-ttu-id="1b31d-109">Пакеты учета RADIUS можно разделить на следующие категории.</span><span class="sxs-lookup"><span data-stu-id="1b31d-109">RADIUS accounting packets can be divided into the following categories.</span></span>



| <span data-ttu-id="1b31d-110">Пакет учета</span><span class="sxs-lookup"><span data-stu-id="1b31d-110">Accounting packet</span></span>  | <span data-ttu-id="1b31d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1b31d-111">Description</span></span>                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b31d-112">Accounting-On</span><span class="sxs-lookup"><span data-stu-id="1b31d-112">Accounting-On</span></span>      | <span data-ttu-id="1b31d-113">Отправляется сервером сетевого доступа (NAS) для указания на перезагрузку.</span><span class="sxs-lookup"><span data-stu-id="1b31d-113">Sent by the Network Access Server (NAS) to indicate that it has restarted.</span></span><br/> <span data-ttu-id="1b31d-114">Содержит идентификатор NAS-identifier/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="1b31d-114">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                        |
| <span data-ttu-id="1b31d-115">Accounting-Off</span><span class="sxs-lookup"><span data-stu-id="1b31d-115">Accounting-Off</span></span>     | <span data-ttu-id="1b31d-116">Отправляется NAS для указания на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="1b31d-116">Sent by the NAS to indicate that it is being shutdown.</span></span><br/> <span data-ttu-id="1b31d-117">Содержит идентификатор NAS-identifier/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="1b31d-117">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                                            |
| <span data-ttu-id="1b31d-118">Accounting-Start</span><span class="sxs-lookup"><span data-stu-id="1b31d-118">Accounting-Start</span></span>   | <span data-ttu-id="1b31d-119">Отправляется NAS, после того как пользователь прошел проверку подлинности и авторизован, чтобы указать начало сеанса пользователя.</span><span class="sxs-lookup"><span data-stu-id="1b31d-119">Sent by the NAS, after the user was authenticated and authorized, to indicate the start of a user session.</span></span> <br/> <span data-ttu-id="1b31d-120">Содержит UserID, NAS-identifier/IPAddress и другие сведения, полученные от NAS.</span><span class="sxs-lookup"><span data-stu-id="1b31d-120">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/> |
| <span data-ttu-id="1b31d-121">Accounting-Stop</span><span class="sxs-lookup"><span data-stu-id="1b31d-121">Accounting-Stop</span></span>    | <span data-ttu-id="1b31d-122">Отправляется NAS для указания на конец сеанса пользователя.</span><span class="sxs-lookup"><span data-stu-id="1b31d-122">Sent by the NAS to indicate the end of a user session.</span></span><br/> <span data-ttu-id="1b31d-123">Содержит UserID, NAS-identifier/IPAddress и другие сведения, полученные от NAS.</span><span class="sxs-lookup"><span data-stu-id="1b31d-123">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/>                                                      |
| <span data-ttu-id="1b31d-124">Accounting-Interim</span><span class="sxs-lookup"><span data-stu-id="1b31d-124">Accounting-Interim</span></span> | <span data-ttu-id="1b31d-125">Может периодически отправляться NAS для каждого пользователя, вошедшего в систему на NAS.</span><span class="sxs-lookup"><span data-stu-id="1b31d-125">Could be sent periodically by the NAS for each user that is logged on at the NAS.</span></span> <br/> <span data-ttu-id="1b31d-126">Эта функция обычно поддерживается в более новых версиях NAS.</span><span class="sxs-lookup"><span data-stu-id="1b31d-126">This feature is generally supported in newer versions of NAS.</span></span><br/>                                                     |



 

<span data-ttu-id="1b31d-127">При сборе данных учета, доступных через RADIUS, важно учитывать следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="1b31d-127">The following issues are important to consider when collecting accounting information made available through RADIUS:</span></span>

-   <span data-ttu-id="1b31d-128">В редких случаях пакеты могут быть потеряны во время передачи и никогда не достигают сервера RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b31d-128">In rare cases, packets could be lost during transmission and may never reach the RADIUS server.</span></span>
-   <span data-ttu-id="1b31d-129">Сервер RADIUS не получает уведомления при прерывании работы NAS.</span><span class="sxs-lookup"><span data-stu-id="1b31d-129">The RADIUS server is not notified if the NAS aborts.</span></span>
-   <span data-ttu-id="1b31d-130">ISDN поддерживает несколько сеансов, и каждый сеанс создает пару пакетов Account-Start/-остановкой.</span><span class="sxs-lookup"><span data-stu-id="1b31d-130">ISDN supports multiple sessions and each session generates an Accounting-Start/-Stop pair of packets.</span></span> <span data-ttu-id="1b31d-131">Существует атрибут учета, именуемый идентификатором нескольких сеансов, который четко определяет такие многосеансовые пакеты.</span><span class="sxs-lookup"><span data-stu-id="1b31d-131">There is an accounting attribute called multi-session identifier that clearly identifies such multi-session packets.</span></span> <span data-ttu-id="1b31d-132">Проверьте многосеансовый идентификатор в дополнение к идентификатору сеанса, чтобы вычислить количество сеансов.</span><span class="sxs-lookup"><span data-stu-id="1b31d-132">Check for the multi-session identifier in addition to the session identifier to calculate the number of sessions.</span></span>

## <a name="requests-logged-by-nps"></a><span data-ttu-id="1b31d-133">Запросы, регистрируемые NPS</span><span class="sxs-lookup"><span data-stu-id="1b31d-133">Requests Logged by NPS</span></span>

<span data-ttu-id="1b31d-134">По умолчанию NPS не регистрирует никаких данных.</span><span class="sxs-lookup"><span data-stu-id="1b31d-134">By default, NPS does not log any data.</span></span> <span data-ttu-id="1b31d-135">NPS можно настроить с помощью пользовательского интерфейса NPS (NPS. msc), чтобы заносить в журнал следующие запросы.</span><span class="sxs-lookup"><span data-stu-id="1b31d-135">NPS can be configured, using the NPS user interface (nps.msc), to log the following requests.</span></span>



| <span data-ttu-id="1b31d-136">Записанный пакет</span><span class="sxs-lookup"><span data-stu-id="1b31d-136">Logged packet</span></span>          | <span data-ttu-id="1b31d-137">Описание</span><span class="sxs-lookup"><span data-stu-id="1b31d-137">Description</span></span>                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b31d-138">Запрос учета</span><span class="sxs-lookup"><span data-stu-id="1b31d-138">Accounting Request</span></span>     | <span data-ttu-id="1b31d-139">Любой из пакетов учета, описанных в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="1b31d-139">Any of the accounting packets described in the previous table.</span></span><br/>                                                                    |
| <span data-ttu-id="1b31d-140">Запрос проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="1b31d-140">Authentication Request</span></span> | <span data-ttu-id="1b31d-141">Отправляется NAS от имени подключающегося пользователя.</span><span class="sxs-lookup"><span data-stu-id="1b31d-141">Sent by the NAS on behalf of the connecting user.</span></span><br/> <span data-ttu-id="1b31d-142">Записи журнала содержат только входящие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1b31d-142">The log entries contain only incoming attributes.</span></span><br/>                    |
| <span data-ttu-id="1b31d-143">Принятие проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="1b31d-143">Authentication Accept</span></span>  | <span data-ttu-id="1b31d-144">Отправляется NPS для указания на то, что подключение пользователя должно быть принято.</span><span class="sxs-lookup"><span data-stu-id="1b31d-144">Sent by NPS to indicate that the user connection should be accepted.</span></span><br/> <span data-ttu-id="1b31d-145">Записи журнала содержат только исходящие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1b31d-145">The log entries contain only outgoing attributes.</span></span><br/> |
| <span data-ttu-id="1b31d-146">Отклонение проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="1b31d-146">Authentication Reject</span></span>  | <span data-ttu-id="1b31d-147">Отсылается NPS, чтобы указать, что подключение пользователя должно быть отклонено.</span><span class="sxs-lookup"><span data-stu-id="1b31d-147">Sent by NPS to indicate that the user connection should be rejected.</span></span><br/> <span data-ttu-id="1b31d-148">Записи журнала содержат только исходящие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1b31d-148">The log entries contain only outgoing attributes.</span></span><br/> |



 

<span data-ttu-id="1b31d-149">Данные, регистрируемые NPS, могут попасть в текстовый файл на сервере NPS или в центральную базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="1b31d-149">Data logged by NPS can go to a text file on the NPS server or to a central SQL database.</span></span> <span data-ttu-id="1b31d-150">Дополнительные сведения о ведении журнала NPS SQL см. в разделе [программирование SQL](sql-programmability.md).</span><span class="sxs-lookup"><span data-stu-id="1b31d-150">For more information on NPS SQL logging, see [SQL Programmability](sql-programmability.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b31d-151">См. также</span><span class="sxs-lookup"><span data-stu-id="1b31d-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b31d-152">Служба проверки подлинности в Интернете и сервер политики сети</span><span class="sxs-lookup"><span data-stu-id="1b31d-152">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="1b31d-153">Проверка подлинности, авторизация и учет RADIUS</span><span class="sxs-lookup"><span data-stu-id="1b31d-153">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="1b31d-154">Работа с сервером состояний</span><span class="sxs-lookup"><span data-stu-id="1b31d-154">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

