---
title: Функции защитника Windows
description: Функции, вызываемые приложениями для запроса проверок, обновлений сигнатур или сведений из защитника Windows.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412433"
---
# <a name="windows-defender-functions"></a><span data-ttu-id="4f09b-103">Функции защитника Windows</span><span class="sxs-lookup"><span data-stu-id="4f09b-103">Windows Defender Functions</span></span>

<span data-ttu-id="4f09b-104">Функции, вызываемые приложениями для запроса проверок, обновлений сигнатур или сведений из защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="4f09b-104">Functions called by apps to request scans, signature updates, or information from Windows Defender.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f09b-105">Функция</span><span class="sxs-lookup"><span data-stu-id="4f09b-105">Function</span></span></th>
<th><span data-ttu-id="4f09b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="4f09b-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4f09b-107"><a href="mperrormessageformat.md"><strong>мперрормессажеформат</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-108">Возвращает отформатированное сообщение об ошибке на основе кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="4f09b-108">Returns a formatted error message based on an error code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f09b-109"><a href="mpfreememory.md"><strong>мпфримемори</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-110">Освобождает память для диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="4f09b-110">Frees memory for the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f09b-111"><a href="mphandleclose.md"><strong>мфандлеклосе</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-112">Закрывает маркер, возвращенный <a href="mpmanageropen.md"><strong>мпманажеропен</strong></a>, <a href="mpscanstart.md"><strong>мпсканстарт</strong></a>, <a href="mpthreatopen.md"><strong>мпсреатопен</strong></a>или <a href="mpupdatestart.md"><strong>мпупдатестарт</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4f09b-112">Closes the handle returned by <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>, or <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f09b-113"><a href="mpmanageropen.md"><strong>мпманажеропен</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-114">Устанавливает подключение к диспетчеру защиты от вредоносных программ на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4f09b-114">Establishes a connection to the malware protection manager on the local computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f09b-115"><a href="mpmanagerstatusquery.md"><strong>мпманажерстатускуери</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-116"><strong>Не поддерживается.</strong></span><span class="sxs-lookup"><span data-stu-id="4f09b-116"><strong>Not supported.</strong></span></span> <span data-ttu-id="4f09b-117">Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="4f09b-117">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f09b-118"><a href="mpmanagerstatusqueryex.md"><strong>мпманажерстатускуерекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-119">Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="4f09b-119">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f09b-120"><a href="mpmanagerversionquery.md"><strong>мпманажерверсионкуери</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-121">Возвращает сведения о версии различных компонентов диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="4f09b-121">Returns version information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f09b-122"><a href="mpscancontrol.md"><strong>мпсканконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-123">Разрешает Управление сканированием, которое было асинхронно инициировано через <a href="mpscanstart.md"><strong>мпсканстарт</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4f09b-123">Allows the control of a scan that was asynchronously initiated via <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f09b-124"><a href="mpscanstart.md"><strong>мпсканстарт</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-125">Запускает операцию сканирования.</span><span class="sxs-lookup"><span data-stu-id="4f09b-125">Starts a scanning operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f09b-126"><a href="mpthreatenumerate.md"><strong>мпсреатенумерате</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-127">Возвращает сведения о следующей угрозе в списке перечисления.</span><span class="sxs-lookup"><span data-stu-id="4f09b-127">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="4f09b-128">Эту функцию можно вызывать повторно до тех пор, пока не завершится перечисление всех угроз.</span><span class="sxs-lookup"><span data-stu-id="4f09b-128">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f09b-129"><a href="mpthreatopen.md"><strong>мпсреатопен</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-130">Возвращает маркер перечисления, предназначенный для получения угроз.</span><span class="sxs-lookup"><span data-stu-id="4f09b-130">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="4f09b-131">Эта функция может использоваться для открытия угроз, обнаруженных конкретным сканированием, всех активных угроз в системе, истории заражения угроз или всех угроз, имеющихся в базе данных сигнатур.</span><span class="sxs-lookup"><span data-stu-id="4f09b-131">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f09b-132"><a href="mpthreatquery.md"><strong>мпсреаткуери</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-133">Используется для запроса статических (таких как серьезность и категория) или локализованных сведений о конкретной угрозе (например, описание категории и рекомендации).</span><span class="sxs-lookup"><span data-stu-id="4f09b-133">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f09b-134"><a href="mpupdatecontrol.md"><strong>мпупдатеконтрол</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-135">Позволяет управлять операцией обновления сигнатур, которая была асинхронно инициирована через <a href="mpupdatestart.md"><strong>мпупдатестарт</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4f09b-135">Allows the control of a signature update operation that was asynchronously initiated via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f09b-136"><a href="mpupdatestart.md"><strong>мпупдатестарт</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-137">Запускает операцию обновления сигнатур.</span><span class="sxs-lookup"><span data-stu-id="4f09b-137">Starts a signature update operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f09b-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>вденабле</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-139">Изменяет состояние защитника Windows на вкл. или выключено.</span><span class="sxs-lookup"><span data-stu-id="4f09b-139">Changes Windows Defender status to on or off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4f09b-140">Начиная с Windows 10, версии 1607 и Windows Server 2016 функция <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>вденабле</strong></a> всегда возвращает <strong>E_NOTIMPL</strong>.</span><span class="sxs-lookup"><span data-stu-id="4f09b-140">Beginning in Windows 10, version 1607 and Windows Server 2016, the <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> function always returns <strong>E_NOTIMPL</strong>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f09b-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>вдстатус</strong></a></span><span class="sxs-lookup"><span data-stu-id="4f09b-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span></span></td>
<td><span data-ttu-id="4f09b-142">Возвращает текущее состояние защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="4f09b-142">Returns the current status of Windows Defender.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





