---
description: Установщик задает для свойства Виндовсволуме значение Volume папки Windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Виндовсволуме, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651940"
---
# <a name="windowsvolume-property"></a><span data-ttu-id="3acc0-103">Виндовсволуме, свойство</span><span class="sxs-lookup"><span data-stu-id="3acc0-103">WindowsVolume property</span></span>

<span data-ttu-id="3acc0-104">Установщик задает для свойства **виндовсволуме** значение Volume папки Windows.</span><span class="sxs-lookup"><span data-stu-id="3acc0-104">The installer sets the **WindowsVolume** property to the volume of the windows folder.</span></span> <span data-ttu-id="3acc0-105">Свойство всегда заканчивается обратной косой чертой.</span><span class="sxs-lookup"><span data-stu-id="3acc0-105">The property always ends with a backslash.</span></span> <span data-ttu-id="3acc0-106">Это можно использовать, чтобы задать расположение по умолчанию для тома, в котором находится папка Windows, поскольку свойство [**рутдриве**](rootdrive.md) не обязательно равно этому диску.</span><span class="sxs-lookup"><span data-stu-id="3acc0-106">This can be used to set the default location to the volume the Windows folder is on because the [**ROOTDRIVE**](rootdrive.md) property does not necessarily equal this drive.</span></span>

## <a name="remarks"></a><span data-ttu-id="3acc0-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3acc0-107">Remarks</span></span>

<span data-ttu-id="3acc0-108">Не используйте свойство **виндовсволуме** в столбце Directory таблицы [Directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="3acc0-108">Do not use the **WindowsVolume** property in the Directory column of the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="3acc0-109">Свойство [**виндовсфолдер**](windowsfolder.md) содержит путь к папке Windows.</span><span class="sxs-lookup"><span data-stu-id="3acc0-109">The [**WindowsFolder**](windowsfolder.md) property contains the path to the Windows folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="3acc0-110">Требования</span><span class="sxs-lookup"><span data-stu-id="3acc0-110">Requirements</span></span>



| <span data-ttu-id="3acc0-111">Требование</span><span class="sxs-lookup"><span data-stu-id="3acc0-111">Requirement</span></span> | <span data-ttu-id="3acc0-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3acc0-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3acc0-113">Версия</span><span class="sxs-lookup"><span data-stu-id="3acc0-113">Version</span></span><br/> | <span data-ttu-id="3acc0-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3acc0-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3acc0-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3acc0-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3acc0-116">Установщик Windows в Windows Server 2003 или Windows XP ознакомьтесь с [требованиями к установщик Windows Run-Time](windows-installer-portal.md) , чтобы получить сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии.</span><span class="sxs-lookup"><span data-stu-id="3acc0-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3acc0-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3acc0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3acc0-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="3acc0-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




