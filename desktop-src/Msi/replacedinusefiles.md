---
description: Свойство Реплацединусефилес задается, если программа установки записывает файл, который используется.
ms.assetid: cef7d36e-c721-4d47-beaa-53e6749334b6
title: Реплацединусефилес, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d6826f1db2ec1844234cf32f1137e43c89528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652077"
---
# <a name="replacedinusefiles-property"></a><span data-ttu-id="e1b18-103">Реплацединусефилес, свойство</span><span class="sxs-lookup"><span data-stu-id="e1b18-103">ReplacedInUseFiles property</span></span>

<span data-ttu-id="e1b18-104">Свойство **реплацединусефилес** задается, если программа установки записывает файл, который используется.</span><span class="sxs-lookup"><span data-stu-id="e1b18-104">The **ReplacedInUseFiles** property is set if the installer writes over a file that is being held in use.</span></span> <span data-ttu-id="e1b18-105">Это свойство используется настраиваемыми действиями для обнаружения необходимости перезагрузки для завершения установки.</span><span class="sxs-lookup"><span data-stu-id="e1b18-105">This property is used by custom actions to detect that a reboot is required to complete the installation.</span></span>

<span data-ttu-id="e1b18-106">Задается во время действий [инсталлексекуте](installexecute-action.md) и [функции InstallFinalize](installfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b18-106">Set during the [InstallExecute](installexecute-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b18-107">Требования</span><span class="sxs-lookup"><span data-stu-id="e1b18-107">Requirements</span></span>



| <span data-ttu-id="e1b18-108">Требование</span><span class="sxs-lookup"><span data-stu-id="e1b18-108">Requirement</span></span> | <span data-ttu-id="e1b18-109">Значение</span><span class="sxs-lookup"><span data-stu-id="e1b18-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b18-110">Версия</span><span class="sxs-lookup"><span data-stu-id="e1b18-110">Version</span></span><br/> | <span data-ttu-id="e1b18-111">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1b18-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e1b18-112">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1b18-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e1b18-113">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e1b18-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e1b18-114">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e1b18-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1b18-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e1b18-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b18-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="e1b18-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




