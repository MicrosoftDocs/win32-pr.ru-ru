---
description: Определите версию агента Центр обновления Windows (WUA) перед его использованием.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Определение текущей версии WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701929"
---
# <a name="determining-the-current-version-of-wua"></a><span data-ttu-id="850e6-103">Определение текущей версии WUA</span><span class="sxs-lookup"><span data-stu-id="850e6-103">Determining the Current Version of WUA</span></span>

<span data-ttu-id="850e6-104">Общие сведения об обновлении WUA, включая пошаговые инструкции по программному определению в приложении того, соответствует ли версия WUA, выполняемая на компьютере, требованиям, см. в разделе [обновление агента Центр обновления Windows](updating-the-windows-update-agent.md).</span><span class="sxs-lookup"><span data-stu-id="850e6-104">For general information on updating the WUA, including step by step instructions to programmatically determine from within your app whether the version of WUA that is running on the computer meets your needs, see [Updating the Windows Update Agent](updating-the-windows-update-agent.md).</span></span>

<span data-ttu-id="850e6-105">В версиях Windows, предшествующих Windows 7 и Windows Server 2008 R2, перед использованием необходимо определить установленную версию Центр обновления Windows Agent (WUA).</span><span class="sxs-lookup"><span data-stu-id="850e6-105">On versions of Windows prior to Windows 7 and Windows Server 2008 R2, you should determine the installed version of Windows Update Agent (WUA) before you use it.</span></span> <span data-ttu-id="850e6-106">Текущая версия WUA определяется версией Wuaueng.dll, которая выполняется в \\ подкаталоге system32 текущей установки Windows.</span><span class="sxs-lookup"><span data-stu-id="850e6-106">The current version of WUA is determined by the version of the Wuaueng.dll that is running in the \\System32 subdirectory of the current Windows installation.</span></span> <span data-ttu-id="850e6-107">Если версия Wuaueng.dll имеет версию 5.4.3790.1000 или более позднюю, то будет установлен WUA.</span><span class="sxs-lookup"><span data-stu-id="850e6-107">If the version of Wuaueng.dll is version 5.4.3790.1000 or a later version, WUA is installed.</span></span> <span data-ttu-id="850e6-108">Версия, более ранняя чем 5.4.3790.1000, указывает, что установлены службы Software Update Services (SUS) 1,0.</span><span class="sxs-lookup"><span data-stu-id="850e6-108">A version that is earlier than 5.4.3790.1000 indicates that Software Update Services (SUS) 1.0 is installed.</span></span>

<span data-ttu-id="850e6-109">При обращении к службе SUS 1,0 с помощью API WUA возвращается **значение HRESULT** службы WU \_ E \_ Au \_ легацисервер.</span><span class="sxs-lookup"><span data-stu-id="850e6-109">When a call is made to SUS 1.0 by using the WUA API, an **HRESULT** of WU\_E\_AU\_LEGACYSERVER is returned.</span></span>

<span data-ttu-id="850e6-110">Можно также использовать метод [**ивиндовсупдатеажентинфо::-info**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) для получения текущей версии файла Wuapi.dll, которая выполняется на компьютере.</span><span class="sxs-lookup"><span data-stu-id="850e6-110">You can also use the [**IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) method to retrieve the current file version of Wuapi.dll that is running on a computer.</span></span> <span data-ttu-id="850e6-111">Интерфейс [**ивиндовсупдатеажентинфо**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) не поддерживается в WUA 1,0.</span><span class="sxs-lookup"><span data-stu-id="850e6-111">The [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) interface is not supported in WUA 1.0.</span></span>
