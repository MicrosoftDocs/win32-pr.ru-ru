---
description: Свойство TARGETDIR указывает корневой каталог назначения для установки.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: TARGETDIR, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675840"
---
# <a name="targetdir-property"></a><span data-ttu-id="7772f-103">TARGETDIR, свойство</span><span class="sxs-lookup"><span data-stu-id="7772f-103">TARGETDIR property</span></span>

<span data-ttu-id="7772f-104">Свойство **targetDir** указывает корневой каталог назначения для установки.</span><span class="sxs-lookup"><span data-stu-id="7772f-104">The **TARGETDIR** property specifies the root destination directory for the installation.</span></span> <span data-ttu-id="7772f-105">Параметр **targetDir** должен быть именем одного корня в таблице [Directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="7772f-105">**TARGETDIR** must be the name of one root in the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="7772f-106">Может существовать только один корневой каталог назначения.</span><span class="sxs-lookup"><span data-stu-id="7772f-106">There may be only a single root destination directory.</span></span> <span data-ttu-id="7772f-107">Во время [административной установки](administrative-installation.md) это свойство указывает расположение для копирования установочного пакета.</span><span class="sxs-lookup"><span data-stu-id="7772f-107">During an [administrative installation](administrative-installation.md) this property specifies the location to copy the installation package.</span></span> <span data-ttu-id="7772f-108">Во время установки без администрирования это свойство указывает корневой каталог назначения.</span><span class="sxs-lookup"><span data-stu-id="7772f-108">During a non-administrative installation this property specifies the root destination directory.</span></span>

<span data-ttu-id="7772f-109">Чтобы указать корневой каталог назначения, задайте для столбца каталога таблицы Directory свойство **targetDir** , а для столбца дефаултдир — значение свойства [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="7772f-109">To specify the root destination directory, set the Directory column of the Directory table to the **TARGETDIR** property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="7772f-110">Если определено свойство **targetDir** , целевой каталог разрешается в значение свойства.</span><span class="sxs-lookup"><span data-stu-id="7772f-110">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="7772f-111">Если свойство **targetDir** не определено, для разрешения пути используется свойство [**рутдриве**](rootdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="7772f-111">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span> <span data-ttu-id="7772f-112">Дополнительные сведения об использовании свойства **targetDir** см. в разделе [Использование таблицы Directory](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="7772f-112">For more information about using the **TARGETDIR** property, see [Using the Directory Table](using-the-directory-table.md).</span></span>

<span data-ttu-id="7772f-113">Обратите внимание, что значение свойства **targetDir** обычно задается в командной строке или через пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7772f-113">Note that the value of the **TARGETDIR** property is typically set at the command line or through a user interface.</span></span> <span data-ttu-id="7772f-114">Установка параметра **targetDir** путем создания пути к [таблице свойств](property-table.md) не рекомендуется, так как компьютеры отличаются в настройке локального диска.</span><span class="sxs-lookup"><span data-stu-id="7772f-114">Setting **TARGETDIR** by authoring a path into the [Property table](property-table.md) is not recommended because computers differ in the set up of the local drive.</span></span>

<span data-ttu-id="7772f-115">Дополнительные сведения об изменении TARGETDIR во время установки см. в статье [изменение целевого расположения каталога](changing-the-target-location-for-a-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="7772f-115">For more information on how to change TARGETDIR during an installation see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="7772f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7772f-116">Requirements</span></span>



| <span data-ttu-id="7772f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7772f-117">Requirement</span></span> | <span data-ttu-id="7772f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7772f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7772f-119">Версия</span><span class="sxs-lookup"><span data-stu-id="7772f-119">Version</span></span><br/> | <span data-ttu-id="7772f-120">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7772f-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7772f-121">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7772f-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7772f-122">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7772f-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7772f-123">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="7772f-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7772f-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7772f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7772f-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="7772f-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




