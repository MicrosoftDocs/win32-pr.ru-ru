---
description: Объект Patch представляет уникальный экземпляр зарегистрированного или примененного исправления. Экземпляр объекта можно создать с помощью свойства Patch, как &\# 0034; Виндовсинсталлер. Installer. patch (Патчкоде, ProductCode,, контекст) &\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Объект Patch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651645"
---
# <a name="patch-object"></a><span data-ttu-id="ec637-103">Объект Patch</span><span class="sxs-lookup"><span data-stu-id="ec637-103">Patch object</span></span>

<span data-ttu-id="ec637-104">Объект **Patch** представляет уникальный экземпляр зарегистрированного или примененного исправления.</span><span class="sxs-lookup"><span data-stu-id="ec637-104">The **Patch** object represents a unique instance of a patch that has been registered or applied.</span></span>

<span data-ttu-id="ec637-105">Экземпляр объекта можно создать с помощью свойства **Patch** как «Виндовсинсталлер. Installer. patch (*патчкоде*, *ProductCode*,) ». </span><span class="sxs-lookup"><span data-stu-id="ec637-105">The object can be instantiated with the **Patch** property as "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="ec637-106">Для контекста компьютера параметром « *значение» должен* быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="ec637-106">For a machine context, the *UserSid* parameter must be an empty string.</span></span> <span data-ttu-id="ec637-107">Значение *ProductCode* может быть пустой строкой для исправлений, которые зарегистрированы только и еще не применены к какому либо продукту.</span><span class="sxs-lookup"><span data-stu-id="ec637-107">The *ProductCode* can be set to an empty string for patches that are registered only and not yet applied to any product.</span></span> <span data-ttu-id="ec637-108">Значение *ProductCode* может быть пустой строкой при чтении или обновлении сведений списка источников исправления.</span><span class="sxs-lookup"><span data-stu-id="ec637-108">The *ProductCode* can be set to an empty string when only reading or updating a patch's source list information.</span></span>

## <a name="members"></a><span data-ttu-id="ec637-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="ec637-109">Members</span></span>

<span data-ttu-id="ec637-110">Объект **Patch** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ec637-110">The **Patch** object has these types of members:</span></span>

-   [<span data-ttu-id="ec637-111">Методы</span><span class="sxs-lookup"><span data-stu-id="ec637-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ec637-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec637-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ec637-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ec637-113">Methods</span></span>

<span data-ttu-id="ec637-114">Объект **Patch** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ec637-114">The **Patch** object has these methods.</span></span>



| <span data-ttu-id="ec637-115">Метод</span><span class="sxs-lookup"><span data-stu-id="ec637-115">Method</span></span>                                                               | <span data-ttu-id="ec637-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ec637-116">Description</span></span>                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec637-117">**саурцелистаддмедиадиск**</span><span class="sxs-lookup"><span data-stu-id="ec637-117">**SourceListAddMediaDisk**</span></span>](patch-sourcelistaddmediadisk.md)       | <span data-ttu-id="ec637-118">Добавьте диск в набор зарегистрированных дисков.</span><span class="sxs-lookup"><span data-stu-id="ec637-118">Add a disk to the set of registered disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="ec637-119">**саурцелистаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="ec637-119">**SourceListAddSource**</span></span>](patch-sourcelistaddsource.md)             | <span data-ttu-id="ec637-120">Добавьте сеть или URL-адрес в исходный список.</span><span class="sxs-lookup"><span data-stu-id="ec637-120">Add a network or URL source to the source list.</span></span> <br/>                                                                             |
| [<span data-ttu-id="ec637-121">**саурцелистклеаралл**</span><span class="sxs-lookup"><span data-stu-id="ec637-121">**SourceListClearAll**</span></span>](patch-sourcelistclearall.md)               | <span data-ttu-id="ec637-122">Очищает полный исходный список указанного типа источников.</span><span class="sxs-lookup"><span data-stu-id="ec637-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                                            |
| [<span data-ttu-id="ec637-123">**саурцелистклеармедиадиск**</span><span class="sxs-lookup"><span data-stu-id="ec637-123">**SourceListClearMediaDisk**</span></span>](patch-sourcelistclearmediadisk.md)   | <span data-ttu-id="ec637-124">Удалить диск из набора зарегистрированных дисков из списка источников.</span><span class="sxs-lookup"><span data-stu-id="ec637-124">Remove a disk from the set of registered disks from the source list.</span></span> <br/>                                                        |
| [<span data-ttu-id="ec637-125">**саурцелистклеарсаурце**</span><span class="sxs-lookup"><span data-stu-id="ec637-125">**SourceListClearSource**</span></span>](patch-sourcelistclearsource.md)         | <span data-ttu-id="ec637-126">Удаление сети или источника URL-адреса из списка источников.</span><span class="sxs-lookup"><span data-stu-id="ec637-126">Remove a network or URL source from the source list.</span></span><br/>                                                                         |
| [<span data-ttu-id="ec637-127">**саурцелистфорцересолутион**</span><span class="sxs-lookup"><span data-stu-id="ec637-127">**SourceListForceResolution**</span></span>](patch-sourcelistforceresolution.md) | <span data-ttu-id="ec637-128">Удаляет последний использованный источник из исходного списка.</span><span class="sxs-lookup"><span data-stu-id="ec637-128">Clears the last used source from the source list.</span></span> <span data-ttu-id="ec637-129">Это приводит к тому, что разрешение списка источников будет вычисляться в следующий раз, когда требуется источник.</span><span class="sxs-lookup"><span data-stu-id="ec637-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ec637-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec637-130">Properties</span></span>

<span data-ttu-id="ec637-131">Объект **Patch** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="ec637-131">The **Patch** object has these properties.</span></span>



| <span data-ttu-id="ec637-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="ec637-132">Property</span></span>                                                  | <span data-ttu-id="ec637-133">Описание</span><span class="sxs-lookup"><span data-stu-id="ec637-133">Description</span></span>                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec637-134">**Контекст**</span><span class="sxs-lookup"><span data-stu-id="ec637-134">**Context**</span></span>](patch-context.md)<br/>               | <span data-ttu-id="ec637-135">Контекстом этого экземпляра Patch является значение МСИИНСТАЛЛКОНТЕКСТ.</span><span class="sxs-lookup"><span data-stu-id="ec637-135">Context of this patch instance is an MSIINSTALLCONTEXT value.</span></span><br/>                                   |
| [<span data-ttu-id="ec637-136">**медиадискс**</span><span class="sxs-lookup"><span data-stu-id="ec637-136">**MediaDisks**</span></span>](patch-mediadisks.md)<br/>         | <span data-ttu-id="ec637-137">Перечисление всех дисков мультимедиа для данного экземпляра исправления.</span><span class="sxs-lookup"><span data-stu-id="ec637-137">Enumerates all the media disks for this patch instance.</span></span><br/>                                         |
| [<span data-ttu-id="ec637-138">**патчкоде**</span><span class="sxs-lookup"><span data-stu-id="ec637-138">**PatchCode**</span></span>](patch-patchcode.md)<br/>           | <span data-ttu-id="ec637-139">Возвращает код исправления.</span><span class="sxs-lookup"><span data-stu-id="ec637-139">Returns the patch code.</span></span><br/>                                                                         |
| [<span data-ttu-id="ec637-140">**патчпроперти**</span><span class="sxs-lookup"><span data-stu-id="ec637-140">**PatchProperty**</span></span>](patch-patchproperty.md)<br/>   | <span data-ttu-id="ec637-141">Возвращает сведения о свойстве конкретного исправления, примененного к конкретному экземпляру продукта.</span><span class="sxs-lookup"><span data-stu-id="ec637-141">Gets property information about a specific patch applied to a specific instance of the product.</span></span><br/> |
| [<span data-ttu-id="ec637-142">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="ec637-142">**ProductCode**</span></span>](patch-productcode.md)<br/>       | <span data-ttu-id="ec637-143">Возвращает код продукта.</span><span class="sxs-lookup"><span data-stu-id="ec637-143">Returns the product code.</span></span><br/>                                                                       |
| [<span data-ttu-id="ec637-144">**саурцелистинфо**</span><span class="sxs-lookup"><span data-stu-id="ec637-144">**SourceListInfo**</span></span>](patch-sourcelistinfo.md)<br/> | <span data-ttu-id="ec637-145">Возвращает и задает свойства сведений об источнике.</span><span class="sxs-lookup"><span data-stu-id="ec637-145">Gets and sets the source information properties.</span></span> <span data-ttu-id="ec637-146">Это свойство для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="ec637-146">This is a read or write property.</span></span><br/>              |
| [<span data-ttu-id="ec637-147">**Исход**</span><span class="sxs-lookup"><span data-stu-id="ec637-147">**Sources**</span></span>](patch-sources.md)<br/>               | <span data-ttu-id="ec637-148">Перечисляет все источники для данного экземпляра patch.</span><span class="sxs-lookup"><span data-stu-id="ec637-148">Enumerates all the sources for this patch instance.</span></span><br/>                                             |
| [<span data-ttu-id="ec637-149">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ec637-149">**State**</span></span>](patch-state.md)<br/>                   | <span data-ttu-id="ec637-150">Состояние установки исправления.</span><span class="sxs-lookup"><span data-stu-id="ec637-150">Installation state of the patch.</span></span><br/>                                                                |
| [<span data-ttu-id="ec637-151">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="ec637-151">**UserSid**</span></span>](patch-usersid.md)<br/>               | <span data-ttu-id="ec637-152">Возвращает идентификатор SID пользователя в учетной записи, доступной для данного экземпляра patch.</span><span class="sxs-lookup"><span data-stu-id="ec637-152">Returns the User SID, under the account this patch instance is available.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="ec637-153">Требования</span><span class="sxs-lookup"><span data-stu-id="ec637-153">Requirements</span></span>



| <span data-ttu-id="ec637-154">Требование</span><span class="sxs-lookup"><span data-stu-id="ec637-154">Requirement</span></span> | <span data-ttu-id="ec637-155">Значение</span><span class="sxs-lookup"><span data-stu-id="ec637-155">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec637-156">Версия</span><span class="sxs-lookup"><span data-stu-id="ec637-156">Version</span></span><br/> | <span data-ttu-id="ec637-157">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ec637-157">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ec637-158">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ec637-158">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ec637-159">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ec637-159">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="ec637-160">DLL</span><span class="sxs-lookup"><span data-stu-id="ec637-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="ec637-161"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec637-161"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="ec637-162">IID</span><span class="sxs-lookup"><span data-stu-id="ec637-162">IID</span></span><br/>     | <span data-ttu-id="ec637-163">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ec637-163">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="ec637-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec637-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec637-165">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="ec637-165">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




