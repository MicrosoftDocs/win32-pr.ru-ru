---
description: Свойство Саурцелистинфо объекта Patch возвращает и задает свойства исходных сведений для исправления. Это свойство вызывает Мсисаурцелистжетинфо или Мсисаурцелистсетинфо. Это свойство для чтения или записи.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Свойство patch. Саурцелистинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651702"
---
# <a name="patchsourcelistinfo-property"></a><span data-ttu-id="f50a4-105">Свойство patch. Саурцелистинфо</span><span class="sxs-lookup"><span data-stu-id="f50a4-105">Patch.SourceListInfo property</span></span>

<span data-ttu-id="f50a4-106">Свойство **саурцелистинфо** объекта [**Patch**](patch-object.md) возвращает и задает свойства исходных сведений для исправления.</span><span class="sxs-lookup"><span data-stu-id="f50a4-106">The **SourceListInfo** property of the [**Patch**](patch-object.md) object gets and sets the source information properties for a patch.</span></span> <span data-ttu-id="f50a4-107">Это свойство вызывает [**мсисаурцелистжетинфо**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) или [**мсисаурцелистсетинфо**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="f50a4-107">This property call [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="f50a4-108">Это свойство для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="f50a4-108">This is a read or write property.</span></span>

<span data-ttu-id="f50a4-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f50a4-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f50a4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f50a4-110">Syntax</span></span>


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="f50a4-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f50a4-111">Property value</span></span>

<span data-ttu-id="f50a4-112">Имя свойств сведений об источнике, для которого запрашивается или задается исправление.</span><span class="sxs-lookup"><span data-stu-id="f50a4-112">The name of the source information properties for a patch to query or set.</span></span> <span data-ttu-id="f50a4-113">Возможные значения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="f50a4-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="f50a4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f50a4-114">Remarks</span></span>

<span data-ttu-id="f50a4-115">Можно задать не все свойства, которые могут быть получены.</span><span class="sxs-lookup"><span data-stu-id="f50a4-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="f50a4-116">Параметр *сзпроперти* может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f50a4-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="f50a4-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="f50a4-117">Property</span></span>         | <span data-ttu-id="f50a4-118">Можно ли установить?</span><span class="sxs-lookup"><span data-stu-id="f50a4-118">Can set?</span></span> | <span data-ttu-id="f50a4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f50a4-119">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f50a4-120">медиапаккажепас</span><span class="sxs-lookup"><span data-stu-id="f50a4-120">MediaPackagePath</span></span> | <span data-ttu-id="f50a4-121">Да</span><span class="sxs-lookup"><span data-stu-id="f50a4-121">Y</span></span>        | <span data-ttu-id="f50a4-122">Путь относительно корня установочного носителя.</span><span class="sxs-lookup"><span data-stu-id="f50a4-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="f50a4-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="f50a4-123">DiskPrompt</span></span>       | <span data-ttu-id="f50a4-124">Да</span><span class="sxs-lookup"><span data-stu-id="f50a4-124">Y</span></span>        | <span data-ttu-id="f50a4-125">Шаблон подсказки, используемый при запросе пользователя к установочному носителю.</span><span class="sxs-lookup"><span data-stu-id="f50a4-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="f50a4-126">ластуседсаурце</span><span class="sxs-lookup"><span data-stu-id="f50a4-126">LastUsedSource</span></span>   | <span data-ttu-id="f50a4-127">Да</span><span class="sxs-lookup"><span data-stu-id="f50a4-127">Y</span></span>        | <span data-ttu-id="f50a4-128">Последнее использованное исходное расположение исправления.</span><span class="sxs-lookup"><span data-stu-id="f50a4-128">The most recently used source location for the patch.</span></span> <span data-ttu-id="f50a4-129">При задании этого свойства укажите для расположения источника значение "n;" для источника сети или "u;" для типа URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f50a4-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="f50a4-130">Например, используйте "n; \\ \\ \\Тест "Рабочая Рабочая область \\ " или "u; https://microsoft.com/Patches/Office/SP1 ".</span><span class="sxs-lookup"><span data-stu-id="f50a4-130">For example, use "n;\\\\scratch\\scratch\\test" or "u;https://microsoft.com/Patches/Office/SP1".</span></span> |
| <span data-ttu-id="f50a4-131">ластуседтипе</span><span class="sxs-lookup"><span data-stu-id="f50a4-131">LastUsedType</span></span>     | <span data-ttu-id="f50a4-132">Нет</span><span class="sxs-lookup"><span data-stu-id="f50a4-132">N</span></span>        | <span data-ttu-id="f50a4-133">"n", если последний источник является сетевым расположением.</span><span class="sxs-lookup"><span data-stu-id="f50a4-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="f50a4-134">"u", если последний использованный источник был URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="f50a4-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="f50a4-135">"m", если последний использованный источник был носителем.</span><span class="sxs-lookup"><span data-stu-id="f50a4-135">"m" if the last used source was media.</span></span> <span data-ttu-id="f50a4-136">Пустая строка (""), если нет последнего использованного источника.</span><span class="sxs-lookup"><span data-stu-id="f50a4-136">Empty string ("") if there is no last used source.</span></span>                                                                      |
| <span data-ttu-id="f50a4-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="f50a4-137">PackageName</span></span>      | <span data-ttu-id="f50a4-138">Да</span><span class="sxs-lookup"><span data-stu-id="f50a4-138">Y</span></span>        | <span data-ttu-id="f50a4-139">Имя пакета установщик Windows или пакета исправлений в источнике.</span><span class="sxs-lookup"><span data-stu-id="f50a4-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="f50a4-140">Требования</span><span class="sxs-lookup"><span data-stu-id="f50a4-140">Requirements</span></span>



| <span data-ttu-id="f50a4-141">Требование</span><span class="sxs-lookup"><span data-stu-id="f50a4-141">Requirement</span></span> | <span data-ttu-id="f50a4-142">Значение</span><span class="sxs-lookup"><span data-stu-id="f50a4-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f50a4-143">Версия</span><span class="sxs-lookup"><span data-stu-id="f50a4-143">Version</span></span><br/> | <span data-ttu-id="f50a4-144">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f50a4-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f50a4-145">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f50a4-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f50a4-146">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f50a4-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="f50a4-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f50a4-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="f50a4-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f50a4-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="f50a4-149">IID</span><span class="sxs-lookup"><span data-stu-id="f50a4-149">IID</span></span><br/>     | <span data-ttu-id="f50a4-150">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f50a4-150">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="f50a4-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f50a4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f50a4-152">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="f50a4-152">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="f50a4-153">**мсисаурцелистжетинфо**</span><span class="sxs-lookup"><span data-stu-id="f50a4-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="f50a4-154">**мсисаурцелистсетинфо**</span><span class="sxs-lookup"><span data-stu-id="f50a4-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="f50a4-155">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="f50a4-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




