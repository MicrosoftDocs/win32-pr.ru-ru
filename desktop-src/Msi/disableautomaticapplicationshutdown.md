---
description: Если для этой системной политики на уровне компьютера задано значение 1 (один), установщик Windows не взаимодействует с диспетчером перезапуска, но будет использовать диалоговое окно Филесинусе. Если для этой системной политики на уровне компьютера задано значение 2 (два), установщик Windows использует диалоговое окно Филесинусе.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: дисаблеаутоматикаппликатионшутдовн
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662791"
---
# <a name="disableautomaticapplicationshutdown"></a><span data-ttu-id="a95d4-103">дисаблеаутоматикаппликатионшутдовн</span><span class="sxs-lookup"><span data-stu-id="a95d4-103">DisableAutomaticApplicationShutdown</span></span>

<span data-ttu-id="a95d4-104">Если для этой системной политики на уровне компьютера задано значение 1 (один), установщик Windows не взаимодействует с [диспетчером перезапуска](/windows/desktop/RstMgr/restart-manager-portal), но будет использовать [диалоговое окно филесинусе](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="a95d4-104">If this per-machine system policy is set to 1 (one), Windows Installer does not interact with [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal), but it will use the [FilesInUse Dialog](filesinuse-dialog.md).</span></span>

<span data-ttu-id="a95d4-105">Если для этой системной политики на компьютере задано значение 2 (два), установщик Windows использует [диалоговое окно филесинусе](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="a95d4-105">If this per-machine system policy is set to 2 (two), Windows Installer uses the [FilesInUse Dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="a95d4-106">Этот параметр отключает попытки [диспетчера](/windows/desktop/RstMgr/restart-manager-portal) перезапуска по устранению перезапусков при установке пакета установщик Windows, который не был создан для использования диспетчера перезапуска.</span><span class="sxs-lookup"><span data-stu-id="a95d4-106">This setting disables attempts by the [Restart Manager](/windows/desktop/RstMgr/restart-manager-portal) to mitigate restarts when installing a Windows Installer package that has not been authored to use the Restart Manager.</span></span> <span data-ttu-id="a95d4-107">Установщик по-прежнему использует диспетчер перезапуска для обнаружения файлов, используемых приложениями.</span><span class="sxs-lookup"><span data-stu-id="a95d4-107">The installer still uses the Restart Manager to detect files in use by applications.</span></span>

<span data-ttu-id="a95d4-108">Политика Дисаблеаутоматикаппликатионшутдовн доступна начиная с установщик Windows версии 4,0 в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a95d4-108">The DisableAutomaticApplicationShutdown policy is available beginning with Windows Installer version 4.0 on Windows Vista.</span></span>

## <a name="registry-key"></a><span data-ttu-id="a95d4-109">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="a95d4-109">Registry Key</span></span>

<span data-ttu-id="a95d4-110">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="a95d4-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="a95d4-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a95d4-111">Data Type</span></span>

<span data-ttu-id="a95d4-112">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a95d4-112">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="a95d4-113">См. также</span><span class="sxs-lookup"><span data-stu-id="a95d4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a95d4-114">**мсирестартманажерконтрол**</span><span class="sxs-lookup"><span data-stu-id="a95d4-114">**MSIRESTARTMANAGERCONTROL**</span></span>](msirestartmanagercontrol.md)
</dt> <dt>

[<span data-ttu-id="a95d4-115">Не поддерживается в установщик Windows 3,1 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="a95d4-115">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
