---
description: Свойство Патчпроперти возвращает сведения о конкретном исправлении, примененном к конкретному экземпляру продукта. Это свойство вызывает Мсижетпатчинфоекс.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Метод PATCH. Патчпроперти
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652022"
---
# <a name="patchpatchproperty-method"></a><span data-ttu-id="e39ce-104">Метод PATCH. Патчпроперти</span><span class="sxs-lookup"><span data-stu-id="e39ce-104">Patch.PatchProperty method</span></span>

<span data-ttu-id="e39ce-105">Свойство **патчпроперти** возвращает сведения о конкретном исправлении, примененном к конкретному экземпляру продукта.</span><span class="sxs-lookup"><span data-stu-id="e39ce-105">The **PatchProperty** property gets information about a specific patch applied to a specific instance of the product.</span></span> <span data-ttu-id="e39ce-106">Это свойство вызывает [**мсижетпатчинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="e39ce-106">This property calls [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="e39ce-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e39ce-107">Syntax</span></span>


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a><span data-ttu-id="e39ce-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e39ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e39ce-109">*сзпроперти*</span><span class="sxs-lookup"><span data-stu-id="e39ce-109">*szProperty*</span></span> 
</dt> <dd>

<span data-ttu-id="e39ce-110">Параметр *сзпроперти* может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e39ce-110">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="e39ce-111">Имя</span><span class="sxs-lookup"><span data-stu-id="e39ce-111">Name</span></span>          | <span data-ttu-id="e39ce-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e39ce-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e39ce-113">локалпаккаже</span><span class="sxs-lookup"><span data-stu-id="e39ce-113">LocalPackage</span></span>  | <span data-ttu-id="e39ce-114">Получите кэшированный файл исправления, используемый продуктом.</span><span class="sxs-lookup"><span data-stu-id="e39ce-114">Get the cached patch file used by the product.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="e39ce-115">Преобразования</span><span class="sxs-lookup"><span data-stu-id="e39ce-115">Transforms</span></span>    | <span data-ttu-id="e39ce-116">Получение набора преобразований исправлений, примененных к продукту при последнем установке исправлений.</span><span class="sxs-lookup"><span data-stu-id="e39ce-116">Get the set of patch transforms applied to the product by the last patch installation.</span></span> <span data-ttu-id="e39ce-117">Это значение может быть недоступно для неуправляемых приложений для отдельных пользователей, если пользователь не вошел в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="e39ce-117">This value may not be available for per-user-unmanaged applications if the user is not logged in to the computer.</span></span>                                                                                                                     |
| <span data-ttu-id="e39ce-118">InstallDate</span><span class="sxs-lookup"><span data-stu-id="e39ce-118">InstallDate</span></span>   | <span data-ttu-id="e39ce-119">Получение даты, когда исправление было применено к продукту.</span><span class="sxs-lookup"><span data-stu-id="e39ce-119">Get the date when the patch was applied to the product.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="e39ce-120">Удалять</span><span class="sxs-lookup"><span data-stu-id="e39ce-120">Uninstallable</span></span> | <span data-ttu-id="e39ce-121">Возвращает значение 1, если исправление помечено как можно для удаления из продукта.</span><span class="sxs-lookup"><span data-stu-id="e39ce-121">Returns "1" if the patch is marked as possible to uninstall from the product.</span></span> <span data-ttu-id="e39ce-122">В этом случае установщик по-прежнему может блокировать удаление, если это исправление требуется для другого исправления, которое не может быть удалено.</span><span class="sxs-lookup"><span data-stu-id="e39ce-122">In this case, the installer can still block the uninstallation if this patch is required by another patch that cannot be uninstalled.</span></span>                                                                                                          |
| <span data-ttu-id="e39ce-123">Состояние</span><span class="sxs-lookup"><span data-stu-id="e39ce-123">State</span></span>         | <span data-ttu-id="e39ce-124">Возвращает значение 1, если данное исправление применяется к продукту.</span><span class="sxs-lookup"><span data-stu-id="e39ce-124">Returns "1" if this patch is currently applied to the product.</span></span> <span data-ttu-id="e39ce-125">Возвращает значение 2, если это исправление заменено другим исправлением.</span><span class="sxs-lookup"><span data-stu-id="e39ce-125">Returns "2" if this patch has been superseded by another patch.</span></span> <span data-ttu-id="e39ce-126">Возвращает значение 4, если это исправление стало устаревшим другим исправлением.</span><span class="sxs-lookup"><span data-stu-id="e39ce-126">Returns "4" if this patch has been made obsolete by another patch.</span></span> <span data-ttu-id="e39ce-127">Эти значения соответствуют константам, используемым параметром *Двфилтер* [**мсиенумпатчесекс**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="e39ce-127">These values correspond to the constants used by the *dwFilter* parameter of [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span> |
| <span data-ttu-id="e39ce-128">DisplayName</span><span class="sxs-lookup"><span data-stu-id="e39ce-128">DisplayName</span></span>   | <span data-ttu-id="e39ce-129">Получите Зарегистрированное отображаемое имя для исправления.</span><span class="sxs-lookup"><span data-stu-id="e39ce-129">Get the registered display name for the patch.</span></span> <span data-ttu-id="e39ce-130">Для исправлений, которые не включают свойство DisplayName в таблицу [мсипатчметадата](msipatchmetadata-table.md) , возвращаемое отображаемое имя является пустой строкой ("").</span><span class="sxs-lookup"><span data-stu-id="e39ce-130">For patches that do not include the DisplayName property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned display name is an empty string ("").</span></span>                                                                                                      |
| <span data-ttu-id="e39ce-131">мореинфаурл</span><span class="sxs-lookup"><span data-stu-id="e39ce-131">MoreInfoURL</span></span>   | <span data-ttu-id="e39ce-132">Получите зарегистрированный URL-адрес сведений о поддержке для исправления.</span><span class="sxs-lookup"><span data-stu-id="e39ce-132">Get the registered support information URL for the patch.</span></span> <span data-ttu-id="e39ce-133">Для исправлений, которые не включают свойство Мореинфаурл в таблицу [мсипатчметадата](msipatchmetadata-table.md) , возвращенный URL-адрес информации о поддержке является пустой строкой ("").</span><span class="sxs-lookup"><span data-stu-id="e39ce-133">For patches that do not include the MoreInfoURL property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned support information URL is an empty string ("").</span></span>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e39ce-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e39ce-134">Return value</span></span>

<span data-ttu-id="e39ce-135">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e39ce-135">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e39ce-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e39ce-136">Remarks</span></span>

<span data-ttu-id="e39ce-137">Этот метод может возвращать ошибку \_ неизвестное \_ исправление, если объект [**Patch**](patch-object.md) инициализируется пустой строкой для *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="e39ce-137">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e39ce-138">Требования</span><span class="sxs-lookup"><span data-stu-id="e39ce-138">Requirements</span></span>



| <span data-ttu-id="e39ce-139">Требование</span><span class="sxs-lookup"><span data-stu-id="e39ce-139">Requirement</span></span> | <span data-ttu-id="e39ce-140">Значение</span><span class="sxs-lookup"><span data-stu-id="e39ce-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e39ce-141">Версия</span><span class="sxs-lookup"><span data-stu-id="e39ce-141">Version</span></span><br/> | <span data-ttu-id="e39ce-142">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e39ce-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e39ce-143">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e39ce-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e39ce-144">Установщик Windows 3,0 или более поздней версии в Windows Server 2003, Windows XP и Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e39ce-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e39ce-145">DLL</span><span class="sxs-lookup"><span data-stu-id="e39ce-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="e39ce-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e39ce-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e39ce-147">IID</span><span class="sxs-lookup"><span data-stu-id="e39ce-147">IID</span></span><br/>     | <span data-ttu-id="e39ce-148">IID \_ ипатч определен как 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e39ce-148">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="e39ce-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e39ce-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e39ce-150">**Защиты**</span><span class="sxs-lookup"><span data-stu-id="e39ce-150">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="e39ce-151">**мсиенумпатчесекс**</span><span class="sxs-lookup"><span data-stu-id="e39ce-151">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="e39ce-152">**мсижетпатчинфоекс**</span><span class="sxs-lookup"><span data-stu-id="e39ce-152">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="e39ce-153">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="e39ce-153">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




