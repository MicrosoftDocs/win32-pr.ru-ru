---
description: Свойство РУТДРИВЕ указывает диск по умолчанию для целевого каталога установки.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: РУТДРИВЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675188"
---
# <a name="rootdrive-property"></a><span data-ttu-id="e3d00-103">РУТДРИВЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="e3d00-103">ROOTDRIVE property</span></span>

<span data-ttu-id="e3d00-104">Свойство **рутдриве** указывает диск по умолчанию для целевого каталога установки.</span><span class="sxs-lookup"><span data-stu-id="e3d00-104">The **ROOTDRIVE** property specifies the default drive for the destination directory of the installation.</span></span> <span data-ttu-id="e3d00-105">Если столбец каталога в [таблице Directory](directory-table.md) указывает корневой каталог назначения по имени свойства, которое не определено, установщик использует значение свойства **рутдриве** для разрешения пути к целевому каталогу.</span><span class="sxs-lookup"><span data-stu-id="e3d00-105">If the Directory column of the [Directory table](directory-table.md) indicates the root destination directory by a property name that is undefined, the installer uses the value of the **ROOTDRIVE** property to resolve the path to the destination directory.</span></span>

<span data-ttu-id="e3d00-106">Если **рутдриве** не задан в командной строке или создан в [таблице свойств](property-table.md), установщик устанавливает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e3d00-106">If **ROOTDRIVE** is not set at a command line or authored into the [Property table](property-table.md), the installer sets this property.</span></span> <span data-ttu-id="e3d00-107">Во время [административной установки](administrative-installation.md) установщик устанавливает **рутдриве** в первый подключенный сетевой диск, который может быть записан в.</span><span class="sxs-lookup"><span data-stu-id="e3d00-107">During an [administrative installation](administrative-installation.md) the installer sets **ROOTDRIVE** to the first connected network drive it finds that can be written to.</span></span> <span data-ttu-id="e3d00-108">Если это не административная установка или если установщик не может найти сетевые диски, установщик устанавливает **рутдриве** на локальный диск, на который может быть помещено наибольшее свободное пространство.</span><span class="sxs-lookup"><span data-stu-id="e3d00-108">If it is not an administrative installation, or if the installer can find no network drives, the installer sets **ROOTDRIVE** to the local drive that can be written to having the most free space.</span></span>

<span data-ttu-id="e3d00-109">Значение этого свойства должно заканчиваться на " \\ ".</span><span class="sxs-lookup"><span data-stu-id="e3d00-109">The value for this property must end with '\\'.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d00-110">Требования</span><span class="sxs-lookup"><span data-stu-id="e3d00-110">Requirements</span></span>



| <span data-ttu-id="e3d00-111">Требование</span><span class="sxs-lookup"><span data-stu-id="e3d00-111">Requirement</span></span> | <span data-ttu-id="e3d00-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e3d00-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d00-113">Версия</span><span class="sxs-lookup"><span data-stu-id="e3d00-113">Version</span></span><br/> | <span data-ttu-id="e3d00-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e3d00-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e3d00-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e3d00-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e3d00-116">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e3d00-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e3d00-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="e3d00-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e3d00-118">См. также</span><span class="sxs-lookup"><span data-stu-id="e3d00-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d00-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="e3d00-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




