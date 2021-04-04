---
title: Отключение функций службы удаленных рабочих столов
description: Для повышения безопасности можно отключить службы удаленных рабочих столов функции.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "103988072"
---
# <a name="disabling-remote-desktop-services-features"></a><span data-ttu-id="4449a-103">Отключение функций службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="4449a-103">Disabling Remote Desktop Services features</span></span>

<span data-ttu-id="4449a-104">Для повышения безопасности можно отключить службы удаленных рабочих столов такие функции, как перенаправление буфера обмена и перенаправление принтеров, для клиентов, подключающихся к серверам узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) с помощью удаленный рабочий стол элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="4449a-104">For enhanced security, you might choose to disable Remote Desktop Services features such as clipboard redirection and printer redirection for clients that connect to Remote Desktop Session Host (RD Session Host) servers using the Remote Desktop ActiveX Control.</span></span>

<span data-ttu-id="4449a-105">**Отключение функций службы удаленных рабочих столов**</span><span class="sxs-lookup"><span data-stu-id="4449a-105">**To disable Remote Desktop Services features**</span></span>

1.  <span data-ttu-id="4449a-106">Измените реестр клиентского компьютера и добавьте следующие ключи:</span><span class="sxs-lookup"><span data-stu-id="4449a-106">Edit the registry of the client computer and add the following keys:</span></span>

    -   <span data-ttu-id="4449a-107">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Terminal Server \\ дисаблеклипбоардредиректион**</span><span class="sxs-lookup"><span data-stu-id="4449a-107">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableClipboardRedirection**</span></span>
    -   <span data-ttu-id="4449a-108">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Terminal Server \\ дисабледривередиректион**</span><span class="sxs-lookup"><span data-stu-id="4449a-108">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisableDriveRedirection**</span></span>
    -   <span data-ttu-id="4449a-109">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Terminal Server \\ дисаблепринтерредиректион**</span><span class="sxs-lookup"><span data-stu-id="4449a-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server\\DisablePrinterRedirection**</span></span>

2.  <span data-ttu-id="4449a-110">Задайте для обоих ключей значение **reg \_ DWORD** 1.</span><span class="sxs-lookup"><span data-stu-id="4449a-110">Set the value of both keys to **REG\_DWORD** 1.</span></span>

 

 




