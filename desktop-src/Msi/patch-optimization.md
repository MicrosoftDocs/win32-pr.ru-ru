---
description: Установщик Windows можете оптимизировать исправления, чтобы сократить время, необходимое для применения исправлений к установленным приложениям.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Оптимизация исправления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898846"
---
# <a name="patch-optimization"></a><span data-ttu-id="75233-103">Оптимизация исправления</span><span class="sxs-lookup"><span data-stu-id="75233-103">Patch Optimization</span></span>

<span data-ttu-id="75233-104">Установщик Windows можете оптимизировать исправления, чтобы сократить время, необходимое для применения исправлений к установленным приложениям.</span><span class="sxs-lookup"><span data-stu-id="75233-104">Windows Installer can optimize patching to reduce the time that is required to apply patches to installed applications.</span></span>

<span data-ttu-id="75233-105">**Установщик Windows 2,0:** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="75233-105">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="75233-106">Для версий установщик Windows, выпущенных до установщик Windows 3,0, установка исправлений запускает полное восстановление приложения, что может занять значительно больше времени.</span><span class="sxs-lookup"><span data-stu-id="75233-106">For versions of Windows Installer released before Windows Installer 3.0, patching runs a complete repair installation of the application, which can take significantly more time.</span></span>

<span data-ttu-id="75233-107">**Установщик Windows 3,0 и более поздних версий:** Процесс исправления изменяет только те части приложения, которые были изменены с помощью исправления.</span><span class="sxs-lookup"><span data-stu-id="75233-107">**Windows Installer 3.0 and later:** The patching process only changes the parts of an application that are modified by a patch.</span></span>

<span data-ttu-id="75233-108">**Установщик Windows 3,1 и более поздних версий:** Начиная с установщик Windows 3,1, оптимизация исправления требует, чтобы для всех исправлений в транзакции свойство Оптимизединсталлмоде было установлено в 1 (одно) в [таблице мсипатчметадата](msipatchmetadata-table.md).</span><span class="sxs-lookup"><span data-stu-id="75233-108">**Windows Installer 3.1 and later:** Beginning with Windows Installer 3.1, patch optimization requires that all patches in the transaction have the OptimizedInstallMode property set to 1 (one) in the [MsiPatchMetadata Table](msipatchmetadata-table.md).</span></span>

<span data-ttu-id="75233-109">Если исправление изменяет только следующие таблицы, установщик Windows 3,0 или более поздней версии пропускает действия, связанные со всеми другими таблицами, даже если эти действия перечислены в таблицах последовательности исходного пакета установки приложения (MSI-файла).</span><span class="sxs-lookup"><span data-stu-id="75233-109">If a patch only modifies the following tables, Windows Installer 3.0 or later skips the actions that are associated with all the other tables, even if those actions are listed in the sequence tables of the original application installation package (.msi file).</span></span>

-   [<span data-ttu-id="75233-110">админексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="75233-110">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="75233-111">админуисекуенце</span><span class="sxs-lookup"><span data-stu-id="75233-111">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="75233-112">Condition</span><span class="sxs-lookup"><span data-stu-id="75233-112">Condition</span></span>](condition-table.md)
-   [<span data-ttu-id="75233-113">CustomAction</span><span class="sxs-lookup"><span data-stu-id="75233-113">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="75233-114">Файл</span><span class="sxs-lookup"><span data-stu-id="75233-114">File</span></span>](file-table.md)
-   [<span data-ttu-id="75233-115">филесфпкаталог</span><span class="sxs-lookup"><span data-stu-id="75233-115">FileSFPCatalog</span></span>](filesfpcatalog-table.md)
-   [<span data-ttu-id="75233-116">инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="75233-116">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="75233-117">инсталлуисекуенце</span><span class="sxs-lookup"><span data-stu-id="75233-117">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="75233-118">Носитель</span><span class="sxs-lookup"><span data-stu-id="75233-118">Media</span></span>](media-table.md)
-   [<span data-ttu-id="75233-119">MoveFile</span><span class="sxs-lookup"><span data-stu-id="75233-119">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="75233-120">мсиассембли</span><span class="sxs-lookup"><span data-stu-id="75233-120">MsiAssembly</span></span>](msiassembly-table.md)
-   [<span data-ttu-id="75233-121">мсидигиталцертификате</span><span class="sxs-lookup"><span data-stu-id="75233-121">MsiDigitalCertificate</span></span>](msidigitalcertificate-table.md)
-   [<span data-ttu-id="75233-122">мсидигиталсигнатуре</span><span class="sxs-lookup"><span data-stu-id="75233-122">MsiDigitalSignature</span></span>](msidigitalsignature-table.md)
-   [<span data-ttu-id="75233-123">мсифилехаш</span><span class="sxs-lookup"><span data-stu-id="75233-123">MsiFileHash</span></span>](msifilehash-table.md)
-   [<span data-ttu-id="75233-124">мсипатчхеадерс</span><span class="sxs-lookup"><span data-stu-id="75233-124">MsiPatchHeaders</span></span>](msipatchheaders-table.md)
-   [<span data-ttu-id="75233-125">Обновление</span><span class="sxs-lookup"><span data-stu-id="75233-125">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="75233-126">патчпаккаже</span><span class="sxs-lookup"><span data-stu-id="75233-126">PatchPackage</span></span>](patchpackage-table.md)
-   [<span data-ttu-id="75233-127">Свойство</span><span class="sxs-lookup"><span data-stu-id="75233-127">Property</span></span>](property-table.md)
-   [<span data-ttu-id="75233-128">Реестр</span><span class="sxs-lookup"><span data-stu-id="75233-128">Registry</span></span>](registry-table.md)
-   [<span data-ttu-id="75233-129">сфпкаталог</span><span class="sxs-lookup"><span data-stu-id="75233-129">SFPCatalog</span></span>](sfpcatalog-table.md)
-   [<span data-ttu-id="75233-130">Экспорт Typelib</span><span class="sxs-lookup"><span data-stu-id="75233-130">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="75233-131">\_Столбце</span><span class="sxs-lookup"><span data-stu-id="75233-131">\_Columns</span></span>](-columns-table.md)
-   [<span data-ttu-id="75233-132">\_Хранилищах</span><span class="sxs-lookup"><span data-stu-id="75233-132">\_Storages</span></span>](-storages-table.md)
-   [<span data-ttu-id="75233-133">\_Потоки</span><span class="sxs-lookup"><span data-stu-id="75233-133">\_Streams</span></span>](-streams-table.md)
-   [<span data-ttu-id="75233-134">\_Таблицы</span><span class="sxs-lookup"><span data-stu-id="75233-134">\_Tables</span></span>](-tables-table.md)
-   [<span data-ttu-id="75233-135">\_Таблица переformview</span><span class="sxs-lookup"><span data-stu-id="75233-135">\_TransformView Table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="75233-136">\_Проверка</span><span class="sxs-lookup"><span data-stu-id="75233-136">\_Validation</span></span>](-validation-table.md)

<span data-ttu-id="75233-137">Чтобы отключить параметр оптимизации исправлений, используйте политику [дисаблефливеигхтпатчинг](disableflyweightpatching.md) .</span><span class="sxs-lookup"><span data-stu-id="75233-137">To turn off the patch optimization option, use the [DisableFlyWeightPatching](disableflyweightpatching.md) policy.</span></span>

 

 



