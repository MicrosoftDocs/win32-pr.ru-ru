---
description: Объект Product представляет уникальный экземпляр продукта, который объявлен, установлен или неизвестен. Экземпляр объекта можно создать с помощью свойства Product, например &\# 0034; Виндовсинсталлер. Installer. Product (ProductCode, в отношении контекста) &\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Объект Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651756"
---
# <a name="product-object"></a><span data-ttu-id="36784-103">Объект Product</span><span class="sxs-lookup"><span data-stu-id="36784-103">Product object</span></span>

<span data-ttu-id="36784-104">Объект **Product** представляет уникальный экземпляр продукта, который объявлен, установлен или неизвестен.</span><span class="sxs-lookup"><span data-stu-id="36784-104">The **Product** object represents a unique instance of a product that is either advertised, installed or unknown.</span></span>

<span data-ttu-id="36784-105">Экземпляр объекта можно создать с помощью свойства **Product** в виде "Виндовсинсталлер. Installer. Product (*ProductCode* *, с* учетом *контекста*)".</span><span class="sxs-lookup"><span data-stu-id="36784-105">The object can be instantiated with the **Product** property as "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)".</span></span> <span data-ttu-id="36784-106">Для контекста на компьютер значение "со значением *" должно быть* равно null.</span><span class="sxs-lookup"><span data-stu-id="36784-106">*UserSid* must be NULL for per-machine context.</span></span> <span data-ttu-id="36784-107">*Для указанного* текущего пользователя значение «со значением» может быть равно null, если контекст не относится к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="36784-107">*UserSid* can be null to specified current user, when context is not per-machine.</span></span> <span data-ttu-id="36784-108">Требуются параметры *ProductCode* и *context* .</span><span class="sxs-lookup"><span data-stu-id="36784-108">*ProductCode* and *Context* parameters are required.</span></span>

## <a name="members"></a><span data-ttu-id="36784-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="36784-109">Members</span></span>

<span data-ttu-id="36784-110">Объект **Product** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="36784-110">The **Product** object has these types of members:</span></span>

-   [<span data-ttu-id="36784-111">Методы</span><span class="sxs-lookup"><span data-stu-id="36784-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="36784-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="36784-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="36784-113">Методы</span><span class="sxs-lookup"><span data-stu-id="36784-113">Methods</span></span>

<span data-ttu-id="36784-114">Объект **Product** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="36784-114">The **Product** object has these methods.</span></span>



| <span data-ttu-id="36784-115">Метод</span><span class="sxs-lookup"><span data-stu-id="36784-115">Method</span></span>                                                                 | <span data-ttu-id="36784-116">Описание</span><span class="sxs-lookup"><span data-stu-id="36784-116">Description</span></span>                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36784-117">**саурцелистаддмедиадиск**</span><span class="sxs-lookup"><span data-stu-id="36784-117">**SourceListAddMediaDisk**</span></span>](product-sourcelistaddmediadisk.md)       | <span data-ttu-id="36784-118">Добавьте диск в набор зарегистрированных дисков.</span><span class="sxs-lookup"><span data-stu-id="36784-118">Add a disk to the set of registered disks.</span></span><br/>                                                              |
| [<span data-ttu-id="36784-119">**саурцелистаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="36784-119">**SourceListAddSource**</span></span>](product-sourcelistaddsource.md)             | <span data-ttu-id="36784-120">Добавьте сеть или URL-адрес в исходный список.</span><span class="sxs-lookup"><span data-stu-id="36784-120">Add a network or URL source to the source list.</span></span><br/>                                                         |
| [<span data-ttu-id="36784-121">**саурцелистклеаралл**</span><span class="sxs-lookup"><span data-stu-id="36784-121">**SourceListClearAll**</span></span>](product-sourcelistclearall.md)               | <span data-ttu-id="36784-122">Очищает полный исходный список указанного типа источников.</span><span class="sxs-lookup"><span data-stu-id="36784-122">Clears the complete source list of the specified type of sources.</span></span><br/>                                       |
| [<span data-ttu-id="36784-123">**саурцелистклеармедиадиск**</span><span class="sxs-lookup"><span data-stu-id="36784-123">**SourceListClearMediaDisk**</span></span>](product-sourcelistclearmediadisk.md)   | <span data-ttu-id="36784-124">Удалить диск из набора зарегистрированных дисков из списка источников.</span><span class="sxs-lookup"><span data-stu-id="36784-124">Remove a disk from the set of registered disks from the source list.</span></span><br/>                                    |
| [<span data-ttu-id="36784-125">**саурцелистклеарсаурце**</span><span class="sxs-lookup"><span data-stu-id="36784-125">**SourceListClearSource**</span></span>](product-sourcelistclearsource.md)         | <span data-ttu-id="36784-126">Удаление сети или источника URL-адреса из списка источников.</span><span class="sxs-lookup"><span data-stu-id="36784-126">Remove a network or URL source from the source list.</span></span><br/>                                                    |
| [<span data-ttu-id="36784-127">**саурцелистфорцересолутион**</span><span class="sxs-lookup"><span data-stu-id="36784-127">**SourceListForceResolution**</span></span>](product-sourcelistforceresolution.md) | <span data-ttu-id="36784-128">Очищает последний использованный источник.</span><span class="sxs-lookup"><span data-stu-id="36784-128">Clears the last used source.</span></span> <span data-ttu-id="36784-129">Это приводит к тому, что разрешение списка источников будет вычисляться в следующий раз, когда требуется источник.</span><span class="sxs-lookup"><span data-stu-id="36784-129">This forces a source list resolution the next time the source is required.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="36784-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="36784-130">Properties</span></span>

<span data-ttu-id="36784-131">Объект **Product** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="36784-131">The **Product** object has these properties.</span></span>



| <span data-ttu-id="36784-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="36784-132">Property</span></span>                                                      | <span data-ttu-id="36784-133">Описание</span><span class="sxs-lookup"><span data-stu-id="36784-133">Description</span></span>                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36784-134">**компонентстате**</span><span class="sxs-lookup"><span data-stu-id="36784-134">**ComponentState**</span></span>](product-componentstate.md)<br/>   | <span data-ttu-id="36784-135">Состояние указанного компонента для данного экземпляра продукта.</span><span class="sxs-lookup"><span data-stu-id="36784-135">The state of a specified component for this product instance.</span></span> <br/>                   |
| [<span data-ttu-id="36784-136">**Локального**</span><span class="sxs-lookup"><span data-stu-id="36784-136">**Context**</span></span>](product-context.md)<br/>                 | <span data-ttu-id="36784-137">Контекст этого экземпляра продукта в виде значения МСИИНСТАЛЛКОНТЕКСТ.</span><span class="sxs-lookup"><span data-stu-id="36784-137">Context of this product instance as an MSIINSTALLCONTEXT value.</span></span> <br/>                 |
| [<span data-ttu-id="36784-138">**феатурестате**</span><span class="sxs-lookup"><span data-stu-id="36784-138">**FeatureState**</span></span>](product-featurestate.md)<br/>       | <span data-ttu-id="36784-139">Состояние указанной функции для данного экземпляра продукта.</span><span class="sxs-lookup"><span data-stu-id="36784-139">The state of a specified feature for this product instance.</span></span> <br/>                     |
| [<span data-ttu-id="36784-140">**инсталлпроперти**</span><span class="sxs-lookup"><span data-stu-id="36784-140">**InstallProperty**</span></span>](product-installproperty.md)<br/> | <span data-ttu-id="36784-141">Значение указанного свойства.</span><span class="sxs-lookup"><span data-stu-id="36784-141">The value of a specified property.</span></span> <br/>                                              |
| [<span data-ttu-id="36784-142">**медиадискс**</span><span class="sxs-lookup"><span data-stu-id="36784-142">**MediaDisks**</span></span>](product-mediadisks.md)<br/>           | <span data-ttu-id="36784-143">Перечисление всех дисков мультимедиа для данного экземпляра продукта.</span><span class="sxs-lookup"><span data-stu-id="36784-143">Enumerates all the media disks for this product instance.</span></span><br/>                        |
| [<span data-ttu-id="36784-144">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="36784-144">**ProductCode**</span></span>](product-productcode.md)<br/>         | <span data-ttu-id="36784-145">Возвращает код продукта.</span><span class="sxs-lookup"><span data-stu-id="36784-145">Returns the product code.</span></span> <br/>                                                       |
| [<span data-ttu-id="36784-146">**саурцелистинфо**</span><span class="sxs-lookup"><span data-stu-id="36784-146">**SourceListInfo**</span></span>](product-sourcelistinfo.md)<br/>   | <span data-ttu-id="36784-147">Возвращает и задает свойства исходных сведений.</span><span class="sxs-lookup"><span data-stu-id="36784-147">Get and set the source information properties.</span></span> <span data-ttu-id="36784-148">Это свойство для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="36784-148">This is a read or write property.</span></span><br/> |
| [<span data-ttu-id="36784-149">**Исход**</span><span class="sxs-lookup"><span data-stu-id="36784-149">**Sources**</span></span>](product-sources.md)<br/>                 | <span data-ttu-id="36784-150">Перечисляет все источники для данного экземпляра продукта.</span><span class="sxs-lookup"><span data-stu-id="36784-150">Enumerates all the sources for this product instance.</span></span><br/>                            |
| [<span data-ttu-id="36784-151">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="36784-151">**State**</span></span>](product-state.md)<br/>                     | <span data-ttu-id="36784-152">Состояние установки продукта.</span><span class="sxs-lookup"><span data-stu-id="36784-152">Installation state of the product.</span></span><br/>                                               |
| [<span data-ttu-id="36784-153">**UserSid**</span><span class="sxs-lookup"><span data-stu-id="36784-153">**UserSid**</span></span>](product-usersid.md)<br/>                 | <span data-ttu-id="36784-154">Возвращает идентификатор SID пользователя, в котором доступна учетная запись этого экземпляра продукта.</span><span class="sxs-lookup"><span data-stu-id="36784-154">Returns the User SID, under which account this product instance is available.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="36784-155">Требования</span><span class="sxs-lookup"><span data-stu-id="36784-155">Requirements</span></span>



| <span data-ttu-id="36784-156">Требование</span><span class="sxs-lookup"><span data-stu-id="36784-156">Requirement</span></span> | <span data-ttu-id="36784-157">Значение</span><span class="sxs-lookup"><span data-stu-id="36784-157">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36784-158">Версия</span><span class="sxs-lookup"><span data-stu-id="36784-158">Version</span></span><br/> | <span data-ttu-id="36784-159">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="36784-159">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="36784-160">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36784-160">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="36784-161">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="36784-161">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="36784-162">DLL</span><span class="sxs-lookup"><span data-stu-id="36784-162">DLL</span></span><br/>     | <dl> <span data-ttu-id="36784-163"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36784-163"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="36784-164">IID</span><span class="sxs-lookup"><span data-stu-id="36784-164">IID</span></span><br/>     | <span data-ttu-id="36784-165">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="36784-165">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="36784-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36784-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36784-167">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="36784-167">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




