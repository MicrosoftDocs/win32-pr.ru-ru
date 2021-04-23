---
description: Свойство Саурцелистинфо объекта Product получает и задает свойства исходных сведений для продукта. Это свойство вызывает Мсисаурцелистжетинфо или Мсисаурцелистсетинфо. Это свойство для чтения или записи.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Свойство Product. Саурцелистинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652082"
---
# <a name="productsourcelistinfo-property"></a><span data-ttu-id="c927e-105">Свойство Product. Саурцелистинфо</span><span class="sxs-lookup"><span data-stu-id="c927e-105">Product.SourceListInfo property</span></span>

<span data-ttu-id="c927e-106">Свойство **саурцелистинфо** объекта [**Product**](product-object.md) получает и задает свойства исходных сведений для продукта.</span><span class="sxs-lookup"><span data-stu-id="c927e-106">The **SourceListInfo** property of the [**Product**](product-object.md) object gets and sets the source information properties for a product.</span></span> <span data-ttu-id="c927e-107">Это свойство вызывает [**мсисаурцелистжетинфо**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) или [**мсисаурцелистсетинфо**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="c927e-107">This property calls [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="c927e-108">Это свойство для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="c927e-108">This is a read or write property.</span></span>

<span data-ttu-id="c927e-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c927e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c927e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c927e-110">Syntax</span></span>


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="c927e-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c927e-111">Property value</span></span>

<span data-ttu-id="c927e-112">Имя свойств сведений об источнике для продукта, для которого запрашиваются или задаются значения.</span><span class="sxs-lookup"><span data-stu-id="c927e-112">The name of the source information properties for a product to query or set.</span></span> <span data-ttu-id="c927e-113">Возможные значения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="c927e-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="c927e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c927e-114">Remarks</span></span>

<span data-ttu-id="c927e-115">Можно задать не все свойства, которые могут быть получены.</span><span class="sxs-lookup"><span data-stu-id="c927e-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="c927e-116">Параметр *сзпроперти* может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c927e-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="c927e-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="c927e-117">Property</span></span>         | <span data-ttu-id="c927e-118">Можно ли установить?</span><span class="sxs-lookup"><span data-stu-id="c927e-118">Can set?</span></span> | <span data-ttu-id="c927e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c927e-119">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c927e-120">медиапаккажепас</span><span class="sxs-lookup"><span data-stu-id="c927e-120">MediaPackagePath</span></span> | <span data-ttu-id="c927e-121">Да</span><span class="sxs-lookup"><span data-stu-id="c927e-121">Y</span></span>        | <span data-ttu-id="c927e-122">Путь относительно корня установочного носителя.</span><span class="sxs-lookup"><span data-stu-id="c927e-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="c927e-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="c927e-123">DiskPrompt</span></span>       | <span data-ttu-id="c927e-124">Да</span><span class="sxs-lookup"><span data-stu-id="c927e-124">Y</span></span>        | <span data-ttu-id="c927e-125">Шаблон подсказки, используемый при запросе пользователя к установочному носителю.</span><span class="sxs-lookup"><span data-stu-id="c927e-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="c927e-126">ластуседсаурце</span><span class="sxs-lookup"><span data-stu-id="c927e-126">LastUsedSource</span></span>   | <span data-ttu-id="c927e-127">Да</span><span class="sxs-lookup"><span data-stu-id="c927e-127">Y</span></span>        | <span data-ttu-id="c927e-128">Последнее использованное исходное расположение продукта.</span><span class="sxs-lookup"><span data-stu-id="c927e-128">The most recently used source location for the product.</span></span> <span data-ttu-id="c927e-129">При задании этого свойства укажите для расположения источника значение "n;" для источника сети или "u;" для типа URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="c927e-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="c927e-130">Например, "n; \\ \\ «Рабочая \\ зона» \\ и «u; https://MyServer/MyFolder/MySource ».</span><span class="sxs-lookup"><span data-stu-id="c927e-130">For example, "n;\\\\scratch\\scratch\\MySource" and "u;https://MyServer/MyFolder/MySource".</span></span> |
| <span data-ttu-id="c927e-131">ластуседтипе</span><span class="sxs-lookup"><span data-stu-id="c927e-131">LastUsedType</span></span>     | <span data-ttu-id="c927e-132">Нет</span><span class="sxs-lookup"><span data-stu-id="c927e-132">N</span></span>        | <span data-ttu-id="c927e-133">"n", если последний источник является сетевым расположением.</span><span class="sxs-lookup"><span data-stu-id="c927e-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="c927e-134">"u", если последний использованный источник был URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="c927e-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="c927e-135">"m", если последний использованный источник был носителем.</span><span class="sxs-lookup"><span data-stu-id="c927e-135">"m" if the last used source was media.</span></span> <span data-ttu-id="c927e-136">Пустая строка (""), если нет последнего использованного источника.</span><span class="sxs-lookup"><span data-stu-id="c927e-136">Empty string ("") if there is no last used source.</span></span>                                                                   |
| <span data-ttu-id="c927e-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="c927e-137">PackageName</span></span>      | <span data-ttu-id="c927e-138">Да</span><span class="sxs-lookup"><span data-stu-id="c927e-138">Y</span></span>        | <span data-ttu-id="c927e-139">Имя пакета установщик Windows или пакета исправлений в источнике.</span><span class="sxs-lookup"><span data-stu-id="c927e-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="c927e-140">Требования</span><span class="sxs-lookup"><span data-stu-id="c927e-140">Requirements</span></span>



| <span data-ttu-id="c927e-141">Требование</span><span class="sxs-lookup"><span data-stu-id="c927e-141">Requirement</span></span> | <span data-ttu-id="c927e-142">Значение</span><span class="sxs-lookup"><span data-stu-id="c927e-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c927e-143">Версия</span><span class="sxs-lookup"><span data-stu-id="c927e-143">Version</span></span><br/> | <span data-ttu-id="c927e-144">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c927e-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c927e-145">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c927e-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c927e-146">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c927e-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="c927e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c927e-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="c927e-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c927e-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="c927e-149">IID</span><span class="sxs-lookup"><span data-stu-id="c927e-149">IID</span></span><br/>     | <span data-ttu-id="c927e-150">IID \_ ипродукт определен как 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c927e-150">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="c927e-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c927e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c927e-152">**Продукта**</span><span class="sxs-lookup"><span data-stu-id="c927e-152">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="c927e-153">**мсисаурцелистжетинфо**</span><span class="sxs-lookup"><span data-stu-id="c927e-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="c927e-154">**мсисаурцелистсетинфо**</span><span class="sxs-lookup"><span data-stu-id="c927e-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="c927e-155">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="c927e-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




