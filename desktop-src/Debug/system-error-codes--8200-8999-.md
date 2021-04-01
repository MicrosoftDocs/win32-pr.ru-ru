---
description: Описание кодов ошибок 8200-8999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Коды системных ошибок (8200-8999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262637"
---
# <a name="system-error-codes-8200-8999"></a><span data-ttu-id="ad39a-103">Коды системных ошибок (8200-8999)</span><span class="sxs-lookup"><span data-stu-id="ad39a-103">System Error Codes (8200-8999)</span></span>

> [!NOTE]
> <span data-ttu-id="ad39a-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="ad39a-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="ad39a-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="ad39a-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 8200 – 8999.</span><span class="sxs-lookup"><span data-stu-id="ad39a-106">The following list describes [system error codes](system-error-codes.md) for errors 8200 to 8999.</span></span> <span data-ttu-id="ad39a-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="ad39a-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="ad39a-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="ad39a-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="ad39a-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**Ошибка \_ DS \_ не \_ установлена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-109"><span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR\_DS\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-110">8200 (0x2008)</span><span class="sxs-lookup"><span data-stu-id="ad39a-110">8200 (0x2008)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-111">Произошла ошибка при установке службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-111">An error occurred while installing the directory service.</span></span> <span data-ttu-id="ad39a-112">Дополнительные сведения см. в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="ad39a-112">For more information, see the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**Ошибка проверки \_ членства в DS в \_ \_ \_ локальной среде**</span><span class="sxs-lookup"><span data-stu-id="ad39a-113"><span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR\_DS\_MEMBERSHIP\_EVALUATED\_LOCALLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-114">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="ad39a-114">8201 (0x2009)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-115">Служба каталогов проверила членство в группах локально.</span><span class="sxs-lookup"><span data-stu-id="ad39a-115">The directory service evaluated group memberships locally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**Ошибка \_ DS \_ без \_ атрибута \_ или \_ значения**</span><span class="sxs-lookup"><span data-stu-id="ad39a-116"><span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR\_DS\_NO\_ATTRIBUTE\_OR\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-117">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-117">8202 (0x200A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-118">Указанный атрибут или значение службы каталогов не существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-118">The specified directory service attribute or value does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**Ошибка \_ DS \_ недопустимого \_ \_ синтаксиса атрибута**</span><span class="sxs-lookup"><span data-stu-id="ad39a-119"><span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR\_DS\_INVALID\_ATTRIBUTE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-120">8203 (0x200B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-120">8203 (0x200B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-121">В службе каталогов указан недопустимый синтаксис атрибута.</span><span class="sxs-lookup"><span data-stu-id="ad39a-121">The attribute syntax specified to the directory service is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**\_тип атрибута ошибки DS не \_ \_ \_ определен**</span><span class="sxs-lookup"><span data-stu-id="ad39a-122"><span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR\_DS\_ATTRIBUTE\_TYPE\_UNDEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-123">8204 (0x200C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-123">8204 (0x200C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-124">Тип атрибута, указанный для службы каталогов, не определен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-124">The attribute type specified to the directory service is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**\_существует ошибка \_ атрибута \_ или \_ значения \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-125"><span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR\_DS\_ATTRIBUTE\_OR\_VALUE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-126">8205 (0x200D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-126">8205 (0x200D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-127">Указанный атрибут или значение службы каталогов уже существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-127">The specified directory service attribute or value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**Ошибка \_ DS \_ Busy**</span><span class="sxs-lookup"><span data-stu-id="ad39a-128"><span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR\_DS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-129">8206 (0x200E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-129">8206 (0x200E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-130">Служба каталогов занята.</span><span class="sxs-lookup"><span data-stu-id="ad39a-130">The directory service is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**Ошибка \_ DS \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="ad39a-131"><span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR\_DS\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-132">8207 (0x200F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-132">8207 (0x200F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-133">Служба каталогов недоступна.</span><span class="sxs-lookup"><span data-stu-id="ad39a-133">The directory service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**Ошибка \_ DS \_ — \_ не \_ выделено ни одного RID**</span><span class="sxs-lookup"><span data-stu-id="ad39a-134"><span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR\_DS\_NO\_RIDS\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-135">8208 (0x2010)</span><span class="sxs-lookup"><span data-stu-id="ad39a-135">8208 (0x2010)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-136">Служба каталогов не смогла выделить относительный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="ad39a-136">The directory service was unable to allocate a relative identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**Ошибка \_ DS \_ , \_ другие \_ идентификаторы RID**</span><span class="sxs-lookup"><span data-stu-id="ad39a-137"><span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR\_DS\_NO\_MORE\_RIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-138">8209 (0x2011)</span><span class="sxs-lookup"><span data-stu-id="ad39a-138">8209 (0x2011)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-139">Служба каталогов исчерпала пул относительных идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-139">The directory service has exhausted the pool of relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**Ошибка \_ DS \_ — \_ неправильный \_ владелец роли**</span><span class="sxs-lookup"><span data-stu-id="ad39a-140"><span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR\_DS\_INCORRECT\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-141">8210 (0x2012)</span><span class="sxs-lookup"><span data-stu-id="ad39a-141">8210 (0x2012)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-142">Не удалось выполнить запрошенную операцию, так как служба каталогов не является главной для этого типа операции.</span><span class="sxs-lookup"><span data-stu-id="ad39a-142">The requested operation could not be performed because the directory service is not the master for that type of operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**Ошибка \_ при \_ инициализации ридмгр DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-143"><span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERROR\_DS\_RIDMGR\_INIT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-144">8211 (0x2013)</span><span class="sxs-lookup"><span data-stu-id="ad39a-144">8211 (0x2013)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-145">Службе каталогов не удалось инициализировать подсистему, которая выделяет относительные идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-145">The directory service was unable to initialize the subsystem that allocates relative identifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**Ошибка \_ при \_ \_ нарушении класса obj DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-146"><span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR\_DS\_OBJ\_CLASS\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-147">8212 (0x2014)</span><span class="sxs-lookup"><span data-stu-id="ad39a-147">8212 (0x2014)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-148">Запрошенная операция не удовлетворяет одному или нескольким ограничениям, связанным с классом объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-148">The requested operation did not satisfy one or more constraints associated with the class of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**Ошибка \_ DS \_ \_ не удается \_ на \_ неконечных**</span><span class="sxs-lookup"><span data-stu-id="ad39a-149"><span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR\_DS\_CANT\_ON\_NON\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-150">8213 (0x2015)</span><span class="sxs-lookup"><span data-stu-id="ad39a-150">8213 (0x2015)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-151">Служба каталогов может выполнить запрошенную операцию только для конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-151">The directory service can perform the requested operation only on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**Ошибка \_ DS не \_ удается \_ на \_ RDN**</span><span class="sxs-lookup"><span data-stu-id="ad39a-152"><span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR\_DS\_CANT\_ON\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-153">8214 (0x2016)</span><span class="sxs-lookup"><span data-stu-id="ad39a-153">8214 (0x2016)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-154">Службе каталогов не удается выполнить запрошенную операцию с атрибутом RDN объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-154">The directory service cannot perform the requested operation on the RDN attribute of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**Ошибка \_ DS \_ не \_ удается \_ \_ класс obj класса mod**</span><span class="sxs-lookup"><span data-stu-id="ad39a-155"><span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR\_DS\_CANT\_MOD\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-156">8215 (0x2017)</span><span class="sxs-lookup"><span data-stu-id="ad39a-156">8215 (0x2017)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-157">Служба каталогов обнаружила попытку изменить класс объекта объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-157">The directory service detected an attempt to modify the object class of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**Ошибка \_ \_ перемещения перекрестной \_ модели DOM для \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-158"><span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**ERROR\_DS\_CROSS\_DOM\_MOVE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-159">8216 (0x2018)</span><span class="sxs-lookup"><span data-stu-id="ad39a-159">8216 (0x2018)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-160">Не удалось выполнить запрошенную операцию междоменного перемещения.</span><span class="sxs-lookup"><span data-stu-id="ad39a-160">The requested cross-domain move operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**Ошибка \_ \_ сборки мусора DS \_ не \_ доступна**</span><span class="sxs-lookup"><span data-stu-id="ad39a-161"><span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR\_DS\_GC\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-162">8217 (0x2019)</span><span class="sxs-lookup"><span data-stu-id="ad39a-162">8217 (0x2019)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-163">Не удалось связаться с сервером глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="ad39a-163">Unable to contact the global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**\_Общая \_ Политика ошибок**</span><span class="sxs-lookup"><span data-stu-id="ad39a-164"><span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERROR\_SHARED\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-165">8218 (0x201A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-165">8218 (0x201A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-166">Объект политики является общим и может быть изменен только в корне.</span><span class="sxs-lookup"><span data-stu-id="ad39a-166">The policy object is shared and can only be modified at the root.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**\_объект политики \_ ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="ad39a-167"><span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**ERROR\_POLICY\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-168">8219 (0x201B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-168">8219 (0x201B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-169">Объект политики не существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-169">The policy object does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_Политика ошибок \_ только \_ в \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-170"><span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**ERROR\_POLICY\_ONLY\_IN\_DS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-171">8220 (0x201C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-171">8220 (0x201C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-172">Запрошенные сведения о политике находятся только в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-172">The requested policy information is only in the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**\_продвижение ошибки \_ активно**</span><span class="sxs-lookup"><span data-stu-id="ad39a-173"><span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**ERROR\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-174">8221 (0x201D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-174">8221 (0x201D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-175">Повышение роли контроллера домена сейчас активно.</span><span class="sxs-lookup"><span data-stu-id="ad39a-175">A domain controller promotion is currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**Ошибка \_ без \_ повышения \_ активности**</span><span class="sxs-lookup"><span data-stu-id="ad39a-176"><span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR\_NO\_PROMOTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-177">8222 (0x201E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-177">8222 (0x201E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-178">Повышение роли контроллера домена сейчас неактивно.</span><span class="sxs-lookup"><span data-stu-id="ad39a-178">A domain controller promotion is not currently active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**Ошибка \_ \_ операций DS Operations \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-179"><span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**ERROR\_DS\_OPERATIONS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-180">8224 (0x2020)</span><span class="sxs-lookup"><span data-stu-id="ad39a-180">8224 (0x2020)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-181">Произошла ошибка операции.</span><span class="sxs-lookup"><span data-stu-id="ad39a-181">An operations error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**Ошибка \_ \_ протокола DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-182"><span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**ERROR\_DS\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-183">8225 (0x2021)</span><span class="sxs-lookup"><span data-stu-id="ad39a-183">8225 (0x2021)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-184">Произошла ошибка протокола.</span><span class="sxs-lookup"><span data-stu-id="ad39a-184">A protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**\_ \_ превышена ошибка тимелимит DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-185"><span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR\_DS\_TIMELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-186">8226 (0x2022)</span><span class="sxs-lookup"><span data-stu-id="ad39a-186">8226 (0x2022)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-187">Превышено предельное время для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-187">The time limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**\_ \_ превышена ошибка сизелимит DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-188"><span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR\_DS\_SIZELIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-189">8227 (0x2023)</span><span class="sxs-lookup"><span data-stu-id="ad39a-189">8227 (0x2023)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-190">Превышен предельный размер для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-190">The size limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**\_ \_ \_ превышен предел администратора DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-191"><span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERROR\_DS\_ADMIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-192">8228 (0x2024)</span><span class="sxs-lookup"><span data-stu-id="ad39a-192">8228 (0x2024)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-193">Превышено административное ограничение для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-193">The administrative limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**Ошибка \_ DS \_ Compare \_ false**</span><span class="sxs-lookup"><span data-stu-id="ad39a-194"><span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR\_DS\_COMPARE\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-195">8229 (0x2025)</span><span class="sxs-lookup"><span data-stu-id="ad39a-195">8229 (0x2025)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-196">Ответ сравнения был ложным.</span><span class="sxs-lookup"><span data-stu-id="ad39a-196">The compare response was false.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**Ошибка \_ DS \_ Compare \_ true**</span><span class="sxs-lookup"><span data-stu-id="ad39a-197"><span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR\_DS\_COMPARE\_TRUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-198">8230 (0x2026)</span><span class="sxs-lookup"><span data-stu-id="ad39a-198">8230 (0x2026)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-199">Ответ сравнения был истинным.</span><span class="sxs-lookup"><span data-stu-id="ad39a-199">The compare response was true.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**Ошибка \_ \_ \_ \_ не поддерживается метод проверки подлинности DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-200"><span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERROR\_DS\_AUTH\_METHOD\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-201">8231 (0x2027)</span><span class="sxs-lookup"><span data-stu-id="ad39a-201">8231 (0x2027)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-202">Запрошенный метод проверки подлинности не поддерживается сервером.</span><span class="sxs-lookup"><span data-stu-id="ad39a-202">The requested authentication method is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**\_ \_ требуется строгая \_ Проверка подлинности DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-203"><span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR\_DS\_STRONG\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-204">8232 (0x2028)</span><span class="sxs-lookup"><span data-stu-id="ad39a-204">8232 (0x2028)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-205">Для этого сервера требуется более безопасный метод проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ad39a-205">A more secure authentication method is required for this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**Ошибка \_ \_ \_ проверки подлинности DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-206"><span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR\_DS\_INAPPROPRIATE\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-207">8233 (0x2029)</span><span class="sxs-lookup"><span data-stu-id="ad39a-207">8233 (0x2029)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-208">Недопустимая проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="ad39a-208">Inappropriate authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**Ошибка \_ \_ проверки подлинности DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-209"><span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR\_DS\_AUTH\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-210">8234 (0x202A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-210">8234 (0x202A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-211">Неизвестный механизм проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ad39a-211">The authentication mechanism is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**Ссылка на ошибку \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-212"><span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**ERROR\_DS\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-213">8235 (0x202B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-213">8235 (0x202B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-214">С сервера была возвращена отсылка.</span><span class="sxs-lookup"><span data-stu-id="ad39a-214">A referral was returned from the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**Ошибка \_ \_ недоступности \_ расширения критерий DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-215"><span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR\_DS\_UNAVAILABLE\_CRIT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-216">8236 (0x202C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-216">8236 (0x202C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-217">Сервер не поддерживает запрошенное критическое расширение.</span><span class="sxs-lookup"><span data-stu-id="ad39a-217">The server does not support the requested critical extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**\_ \_ требуется конфиденциальность DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-218"><span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR\_DS\_CONFIDENTIALITY\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-219">8237 (0x202D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-219">8237 (0x202D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-220">Для этого запроса требуется безопасное соединение.</span><span class="sxs-lookup"><span data-stu-id="ad39a-220">This request requires a secure connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**Ошибка \_ \_ \_ несоответствия DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-221"><span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR\_DS\_INAPPROPRIATE\_MATCHING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-222">8238 (0x202E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-222">8238 (0x202E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-223">Неуместное сопоставление.</span><span class="sxs-lookup"><span data-stu-id="ad39a-223">Inappropriate matching.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**Ошибка \_ \_ нарушения ограничения \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-224"><span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR\_DS\_CONSTRAINT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-225">8239 (0x202F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-225">8239 (0x202F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-226">Произошло нарушение ограничения.</span><span class="sxs-lookup"><span data-stu-id="ad39a-226">A constraint violation occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**Ошибка \_ DS \_ . \_ такой \_ объект отсутствует**</span><span class="sxs-lookup"><span data-stu-id="ad39a-227"><span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR\_DS\_NO\_SUCH\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-228">8240 (0x2030)</span><span class="sxs-lookup"><span data-stu-id="ad39a-228">8240 (0x2030)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-229">На сервере отсутствует такой объект.</span><span class="sxs-lookup"><span data-stu-id="ad39a-229">There is no such object on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**Ошибка \_ \_ псевдонима \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-230"><span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERROR\_DS\_ALIAS\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-231">8241 (0x2031)</span><span class="sxs-lookup"><span data-stu-id="ad39a-231">8241 (0x2031)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-232">Существует проблема с псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="ad39a-232">There is an alias problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**Ошибка \_ DS с \_ недопустимым \_ \_ синтаксисом DN**</span><span class="sxs-lookup"><span data-stu-id="ad39a-233"><span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR\_DS\_INVALID\_DN\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-234">8242 (0x2032)</span><span class="sxs-lookup"><span data-stu-id="ad39a-234">8242 (0x2032)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-235">Указан недопустимый синтаксис DN.</span><span class="sxs-lookup"><span data-stu-id="ad39a-235">An invalid dn syntax has been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**\_ \_ \_ Конечная ошибка DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-236"><span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERROR\_DS\_IS\_LEAF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-237">8243 (0x2033)</span><span class="sxs-lookup"><span data-stu-id="ad39a-237">8243 (0x2033)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-238">Объект является конечным объектом.</span><span class="sxs-lookup"><span data-stu-id="ad39a-238">The object is a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**Ошибка \_ \_ псевдонима DS, \_ \_ связанная с ошибкой Deref**</span><span class="sxs-lookup"><span data-stu-id="ad39a-239"><span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERROR\_DS\_ALIAS\_DEREF\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-240">8244 (0x2034)</span><span class="sxs-lookup"><span data-stu-id="ad39a-240">8244 (0x2034)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-241">Существует проблема разыменования псевдонима.</span><span class="sxs-lookup"><span data-stu-id="ad39a-241">There is an alias dereferencing problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**\_ \_ не будет \_ выполнена ошибка DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-242"><span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR\_DS\_UNWILLING\_TO\_PERFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-243">8245 (0x2035)</span><span class="sxs-lookup"><span data-stu-id="ad39a-243">8245 (0x2035)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-244">Сервер не будет обрабатывать запрос.</span><span class="sxs-lookup"><span data-stu-id="ad39a-244">The server is unwilling to process the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**Ошибка \_ \_ обнаружения циклов DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-245"><span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR\_DS\_LOOP\_DETECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-246">8246 (0x2036)</span><span class="sxs-lookup"><span data-stu-id="ad39a-246">8246 (0x2036)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-247">Обнаружен цикл.</span><span class="sxs-lookup"><span data-stu-id="ad39a-247">A loop has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**Ошибка \_ \_ именования \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-248"><span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR\_DS\_NAMING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-249">8247 (0x2037)</span><span class="sxs-lookup"><span data-stu-id="ad39a-249">8247 (0x2037)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-250">Существует нарушение именования.</span><span class="sxs-lookup"><span data-stu-id="ad39a-250">There is a naming violation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**\_результаты объекта "ошибка DS" \_ \_ \_ слишком \_ велики**</span><span class="sxs-lookup"><span data-stu-id="ad39a-251"><span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERROR\_DS\_OBJECT\_RESULTS\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-252">8248 (0x2038)</span><span class="sxs-lookup"><span data-stu-id="ad39a-252">8248 (0x2038)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-253">Результирующий набор слишком велик.</span><span class="sxs-lookup"><span data-stu-id="ad39a-253">The result set is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**Служба "ошибки \_ DS" \_ влияет на \_ несколько \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="ad39a-254"><span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERROR\_DS\_AFFECTS\_MULTIPLE\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-255">8249 (0x2039)</span><span class="sxs-lookup"><span data-stu-id="ad39a-255">8249 (0x2039)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-256">Операция влияет на несколько DSA.</span><span class="sxs-lookup"><span data-stu-id="ad39a-256">The operation affects multiple DSAs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**Ошибка \_ \_ сервера DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-257"><span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR\_DS\_SERVER\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-258">8250 (0x203A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-258">8250 (0x203A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-259">Сервер не работает.</span><span class="sxs-lookup"><span data-stu-id="ad39a-259">The server is not operational.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**Ошибка \_ \_ локальной \_ ошибки DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-260"><span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**ERROR\_DS\_LOCAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-261">8251 (0x203B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-261">8251 (0x203B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-262">Произошла локальная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ad39a-262">A local error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**Ошибка \_ \_ кодирования DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-263"><span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**ERROR\_DS\_ENCODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-264">8252 (0x203C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-264">8252 (0x203C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-265">Произошла ошибка кодирования.</span><span class="sxs-lookup"><span data-stu-id="ad39a-265">An encoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**Ошибка \_ \_ декодирования DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-266"><span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**ERROR\_DS\_DECODING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-267">8253 (0x203D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-267">8253 (0x203D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-268">Произошла ошибка декодирования.</span><span class="sxs-lookup"><span data-stu-id="ad39a-268">A decoding error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**Ошибка \_ \_ \_ неизвестного фильтра DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-269"><span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR\_DS\_FILTER\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-270">8254 (0x203E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-270">8254 (0x203E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-271">Не удается распознать фильтр поиска.</span><span class="sxs-lookup"><span data-stu-id="ad39a-271">The search filter cannot be recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**Ошибка \_ параметра службы DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-272"><span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**ERROR\_DS\_PARAM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-273">8255 (0x203F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-273">8255 (0x203F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-274">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-274">One or more parameters are illegal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**Ошибка \_ DS \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="ad39a-275"><span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR\_DS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-276">8256 (0x2040)</span><span class="sxs-lookup"><span data-stu-id="ad39a-276">8256 (0x2040)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-277">Указанный метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-277">The specified method is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**Ошибка \_ DS \_ . \_ результаты не \_ возвращены**</span><span class="sxs-lookup"><span data-stu-id="ad39a-278"><span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR\_DS\_NO\_RESULTS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-279">8257 (0x2041)</span><span class="sxs-lookup"><span data-stu-id="ad39a-279">8257 (0x2041)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-280">Результаты не возвращены.</span><span class="sxs-lookup"><span data-stu-id="ad39a-280">No results were returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**Ошибка \_ \_ управления DS \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-281"><span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERROR\_DS\_CONTROL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-282">8258 (0x2042)</span><span class="sxs-lookup"><span data-stu-id="ad39a-282">8258 (0x2042)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-283">Указанный элемент управления не поддерживается сервером.</span><span class="sxs-lookup"><span data-stu-id="ad39a-283">The specified control is not supported by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**Ошибка \_ \_ клиентский \_ цикл DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-284"><span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR\_DS\_CLIENT\_LOOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-285">8259 (0x2043)</span><span class="sxs-lookup"><span data-stu-id="ad39a-285">8259 (0x2043)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-286">Клиент обнаружил цикл ссылок.</span><span class="sxs-lookup"><span data-stu-id="ad39a-286">A referral loop was detected by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**\_ \_ \_ превышен предел ссылок DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-287"><span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERROR\_DS\_REFERRAL\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-288">8260 (0x2044)</span><span class="sxs-lookup"><span data-stu-id="ad39a-288">8260 (0x2044)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-289">Предустановленный предел ссылок был превышен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-289">The preset referral limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**Ошибка \_ \_ управления сортировкой DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-290"><span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR\_DS\_SORT\_CONTROL\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-291">8261 (0x2045)</span><span class="sxs-lookup"><span data-stu-id="ad39a-291">8261 (0x2045)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-292">Для поиска требуется элемент управления SORT.</span><span class="sxs-lookup"><span data-stu-id="ad39a-292">The search requires a SORT control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**Ошибка \_ \_ диапазона смещения для DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-293"><span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**ERROR\_DS\_OFFSET\_RANGE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-294">8262 (0x2046)</span><span class="sxs-lookup"><span data-stu-id="ad39a-294">8262 (0x2046)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-295">Результаты поиска превышают указанный диапазон смещений.</span><span class="sxs-lookup"><span data-stu-id="ad39a-295">The search results exceed the offset range specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**Ошибка \_ DS \_ ридмгр \_ Disabled**</span><span class="sxs-lookup"><span data-stu-id="ad39a-296"><span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR\_DS\_RIDMGR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-297">8263 (0x2047)</span><span class="sxs-lookup"><span data-stu-id="ad39a-297">8263 (0x2047)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-298">Служба каталогов обнаружила, что подсистема, которая выделяет относительные идентификаторы, отключена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-298">The directory service detected the subsystem that allocates relative identifiers is disabled.</span></span> <span data-ttu-id="ad39a-299">Это может произойти в качестве защитного механизма, когда система определяет значительную часть относительных идентификаторов (RID).</span><span class="sxs-lookup"><span data-stu-id="ad39a-299">This can occur as a protective mechanism when the system determines a significant portion of relative identifiers (RIDs) have been exhausted.</span></span> <span data-ttu-id="ad39a-300"><https://go.microsoft.com/fwlink/p/?linkid=228610>Рекомендуемые шаги диагностики и процедура повторного включения создания учетной записи см. в разделе.</span><span class="sxs-lookup"><span data-stu-id="ad39a-300">Please see <https://go.microsoft.com/fwlink/p/?linkid=228610> for recommended diagnostic steps and the procedure to re-enable account creation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**\_корень DS \_ ошибок \_ должен \_ быть \_ NC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-301"><span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERROR\_DS\_ROOT\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-302">8301 (0x206D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-302">8301 (0x206D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-303">Корневой объект должен быть заголовком контекста именования.</span><span class="sxs-lookup"><span data-stu-id="ad39a-303">The root object must be the head of a naming context.</span></span> <span data-ttu-id="ad39a-304">Корневой объект не может иметь экземпляр родителя.</span><span class="sxs-lookup"><span data-stu-id="ad39a-304">The root object cannot have an instantiated parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**Ошибка \_ при \_ добавлении \_ реплики DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-305"><span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR\_DS\_ADD\_REPLICA\_INHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-306">8302 (0x206E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-306">8302 (0x206E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-307">Не удается выполнить операцию добавления реплики.</span><span class="sxs-lookup"><span data-stu-id="ad39a-307">The add replica operation cannot be performed.</span></span> <span data-ttu-id="ad39a-308">Для создания реплики контекст именования должен быть записываемым.</span><span class="sxs-lookup"><span data-stu-id="ad39a-308">The naming context must be writeable in order to create the replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**Ошибка \_ DS \_ Атри \_ Not \_ DEF \_ в \_ схеме**</span><span class="sxs-lookup"><span data-stu-id="ad39a-309"><span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-310">8303 (0x206F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-310">8303 (0x206F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-311">Ссылка на атрибут, который не определен в схеме.</span><span class="sxs-lookup"><span data-stu-id="ad39a-311">A reference to an attribute that is not defined in the schema occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**\_ \_ \_ превышен максимальный размер obj \_ \_ -службы DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-312"><span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERROR\_DS\_MAX\_OBJ\_SIZE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-313">8304 (0x2070)</span><span class="sxs-lookup"><span data-stu-id="ad39a-313">8304 (0x2070)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-314">Превышен максимальный размер объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-314">The maximum size of an object has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**Ошибка \_ доменного \_ \_ \_ имени obj \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-315"><span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR\_DS\_OBJ\_STRING\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-316">8305 (0x2071)</span><span class="sxs-lookup"><span data-stu-id="ad39a-316">8305 (0x2071)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-317">Предпринята попытка добавить в каталог объект с именем, которое уже используется.</span><span class="sxs-lookup"><span data-stu-id="ad39a-317">An attempt was made to add an object to the directory with a name that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**Ошибка \_ DS \_ . \_ не \_ определено RDN \_ в \_ схеме**</span><span class="sxs-lookup"><span data-stu-id="ad39a-318"><span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR\_DS\_NO\_RDN\_DEFINED\_IN\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-319">8306 (0x2072)</span><span class="sxs-lookup"><span data-stu-id="ad39a-319">8306 (0x2072)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-320">Предпринята попытка добавить объект класса, не имеющий RDN, определенного в схеме.</span><span class="sxs-lookup"><span data-stu-id="ad39a-320">An attempt was made to add an object of a class that does not have an RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**Ошибка \_ \_ RDN DS \_ не \_ соответствует \_ схеме соответствия**</span><span class="sxs-lookup"><span data-stu-id="ad39a-321"><span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERROR\_DS\_RDN\_DOESNT\_MATCH\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-322">8307 (0x2073)</span><span class="sxs-lookup"><span data-stu-id="ad39a-322">8307 (0x2073)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-323">Предпринята попытка добавить объект с помощью RDN, который не является RDN, определенным в схеме.</span><span class="sxs-lookup"><span data-stu-id="ad39a-323">An attempt was made to add an object using an RDN that is not the RDN defined in the schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**Ошибка \_ DS \_ . \_ запрошенные \_ АТТС не \_ найдены**</span><span class="sxs-lookup"><span data-stu-id="ad39a-324"><span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR\_DS\_NO\_REQUESTED\_ATTS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-325">8308 (0x2074)</span><span class="sxs-lookup"><span data-stu-id="ad39a-325">8308 (0x2074)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-326">Ни один из запрошенных атрибутов не был найден для объектов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-326">None of the requested attributes were found on the objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**Ошибка \_ \_ \_ \_ небольшого буфера пользователя \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-327"><span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR\_DS\_USER\_BUFFER\_TO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-328">8309 (0x2075)</span><span class="sxs-lookup"><span data-stu-id="ad39a-328">8309 (0x2075)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-329">Буфер пользователя слишком мал.</span><span class="sxs-lookup"><span data-stu-id="ad39a-329">The user buffer is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**Ошибка \_ DS \_ Атри \_ \_ не включена \_ в \_ obj**</span><span class="sxs-lookup"><span data-stu-id="ad39a-330"><span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR\_DS\_ATT\_IS\_NOT\_ON\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-331">8310 (0x2076)</span><span class="sxs-lookup"><span data-stu-id="ad39a-331">8310 (0x2076)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-332">Атрибут, указанный в операции, отсутствует в объекте.</span><span class="sxs-lookup"><span data-stu-id="ad39a-332">The attribute specified in the operation is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**Ошибка \_ DS \_ недопустимой \_ \_ операции mod**</span><span class="sxs-lookup"><span data-stu-id="ad39a-333"><span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR\_DS\_ILLEGAL\_MOD\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-334">8311 (0x2077)</span><span class="sxs-lookup"><span data-stu-id="ad39a-334">8311 (0x2077)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-335">Недопустимая операция изменения.</span><span class="sxs-lookup"><span data-stu-id="ad39a-335">Illegal modify operation.</span></span> <span data-ttu-id="ad39a-336">Некоторые аспекты изменения не разрешены.</span><span class="sxs-lookup"><span data-stu-id="ad39a-336">Some aspect of the modification is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**Ошибка в OBJ-файле \_ DS \_ \_ слишком \_ большой**</span><span class="sxs-lookup"><span data-stu-id="ad39a-337"><span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERROR\_DS\_OBJ\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-338">8312 (0x2078)</span><span class="sxs-lookup"><span data-stu-id="ad39a-338">8312 (0x2078)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-339">Указанный объект слишком велик.</span><span class="sxs-lookup"><span data-stu-id="ad39a-339">The specified object is too large.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**\_ \_ Недопустимый \_ тип экземпляра ошибки DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-340"><span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERROR\_DS\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-341">8313 (0x2079)</span><span class="sxs-lookup"><span data-stu-id="ad39a-341">8313 (0x2079)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-342">Указан недопустимый тип экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ad39a-342">The specified instance type is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**\_требуется ошибка \_ мастердса \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-343"><span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR\_DS\_MASTERDSA\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-344">8314 (0x207A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-344">8314 (0x207A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-345">Эта операция должна выполняться на главном DSA.</span><span class="sxs-lookup"><span data-stu-id="ad39a-345">The operation must be performed at a master DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**\_ \_ \_ требуется класс объекта DS службы "ошибка" \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-346"><span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**ERROR\_DS\_OBJECT\_CLASS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-347">8315 (0x207B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-347">8315 (0x207B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-348">Необходимо указать атрибут класса объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-348">The object class attribute must be specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**в \_ DS \_ отсутствует \_ обязательный \_ Атри**</span><span class="sxs-lookup"><span data-stu-id="ad39a-349"><span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR\_DS\_MISSING\_REQUIRED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-350">8316 (0x207C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-350">8316 (0x207C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-351">Отсутствует обязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="ad39a-351">A required attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**Ошибка \_ DS \_ Атри, \_ не \_ DEF \_ для \_ класса**</span><span class="sxs-lookup"><span data-stu-id="ad39a-352"><span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR\_DS\_ATT\_NOT\_DEF\_FOR\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-353">8317 (0x207D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-353">8317 (0x207D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-354">Предпринята попытка изменить объект, включив в него атрибут, который не является допустимым для его класса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-354">An attempt was made to modify an object to include an attribute that is not legal for its class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**Ошибка \_ DS \_ Атри \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="ad39a-355"><span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERROR\_DS\_ATT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-356">8318 (0x207E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-356">8318 (0x207E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-357">Указанный атрибут уже существует в объекте.</span><span class="sxs-lookup"><span data-stu-id="ad39a-357">The specified attribute is already present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**Ошибка \_ DS \_ не \_ удается \_ Добавить \_ значения Атри**</span><span class="sxs-lookup"><span data-stu-id="ad39a-358"><span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR\_DS\_CANT\_ADD\_ATT\_VALUES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-359">8320 (0x2080)</span><span class="sxs-lookup"><span data-stu-id="ad39a-359">8320 (0x2080)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-360">Указанный атрибут не существует или не имеет значений.</span><span class="sxs-lookup"><span data-stu-id="ad39a-360">The specified attribute is not present, or has no values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**Ошибка \_ с \_ единственным \_ значением \_ в DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-361"><span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR\_DS\_SINGLE\_VALUE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-362">8321 (0x2081)</span><span class="sxs-lookup"><span data-stu-id="ad39a-362">8321 (0x2081)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-363">Для атрибута было указано несколько значений, которые могут иметь только одно значение.</span><span class="sxs-lookup"><span data-stu-id="ad39a-363">Multiple values were specified for an attribute that can have only one value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**Ошибка \_ \_ ограничения диапазона \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-364"><span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERROR\_DS\_RANGE\_CONSTRAINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-365">8322 (0x2082)</span><span class="sxs-lookup"><span data-stu-id="ad39a-365">8322 (0x2082)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-366">Значение атрибута не находится в допустимом диапазоне значений.</span><span class="sxs-lookup"><span data-stu-id="ad39a-366">A value for the attribute was not in the acceptable range of values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**Ошибка \_ DS \_ Атри \_ Val \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="ad39a-367"><span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERROR\_DS\_ATT\_VAL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-368">8323 (0x2083)</span><span class="sxs-lookup"><span data-stu-id="ad39a-368">8323 (0x2083)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-369">Указанное значение уже существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-369">The specified value already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**Ошибка \_ DS не \_ удается \_ REM \_ отсутствует \_ Атри**</span><span class="sxs-lookup"><span data-stu-id="ad39a-370"><span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-371">8324 (0x2084)</span><span class="sxs-lookup"><span data-stu-id="ad39a-371">8324 (0x2084)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-372">Невозможно удалить атрибут, так как он отсутствует в объекте.</span><span class="sxs-lookup"><span data-stu-id="ad39a-372">The attribute cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**Ошибка \_ DS не \_ удается \_ REM \_ отсутствует \_ Атри \_ Val**</span><span class="sxs-lookup"><span data-stu-id="ad39a-373"><span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR\_DS\_CANT\_REM\_MISSING\_ATT\_VAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-374">8325 (0x2085)</span><span class="sxs-lookup"><span data-stu-id="ad39a-374">8325 (0x2085)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-375">Значение атрибута не может быть удалено, поскольку оно отсутствует в объекте.</span><span class="sxs-lookup"><span data-stu-id="ad39a-375">The attribute value cannot be removed because it is not present on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**Ошибка \_ \_ корня DS \_ \_ не может быть \_ субреф**</span><span class="sxs-lookup"><span data-stu-id="ad39a-376"><span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR\_DS\_ROOT\_CANT\_BE\_SUBREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-377">8326 (0x2086)</span><span class="sxs-lookup"><span data-stu-id="ad39a-377">8326 (0x2086)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-378">Указанный корневой объект не может быть субреф.</span><span class="sxs-lookup"><span data-stu-id="ad39a-378">The specified root object cannot be a subref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**Ошибка \_ DS \_ без \_ цепочек**</span><span class="sxs-lookup"><span data-stu-id="ad39a-379"><span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR\_DS\_NO\_CHAINING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-380">8327 (0x2087)</span><span class="sxs-lookup"><span data-stu-id="ad39a-380">8327 (0x2087)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-381">Цепочки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="ad39a-381">Chaining is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**Ошибка \_ DS \_ без \_ цепочек \_ оценки**</span><span class="sxs-lookup"><span data-stu-id="ad39a-382"><span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR\_DS\_NO\_CHAINED\_EVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-383">8328 (0x2088)</span><span class="sxs-lookup"><span data-stu-id="ad39a-383">8328 (0x2088)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-384">Вычисление цепочек не разрешено.</span><span class="sxs-lookup"><span data-stu-id="ad39a-384">Chained evaluation is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**Ошибка \_ DS \_ без \_ родительского \_ объекта**</span><span class="sxs-lookup"><span data-stu-id="ad39a-385"><span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR\_DS\_NO\_PARENT\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-386">8329 (0x2089)</span><span class="sxs-lookup"><span data-stu-id="ad39a-386">8329 (0x2089)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-387">Эта операция не может быть выполнена, т.к. родитель объекта либо не подтвержден, либо удален.</span><span class="sxs-lookup"><span data-stu-id="ad39a-387">The operation could not be performed because the object's parent is either uninstantiated or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**\_ \_ родительский объект ошибки DS \_ является \_ \_ псевдонимом**</span><span class="sxs-lookup"><span data-stu-id="ad39a-388"><span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERROR\_DS\_PARENT\_IS\_AN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-389">8330 (0x208A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-389">8330 (0x208A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-390">Наличие родителя, который является псевдонимом, не допускается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-390">Having a parent that is an alias is not permitted.</span></span> <span data-ttu-id="ad39a-391">Псевдонимы являются конечными объектами.</span><span class="sxs-lookup"><span data-stu-id="ad39a-391">Aliases are leaf objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**Ошибка \_ DS не \_ удается \_ смешать \_ главный \_ и \_ представители**</span><span class="sxs-lookup"><span data-stu-id="ad39a-392"><span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR\_DS\_CANT\_MIX\_MASTER\_AND\_REPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-393">8331 (0x208B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-393">8331 (0x208B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-394">Объект и родитель должны иметь один и тот же тип: как шаблоны, так и обе реплики.</span><span class="sxs-lookup"><span data-stu-id="ad39a-394">The object and parent must be of the same type, either both masters or both replicas.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**\_ \_ присутствуют дочерние элементы DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-395"><span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR\_DS\_CHILDREN\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-396">8332 (0x208C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-396">8332 (0x208C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-397">Невозможно выполнить операцию, так как существуют дочерние объекты.</span><span class="sxs-lookup"><span data-stu-id="ad39a-397">The operation cannot be performed because child objects exist.</span></span> <span data-ttu-id="ad39a-398">Эта операция может быть выполнена только для конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-398">This operation can only be performed on a leaf object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**Ошибка \_ \_ obj \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-399"><span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERROR\_DS\_OBJ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-400">8333 (0x208D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-400">8333 (0x208D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-401">Объект каталога не найден.</span><span class="sxs-lookup"><span data-stu-id="ad39a-401">Directory object not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**Ошибка \_ в \_ псевдониме \_ obj \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-402"><span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERROR\_DS\_ALIASED\_OBJ\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-403">8334 (0x208E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-403">8334 (0x208E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-404">Отсутствует псевдоним объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-404">The aliased object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**Ошибка \_ в \_ синтаксисе неверного \_ имени DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-405"><span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR\_DS\_BAD\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-406">8335 (0x208F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-406">8335 (0x208F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-407">Недопустимый синтаксис имени объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-407">The object name has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**Ошибка \_ \_ псевдонима \_ DS \_ , указывающая на \_ псевдоним**</span><span class="sxs-lookup"><span data-stu-id="ad39a-408"><span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERROR\_DS\_ALIAS\_POINTS\_TO\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-409">8336 (0x2090)</span><span class="sxs-lookup"><span data-stu-id="ad39a-409">8336 (0x2090)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-410">Псевдоним не может ссылаться на другой псевдоним.</span><span class="sxs-lookup"><span data-stu-id="ad39a-410">It is not permitted for an alias to refer to another alias.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**Ошибка \_ DS не удается выявление \_ \_ \_ псевдонима**</span><span class="sxs-lookup"><span data-stu-id="ad39a-411"><span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR\_DS\_CANT\_DEREF\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-412">8337 (0x2091)</span><span class="sxs-lookup"><span data-stu-id="ad39a-412">8337 (0x2091)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-413">Невозможно разыменование псевдонима.</span><span class="sxs-lookup"><span data-stu-id="ad39a-413">The alias cannot be dereferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**Ошибка \_ DS \_ вне \_ \_ области**</span><span class="sxs-lookup"><span data-stu-id="ad39a-414"><span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR\_DS\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-415">8338 (0x2092)</span><span class="sxs-lookup"><span data-stu-id="ad39a-415">8338 (0x2092)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-416">Операция вне области действия.</span><span class="sxs-lookup"><span data-stu-id="ad39a-416">The operation is out of scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**Ошибка \_ \_ удаления объекта \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-417"><span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR\_DS\_OBJECT\_BEING\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-418">8339 (0x2093)</span><span class="sxs-lookup"><span data-stu-id="ad39a-418">8339 (0x2093)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-419">Невозможно продолжить операцию, так как объект находится в процессе удаления.</span><span class="sxs-lookup"><span data-stu-id="ad39a-419">The operation cannot continue because the object is in the process of being removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**Ошибка \_ DS не \_ удается \_ удалить \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="ad39a-420"><span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR\_DS\_CANT\_DELETE\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-421">8340 (0x2094)</span><span class="sxs-lookup"><span data-stu-id="ad39a-421">8340 (0x2094)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-422">Не удается удалить объект DSA.</span><span class="sxs-lookup"><span data-stu-id="ad39a-422">The DSA object cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**Ошибка \_ DS \_ Generic \_ Error**</span><span class="sxs-lookup"><span data-stu-id="ad39a-423"><span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**ERROR\_DS\_GENERIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-424">8341 (0x2095)</span><span class="sxs-lookup"><span data-stu-id="ad39a-424">8341 (0x2095)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-425">Произошла ошибка службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-425">A directory service error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**Ошибка \_ DSA DS, \_ \_ должна \_ быть \_ \_ хозяином int**</span><span class="sxs-lookup"><span data-stu-id="ad39a-426"><span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR\_DS\_DSA\_MUST\_BE\_INT\_MASTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-427">8342 (0x2096)</span><span class="sxs-lookup"><span data-stu-id="ad39a-427">8342 (0x2096)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-428">Эта операция может быть выполнена только для внутреннего основного объекта DSA.</span><span class="sxs-lookup"><span data-stu-id="ad39a-428">The operation can only be performed on an internal master DSA object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**Ошибка \_ класса DS, \_ \_ не являющийся \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="ad39a-429"><span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR\_DS\_CLASS\_NOT\_DSA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-430">8343 (0x2097)</span><span class="sxs-lookup"><span data-stu-id="ad39a-430">8343 (0x2097)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-431">Объект должен иметь класс DSA.</span><span class="sxs-lookup"><span data-stu-id="ad39a-431">The object must be of class DSA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**Ошибка \_ \_ доступа инсуфф \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-432"><span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERROR\_DS\_INSUFF\_ACCESS\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-433">8344 (0x2098)</span><span class="sxs-lookup"><span data-stu-id="ad39a-433">8344 (0x2098)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-434">Недостаточно прав доступа для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ad39a-434">Insufficient access rights to perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**Ошибка \_ DS — \_ Недопустимый \_ старший**</span><span class="sxs-lookup"><span data-stu-id="ad39a-435"><span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR\_DS\_ILLEGAL\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-436">8345 (0x2099)</span><span class="sxs-lookup"><span data-stu-id="ad39a-436">8345 (0x2099)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-437">Не удается добавить объект, поскольку родительский элемент не находится в списке возможных старших элементов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-437">The object cannot be added because the parent is not on the list of possible superiors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**Ошибка \_ \_ атрибута DS \_ , принадлежащего \_ \_ SAM**</span><span class="sxs-lookup"><span data-stu-id="ad39a-438"><span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERROR\_DS\_ATTRIBUTE\_OWNED\_BY\_SAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-439">8346 (0x209A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-439">8346 (0x209A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-440">Доступ к атрибуту не разрешен, так как атрибут принадлежит диспетчеру учетных записей безопасности (SAM).</span><span class="sxs-lookup"><span data-stu-id="ad39a-440">Access to the attribute is not permitted because the attribute is owned by the Security Accounts Manager (SAM).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**Ошибка \_ \_ имя DS \_ слишком \_ много \_ частей**</span><span class="sxs-lookup"><span data-stu-id="ad39a-441"><span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR\_DS\_NAME\_TOO\_MANY\_PARTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-442">8347 (0x209B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-442">8347 (0x209B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-443">Имя содержит слишком много частей.</span><span class="sxs-lookup"><span data-stu-id="ad39a-443">The name has too many parts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**Ошибка \_ \_ \_ слишком \_ длинное имя DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-444"><span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR\_DS\_NAME\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-445">8348 (0x209C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-445">8348 (0x209C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-446">Слишком длинное имя.</span><span class="sxs-lookup"><span data-stu-id="ad39a-446">The name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**Ошибка \_ \_ \_ \_ слишком \_ длинное значение имени DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-447"><span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERROR\_DS\_NAME\_VALUE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-448">8349 (0x209D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-448">8349 (0x209D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-449">Значение имени слишком длинное.</span><span class="sxs-lookup"><span data-stu-id="ad39a-449">The name value is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**Ошибка \_ при \_ \_ разборе имени DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-450"><span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR\_DS\_NAME\_UNPARSEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-451">8350 (0x209E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-451">8350 (0x209E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-452">Произошла ошибка службы каталогов при анализе имени.</span><span class="sxs-lookup"><span data-stu-id="ad39a-452">The directory service encountered an error parsing a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**Ошибка \_ \_ \_ \_ неизвестного типа имени DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-453"><span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR\_DS\_NAME\_TYPE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-454">8351 (0x209F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-454">8351 (0x209F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-455">Служба каталогов не может получить тип атрибута для имени.</span><span class="sxs-lookup"><span data-stu-id="ad39a-455">The directory service cannot get the attribute type for a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**Ошибка \_ DS \_ \_ , не \_ объект**</span><span class="sxs-lookup"><span data-stu-id="ad39a-456"><span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR\_DS\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-457">8352 (0x20A0)</span><span class="sxs-lookup"><span data-stu-id="ad39a-457">8352 (0x20A0)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-458">Имя не определяет объект; имя идентифицирует фантом.</span><span class="sxs-lookup"><span data-stu-id="ad39a-458">The name does not identify an object; the name identifies a phantom.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ОШИБКИ \_ в \_ секунду \_ , \_ слишком \_ короткий**</span><span class="sxs-lookup"><span data-stu-id="ad39a-459"><span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR\_DS\_SEC\_DESC\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-460">8353 (0x20A1)</span><span class="sxs-lookup"><span data-stu-id="ad39a-460">8353 (0x20A1)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-461">Слишком короткий дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="ad39a-461">The security descriptor is too short.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**Ошибка \_ \_ \_ \_ недопустимых DESC в секунду**</span><span class="sxs-lookup"><span data-stu-id="ad39a-462"><span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR\_DS\_SEC\_DESC\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-463">8354 (0x20A2)</span><span class="sxs-lookup"><span data-stu-id="ad39a-463">8354 (0x20A2)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-464">Недопустимый дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="ad39a-464">The security descriptor is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**Ошибка \_ DS \_ без \_ удаленного \_ имени**</span><span class="sxs-lookup"><span data-stu-id="ad39a-465"><span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR\_DS\_NO\_DELETED\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-466">8355 (0x20A3)</span><span class="sxs-lookup"><span data-stu-id="ad39a-466">8355 (0x20A3)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-467">Не удалось создать имя для удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-467">Failed to create name for deleted object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**Ошибка \_ DS \_ субреф \_ должна \_ иметь \_ родителя**</span><span class="sxs-lookup"><span data-stu-id="ad39a-468"><span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERROR\_DS\_SUBREF\_MUST\_HAVE\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-469">8356 (0x20A4)</span><span class="sxs-lookup"><span data-stu-id="ad39a-469">8356 (0x20A4)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-470">Должен существовать родительский элемент нового субреф.</span><span class="sxs-lookup"><span data-stu-id="ad39a-470">The parent of a new subref must exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**Ошибка \_ доменных служб Active Directory ( \_ NCNAME) \_ должна \_ быть \_ NC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-471"><span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR\_DS\_NCNAME\_MUST\_BE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-472">8357 (0x20A5)</span><span class="sxs-lookup"><span data-stu-id="ad39a-472">8357 (0x20A5)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-473">Объект должен быть контекстом именования.</span><span class="sxs-lookup"><span data-stu-id="ad39a-473">The object must be a naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**Ошибка \_ DS \_ не \_ удается \_ Добавить \_ только систему**</span><span class="sxs-lookup"><span data-stu-id="ad39a-474"><span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR\_DS\_CANT\_ADD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-475">8358 (0x20A6)</span><span class="sxs-lookup"><span data-stu-id="ad39a-475">8358 (0x20A6)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-476">Не разрешается добавлять атрибут, принадлежащий системе.</span><span class="sxs-lookup"><span data-stu-id="ad39a-476">It is not permitted to add an attribute which is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**класс DS с ОШИБКАми \_ \_ \_ должен \_ быть \_ конкретным**</span><span class="sxs-lookup"><span data-stu-id="ad39a-477"><span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**ERROR\_DS\_CLASS\_MUST\_BE\_CONCRETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-478">8359 (0x20A7)</span><span class="sxs-lookup"><span data-stu-id="ad39a-478">8359 (0x20A7)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-479">Класс объекта должен быть структурным; нельзя создать экземпляр абстрактного класса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-479">The class of the object must be structural; you cannot instantiate an abstract class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**Ошибка \_ DS \_ Недопустимая \_ ДМД**</span><span class="sxs-lookup"><span data-stu-id="ad39a-480"><span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR\_DS\_INVALID\_DMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-481">8360 (0x20A8)</span><span class="sxs-lookup"><span data-stu-id="ad39a-481">8360 (0x20A8)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-482">Не удалось найти объект схемы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-482">The schema object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**Ошибка \_ - \_ \_ идентификатор GUID DS obj \_ существует**</span><span class="sxs-lookup"><span data-stu-id="ad39a-483"><span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERROR\_DS\_OBJ\_GUID\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-484">8361 (0x20A9)</span><span class="sxs-lookup"><span data-stu-id="ad39a-484">8361 (0x20A9)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-485">Локальный объект с этим идентификатором GUID (Мертвое или неактивное) уже существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-485">A local object with this GUID (dead or alive) already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**Ошибка \_ DS \_ , \_ не \_ посмотрите**</span><span class="sxs-lookup"><span data-stu-id="ad39a-486"><span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR\_DS\_NOT\_ON\_BACKLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-487">8362 (0x20AA)</span><span class="sxs-lookup"><span data-stu-id="ad39a-487">8362 (0x20AA)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-488">Операция не может быть выполнена на обратной ссылке.</span><span class="sxs-lookup"><span data-stu-id="ad39a-488">The operation cannot be performed on a back link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**Ошибка \_ DS \_ без \_ CROSSREF \_ для \_ NC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-489"><span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR\_DS\_NO\_CROSSREF\_FOR\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-490">8363 (0x20AB)</span><span class="sxs-lookup"><span data-stu-id="ad39a-490">8363 (0x20AB)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-491">Перекрестная ссылка для указанного контекста именования не найдена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-491">The cross reference for the specified naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**Ошибка \_ при \_ завершении работы DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-492"><span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR\_DS\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-493">8364 (0x20AC)</span><span class="sxs-lookup"><span data-stu-id="ad39a-493">8364 (0x20AC)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-494">Не удалось выполнить операцию, так как служба каталогов завершает работу.</span><span class="sxs-lookup"><span data-stu-id="ad39a-494">The operation could not be performed because the directory service is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**Ошибка \_ \_ неизвестной \_ операции DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-495"><span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR\_DS\_UNKNOWN\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-496">8365 (0x20AD)</span><span class="sxs-lookup"><span data-stu-id="ad39a-496">8365 (0x20AD)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-497">Недопустимый запрос службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-497">The directory service request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**Ошибка \_ DS, \_ Недопустимая \_ \_ владелец роли**</span><span class="sxs-lookup"><span data-stu-id="ad39a-498"><span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR\_DS\_INVALID\_ROLE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-499">8366 (0x20AE)</span><span class="sxs-lookup"><span data-stu-id="ad39a-499">8366 (0x20AE)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-500">Не удалось прочитать атрибут владельца роли.</span><span class="sxs-lookup"><span data-stu-id="ad39a-500">The role owner attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**Ошибка \_ DS \_ не удалось \_ Contact \_ FSMO**</span><span class="sxs-lookup"><span data-stu-id="ad39a-501"><span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR\_DS\_COULDNT\_CONTACT\_FSMO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-502">8367 (0x20AF)</span><span class="sxs-lookup"><span data-stu-id="ad39a-502">8367 (0x20AF)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-503">Ошибка требуемой операции FSMO.</span><span class="sxs-lookup"><span data-stu-id="ad39a-503">The requested FSMO operation failed.</span></span> <span data-ttu-id="ad39a-504">Нет связи с текущим владельцем FSMO.</span><span class="sxs-lookup"><span data-stu-id="ad39a-504">The current FSMO holder could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**Ошибка \_ \_ \_ \_ переименования DN перекрестного сетевого контроллера в DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-505"><span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR\_DS\_CROSS\_NC\_DN\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-506">8368 (0x20B0)</span><span class="sxs-lookup"><span data-stu-id="ad39a-506">8368 (0x20B0)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-507">Изменение DN в контексте именования не допускается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-507">Modification of a DN across a naming context is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**Ошибка \_ DS \_ не \_ удается \_ только система Mod \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-508"><span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR\_DS\_CANT\_MOD\_SYSTEM\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-509">8369 (0x20B1)</span><span class="sxs-lookup"><span data-stu-id="ad39a-509">8369 (0x20B1)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-510">Невозможно изменить атрибут, так как он принадлежит системе.</span><span class="sxs-lookup"><span data-stu-id="ad39a-510">The attribute cannot be modified because it is owned by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**Ошибка \_ \_ репликатора \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-511"><span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR\_DS\_REPLICATOR\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-512">8370 (0x20B2)</span><span class="sxs-lookup"><span data-stu-id="ad39a-512">8370 (0x20B2)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-513">Эту функцию могут выполнять только репликатор.</span><span class="sxs-lookup"><span data-stu-id="ad39a-513">Only the replicator can perform this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**Ошибка \_ в \_ классе obj DS \_ \_ не \_ определена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-514"><span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-515">8371 (0x20B3)</span><span class="sxs-lookup"><span data-stu-id="ad39a-515">8371 (0x20B3)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-516">Указанный класс не определен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-516">The specified class is not defined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**Ошибка \_ - \_ \_ подкласс для класса obj \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-517"><span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR\_DS\_OBJ\_CLASS\_NOT\_SUBCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-518">8372 (0x20B4)</span><span class="sxs-lookup"><span data-stu-id="ad39a-518">8372 (0x20B4)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-519">Указанный класс не является подклассом.</span><span class="sxs-lookup"><span data-stu-id="ad39a-519">The specified class is not a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**Ошибка \_ \_ \_ Недопустимая ссылка на имя DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-520"><span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR\_DS\_NAME\_REFERENCE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-521">8373 (0x20B5)</span><span class="sxs-lookup"><span data-stu-id="ad39a-521">8373 (0x20B5)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-522">Недопустимая ссылка на имя.</span><span class="sxs-lookup"><span data-stu-id="ad39a-522">The name reference is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**\_существует ошибка \_ перекрестной \_ ссылки DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-523"><span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERROR\_DS\_CROSS\_REF\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-524">8374 (0x20B6)</span><span class="sxs-lookup"><span data-stu-id="ad39a-524">8374 (0x20B6)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-525">Перекрестная ссылка уже существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-525">A cross reference already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ОШИБКА DS не удается присвоить \_ \_ \_ \_ главному узлу Del \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-526"><span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR\_DS\_CANT\_DEL\_MASTER\_CROSSREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-527">8375 (0x20B7)</span><span class="sxs-lookup"><span data-stu-id="ad39a-527">8375 (0x20B7)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-528">Удаление главной перекрестной ссылки не допускается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-528">It is not permitted to delete a master cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**сообщение об ошибке поддерево "ошибка" \_ \_ \_ \_ не \_ \_ head NC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-529"><span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR\_DS\_SUBTREE\_NOTIFY\_NOT\_NC\_HEAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-530">8376 (0x20B8)</span><span class="sxs-lookup"><span data-stu-id="ad39a-530">8376 (0x20B8)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-531">Уведомления поддерева поддерживаются только в заголовках NC.</span><span class="sxs-lookup"><span data-stu-id="ad39a-531">Subtree notifications are only supported on NC heads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**\_ \_ \_ \_ слишком сложный фильтр уведомлений DS \_ с ошибками**</span><span class="sxs-lookup"><span data-stu-id="ad39a-532"><span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR\_DS\_NOTIFY\_FILTER\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-533">8377 (0x20B9)</span><span class="sxs-lookup"><span data-stu-id="ad39a-533">8377 (0x20B9)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-534">Слишком сложный фильтр уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ad39a-534">Notification filter is too complex.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**Ошибка \_ DS \_ DUP \_ RDN**</span><span class="sxs-lookup"><span data-stu-id="ad39a-535"><span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR\_DS\_DUP\_RDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-536">8378 (0x20BA)</span><span class="sxs-lookup"><span data-stu-id="ad39a-536">8378 (0x20BA)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-537">Ошибка обновления схемы: повторяющееся RDN.</span><span class="sxs-lookup"><span data-stu-id="ad39a-537">Schema update failed: duplicate RDN.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**Ошибка \_ DS \_ DUP \_ OID**</span><span class="sxs-lookup"><span data-stu-id="ad39a-538"><span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR\_DS\_DUP\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-539">8379 (0x20BB)</span><span class="sxs-lookup"><span data-stu-id="ad39a-539">8379 (0x20BB)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-540">Сбой обновления схемы: дублирующийся OID.</span><span class="sxs-lookup"><span data-stu-id="ad39a-540">Schema update failed: duplicate OID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**Ошибка \_ DS \_ DUP \_ MAPI \_ ID**</span><span class="sxs-lookup"><span data-stu-id="ad39a-541"><span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERROR\_DS\_DUP\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-542">8380 (0x20BC)</span><span class="sxs-lookup"><span data-stu-id="ad39a-542">8380 (0x20BC)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-543">Сбой обновления схемы: дублирующийся идентификатор MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad39a-543">Schema update failed: duplicate MAPI identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**Ошибка \_ DS \_ DUP \_ Schema \_ ID \_ GUID**</span><span class="sxs-lookup"><span data-stu-id="ad39a-544"><span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR\_DS\_DUP\_SCHEMA\_ID\_GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-545">8381 (0x20BD)</span><span class="sxs-lookup"><span data-stu-id="ad39a-545">8381 (0x20BD)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-546">Сбой обновления схемы: идентификатор GUID схемы дублируется.</span><span class="sxs-lookup"><span data-stu-id="ad39a-546">Schema update failed: duplicate schema-id GUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**Ошибка \_ DS \_ DUP \_ , \_ отображаемое \_ имя LDAP**</span><span class="sxs-lookup"><span data-stu-id="ad39a-547"><span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR\_DS\_DUP\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-548">8382 (0x20BE)</span><span class="sxs-lookup"><span data-stu-id="ad39a-548">8382 (0x20BE)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-549">Ошибка обновления схемы: повторяющееся отображаемое имя LDAP.</span><span class="sxs-lookup"><span data-stu-id="ad39a-549">Schema update failed: duplicate LDAP display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**Ошибка \_ \_ проверки семантического \_ Атри DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-550"><span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR\_DS\_SEMANTIC\_ATT\_TEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-551">8383 (0x20BF)</span><span class="sxs-lookup"><span data-stu-id="ad39a-551">8383 (0x20BF)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-552">Сбой обновления схемы: диапазон-меньше, чем диапазон верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="ad39a-552">Schema update failed: range-lower less than range upper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**Ошибка \_ при \_ несоответствии синтаксиса DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-553"><span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR\_DS\_SYNTAX\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-554">8384 (0x20C0)</span><span class="sxs-lookup"><span data-stu-id="ad39a-554">8384 (0x20C0)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-555">Не удалось обновить схему: несовпадение синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-555">Schema update failed: syntax mismatch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**Ошибка \_ DS \_ Exists \_ в \_ должен \_ иметь**</span><span class="sxs-lookup"><span data-stu-id="ad39a-556"><span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**ERROR\_DS\_EXISTS\_IN\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-557">8385 (0x20C1)</span><span class="sxs-lookup"><span data-stu-id="ad39a-557">8385 (0x20C1)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-558">Сбой удаления схемы: атрибут используется в, который должен содержать.</span><span class="sxs-lookup"><span data-stu-id="ad39a-558">Schema deletion failed: attribute is used in must-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**\_ \_ \_ в \_ возможно \_ , существует ошибка DS в**</span><span class="sxs-lookup"><span data-stu-id="ad39a-559"><span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**ERROR\_DS\_EXISTS\_IN\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-560">8386 (0x20C2)</span><span class="sxs-lookup"><span data-stu-id="ad39a-560">8386 (0x20C2)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-561">Сбой удаления схемы: в возможно, используется атрибут, который содержит.</span><span class="sxs-lookup"><span data-stu-id="ad39a-561">Schema deletion failed: attribute is used in may-contain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**\_ \_ несуществующая ошибка \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-562"><span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERROR\_DS\_NONEXISTENT\_MAY\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-563">8387 (0x20C3)</span><span class="sxs-lookup"><span data-stu-id="ad39a-563">8387 (0x20C3)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-564">Ошибка обновления схемы: атрибут в, возможно, не существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-564">Schema update failed: attribute in may-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**\_НЕсуществующая ошибка DS \_ \_ должна \_ иметь**</span><span class="sxs-lookup"><span data-stu-id="ad39a-565"><span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERROR\_DS\_NONEXISTENT\_MUST\_HAVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-566">8388 (0x20C4)</span><span class="sxs-lookup"><span data-stu-id="ad39a-566">8388 (0x20C4)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-567">Не удалось обновить схему: атрибут в "" должно быть не существует ".</span><span class="sxs-lookup"><span data-stu-id="ad39a-567">Schema update failed: attribute in must-contain does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**Ошибка \_ при \_ \_ проверке AUX \_ CLS \_ в DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-568"><span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR\_DS\_AUX\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-569">8389 (0x20C5)</span><span class="sxs-lookup"><span data-stu-id="ad39a-569">8389 (0x20C5)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-570">Сбой обновления схемы: класс в списке AUX-Class не существует или не является вспомогательным классом.</span><span class="sxs-lookup"><span data-stu-id="ad39a-570">Schema update failed: class in aux-class list does not exist or is not an auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**Ошибка \_ DS, \_ несуществующая \_ ПОСС \_ SUP**</span><span class="sxs-lookup"><span data-stu-id="ad39a-571"><span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR\_DS\_NONEXISTENT\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-572">8390 (0x20C6)</span><span class="sxs-lookup"><span data-stu-id="ad39a-572">8390 (0x20C6)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-573">Сбой обновления схемы: класс в ПОСС-старших не существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-573">Schema update failed: class in poss-superiors does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ОШИБКА подсистемы проверки подсистемы \_ CLS в DS \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-574"><span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR\_DS\_SUB\_CLS\_TEST\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-575">8391 (0x20C7)</span><span class="sxs-lookup"><span data-stu-id="ad39a-575">8391 (0x20C7)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-576">Сбой обновления схемы: класс в списке списках subClassOf не существует или не удовлетворяет правилам иерархии.</span><span class="sxs-lookup"><span data-stu-id="ad39a-576">Schema update failed: class in subclassof list does not exist or does not satisfy hierarchy rules.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**Ошибка \_ DS \_ неверного \_ \_ \_ синтаксиса идентификатора RDN Атри \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-577"><span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR\_DS\_BAD\_RDN\_ATT\_ID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-578">8392 (0x20C8)</span><span class="sxs-lookup"><span data-stu-id="ad39a-578">8392 (0x20C8)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-579">Сбой обновления схемы: RDN-Атри-ID имеет неправильный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="ad39a-579">Schema update failed: Rdn-Att-Id has wrong syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**\_ \_ \_ в \_ AUX \_ CLS существует ошибка DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-580"><span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERROR\_DS\_EXISTS\_IN\_AUX\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-581">8393 (0x20C9)</span><span class="sxs-lookup"><span data-stu-id="ad39a-581">8393 (0x20C9)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-582">Сбой удаления схемы: класс используется в качестве вспомогательного класса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-582">Schema deletion failed: class is used as auxiliary class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**\_ \_ \_ в \_ подсистеме \_ CLS существует ошибка DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-583"><span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERROR\_DS\_EXISTS\_IN\_SUB\_CLS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-584">8394 (0x20CA)</span><span class="sxs-lookup"><span data-stu-id="ad39a-584">8394 (0x20CA)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-585">Сбой удаления схемы: класс используется как подкласс.</span><span class="sxs-lookup"><span data-stu-id="ad39a-585">Schema deletion failed: class is used as sub class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**\_ \_ \_ в \_ ПОСС \_ SUP существует ошибка DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-586"><span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERROR\_DS\_EXISTS\_IN\_POSS\_SUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-587">8395 (0x20CB)</span><span class="sxs-lookup"><span data-stu-id="ad39a-587">8395 (0x20CB)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-588">Сбой удаления схемы: класс используется как ПОСС старший.</span><span class="sxs-lookup"><span data-stu-id="ad39a-588">Schema deletion failed: class is used as poss superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**Ошибка \_ DS \_ рекалксчема \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-589"><span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR\_DS\_RECALCSCHEMA\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-590">8396 (0x20CC)</span><span class="sxs-lookup"><span data-stu-id="ad39a-590">8396 (0x20CC)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-591">Сбой обновления схемы при повторном вычислении кэша проверки.</span><span class="sxs-lookup"><span data-stu-id="ad39a-591">Schema update failed in recalculating validation cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**Ошибка \_ при \_ \_ удалении дерева \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-592"><span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR\_DS\_TREE\_DELETE\_NOT\_FINISHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-593">8397 (0x20CD)</span><span class="sxs-lookup"><span data-stu-id="ad39a-593">8397 (0x20CD)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-594">Удаление дерева не завершено.</span><span class="sxs-lookup"><span data-stu-id="ad39a-594">The tree deletion is not finished.</span></span> <span data-ttu-id="ad39a-595">Чтобы продолжить удаление дерева, необходимо снова выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="ad39a-595">The request must be made again to continue deleting the tree.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**Ошибка \_ при \_ \_ удалении DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-596"><span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR\_DS\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-597">8398 (0x20CE)</span><span class="sxs-lookup"><span data-stu-id="ad39a-597">8398 (0x20CE)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-598">Не удалось выполнить запрошенную операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="ad39a-598">The requested delete operation could not be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**Ошибка \_ \_ \_ \_ ИД требования схемы DS \_ Атри**</span><span class="sxs-lookup"><span data-stu-id="ad39a-599"><span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-600">8399 (0x20CF)</span><span class="sxs-lookup"><span data-stu-id="ad39a-600">8399 (0x20CF)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-601">Не удается прочитать идентификатор класса управляемых классов для записи схемы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-601">Cannot read the governs class identifier for the schema record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**Ошибка \_ DS \_ Bad \_ Атри \_ \_ синтаксис схемы**</span><span class="sxs-lookup"><span data-stu-id="ad39a-602"><span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR\_DS\_BAD\_ATT\_SCHEMA\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-603">8400 (0x20D0)</span><span class="sxs-lookup"><span data-stu-id="ad39a-603">8400 (0x20D0)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-604">Схема атрибута имеет неверный синтаксис.</span><span class="sxs-lookup"><span data-stu-id="ad39a-604">The attribute schema has bad syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**Ошибка \_ DS не \_ удается \_ кэшировать \_ Атри**</span><span class="sxs-lookup"><span data-stu-id="ad39a-605"><span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR\_DS\_CANT\_CACHE\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-606">8401 (0x20D1)</span><span class="sxs-lookup"><span data-stu-id="ad39a-606">8401 (0x20D1)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-607">Не удалось кэшировать атрибут.</span><span class="sxs-lookup"><span data-stu-id="ad39a-607">The attribute could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**Ошибка \_ DS не \_ удается \_ кэшировать \_ класс**</span><span class="sxs-lookup"><span data-stu-id="ad39a-608"><span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR\_DS\_CANT\_CACHE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-609">8402 (0x20D2)</span><span class="sxs-lookup"><span data-stu-id="ad39a-609">8402 (0x20D2)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-610">Не удалось кэшировать класс.</span><span class="sxs-lookup"><span data-stu-id="ad39a-610">The class could not be cached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**Ошибка \_ DS \_ не \_ удается \_ удалить \_ кэш Атри**</span><span class="sxs-lookup"><span data-stu-id="ad39a-611"><span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_ATT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-612">8403 (0x20D3)</span><span class="sxs-lookup"><span data-stu-id="ad39a-612">8403 (0x20D3)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-613">Не удалось удалить атрибут из кэша.</span><span class="sxs-lookup"><span data-stu-id="ad39a-613">The attribute could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**Ошибка \_ DS \_ не \_ удается \_ удалить \_ кэш класса**</span><span class="sxs-lookup"><span data-stu-id="ad39a-614"><span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR\_DS\_CANT\_REMOVE\_CLASS\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-615">8404 (0x20D4)</span><span class="sxs-lookup"><span data-stu-id="ad39a-615">8404 (0x20D4)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-616">Не удалось удалить класс из кэша.</span><span class="sxs-lookup"><span data-stu-id="ad39a-616">The class could not be removed from the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**Ошибка \_ DS не \_ удается \_ получить \_ различающееся имя**</span><span class="sxs-lookup"><span data-stu-id="ad39a-617"><span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR\_DS\_CANT\_RETRIEVE\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-618">8405 (0x20D5)</span><span class="sxs-lookup"><span data-stu-id="ad39a-618">8405 (0x20D5)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-619">Не удалось прочитать атрибут различающегося имени.</span><span class="sxs-lookup"><span data-stu-id="ad39a-619">The distinguished name attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**Ошибка \_ DS \_ Missing \_ супреф**</span><span class="sxs-lookup"><span data-stu-id="ad39a-620"><span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR\_DS\_MISSING\_SUPREF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-621">8406 (0x20D6)</span><span class="sxs-lookup"><span data-stu-id="ad39a-621">8406 (0x20D6)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-622">No superior reference has been configured for the directory service (Для службы каталогов не была настроена ссылка верхнего уровня).</span><span class="sxs-lookup"><span data-stu-id="ad39a-622">No superior reference has been configured for the directory service.</span></span> <span data-ttu-id="ad39a-623">Поэтому служба каталогов не может выдавать ссылки на объекты, находящиеся за пределами этого леса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-623">The directory service is therefore unable to issue referrals to objects outside this forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**Ошибка \_ DS не \_ удается \_ получить \_ экземпляр**</span><span class="sxs-lookup"><span data-stu-id="ad39a-624"><span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR\_DS\_CANT\_RETRIEVE\_INSTANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-625">8407 (0x20D7)</span><span class="sxs-lookup"><span data-stu-id="ad39a-625">8407 (0x20D7)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-626">Не удалось получить атрибут типа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ad39a-626">The instance type attribute could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**Ошибка \_ \_ \_ несогласованности кода DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-627"><span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERROR\_DS\_CODE\_INCONSISTENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-628">8408 (0x20D8)</span><span class="sxs-lookup"><span data-stu-id="ad39a-628">8408 (0x20D8)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-629">Произошла внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="ad39a-629">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**Ошибка \_ \_ базы данных \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-630"><span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**ERROR\_DS\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-631">8409 (0x20D9)</span><span class="sxs-lookup"><span data-stu-id="ad39a-631">8409 (0x20D9)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-632">Произошла ошибка базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad39a-632">A database error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**\_ \_ отсутствует GOVERNSID DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-633"><span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR\_DS\_GOVERNSID\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-634">8410 (0x20DA)</span><span class="sxs-lookup"><span data-stu-id="ad39a-634">8410 (0x20DA)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-635">Отсутствует атрибут GOVERNSID.</span><span class="sxs-lookup"><span data-stu-id="ad39a-635">The attribute GOVERNSID is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**в \_ DS обнаружено \_ \_ непредвиденных \_ Атри**</span><span class="sxs-lookup"><span data-stu-id="ad39a-636"><span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR\_DS\_MISSING\_EXPECTED\_ATT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-637">8411 (0x20DB)</span><span class="sxs-lookup"><span data-stu-id="ad39a-637">8411 (0x20DB)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-638">Отсутствует ожидаемый атрибут.</span><span class="sxs-lookup"><span data-stu-id="ad39a-638">An expected attribute is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**Ошибка \_ в \_ DS \_ NCNAME \_ отсутствует \_ ссылка CR**</span><span class="sxs-lookup"><span data-stu-id="ad39a-639"><span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR\_DS\_NCNAME\_MISSING\_CR\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-640">8412 (0x20DC)</span><span class="sxs-lookup"><span data-stu-id="ad39a-640">8412 (0x20DC)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-641">В указанном контексте именования отсутствует перекрестная ссылка.</span><span class="sxs-lookup"><span data-stu-id="ad39a-641">The specified naming context is missing a cross reference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**Ошибка \_ \_ проверки безопасности \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-642"><span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**ERROR\_DS\_SECURITY\_CHECKING\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-643">8413 (0x20DD)</span><span class="sxs-lookup"><span data-stu-id="ad39a-643">8413 (0x20DD)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-644">Произошла ошибка проверки безопасности.</span><span class="sxs-lookup"><span data-stu-id="ad39a-644">A security checking error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**\_схема DS \_ ошибки \_ не \_ загружена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-645"><span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERROR\_DS\_SCHEMA\_NOT\_LOADED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-646">8414 (0x20DE)</span><span class="sxs-lookup"><span data-stu-id="ad39a-646">8414 (0x20DE)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-647">Схема не загружена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-647">The schema is not loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**Ошибка \_ при выделении \_ схемы DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-648"><span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR\_DS\_SCHEMA\_ALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-649">8415 (0x20DF)</span><span class="sxs-lookup"><span data-stu-id="ad39a-649">8415 (0x20DF)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-650">Не удалось выделить схему.</span><span class="sxs-lookup"><span data-stu-id="ad39a-650">Schema allocation failed.</span></span> <span data-ttu-id="ad39a-651">Убедитесь, что на компьютере недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="ad39a-651">Please check if the machine is running low on memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**Ошибка \_ \_ \_ \_ синтаксиса требования схемы DS Атри \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-652"><span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR\_DS\_ATT\_SCHEMA\_REQ\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-653">8416 (0x20E0)</span><span class="sxs-lookup"><span data-stu-id="ad39a-653">8416 (0x20E0)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-654">Не удалось получить необходимый синтаксис для схемы атрибута.</span><span class="sxs-lookup"><span data-stu-id="ad39a-654">Failed to obtain the required syntax for the attribute schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**Ошибка \_ DS \_ гкверифи \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-655"><span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**ERROR\_DS\_GCVERIFY\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-656">8417 (0x20E1)</span><span class="sxs-lookup"><span data-stu-id="ad39a-656">8417 (0x20E1)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-657">Сбой проверки глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="ad39a-657">The global catalog verification failed.</span></span> <span data-ttu-id="ad39a-658">Глобальный каталог недоступен или не поддерживает эту операцию.</span><span class="sxs-lookup"><span data-stu-id="ad39a-658">The global catalog is not available or does not support the operation.</span></span> <span data-ttu-id="ad39a-659">В настоящее время часть каталога недоступна.</span><span class="sxs-lookup"><span data-stu-id="ad39a-659">Some part of the directory is currently not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**Ошибка \_ \_ \_ несоответствия схемы DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-660"><span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR\_DS\_DRA\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-661">8418 (0x20E2)</span><span class="sxs-lookup"><span data-stu-id="ad39a-661">8418 (0x20E2)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-662">Сбой операции репликации из-за несоответствия схем между вовлеченными серверами.</span><span class="sxs-lookup"><span data-stu-id="ad39a-662">The replication operation failed because of a schema mismatch between the servers involved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**Ошибка \_ DS не \_ удается \_ найти \_ DSA \_ obj**</span><span class="sxs-lookup"><span data-stu-id="ad39a-663"><span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR\_DS\_CANT\_FIND\_DSA\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-664">8419 (0x20E3)</span><span class="sxs-lookup"><span data-stu-id="ad39a-664">8419 (0x20E3)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-665">Не удалось найти объект DSA.</span><span class="sxs-lookup"><span data-stu-id="ad39a-665">The DSA object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**Ошибка \_ DS не \_ удается \_ найти \_ Ожидаемый \_ NC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-666"><span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR\_DS\_CANT\_FIND\_EXPECTED\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-667">8420 (0x20E4)</span><span class="sxs-lookup"><span data-stu-id="ad39a-667">8420 (0x20E4)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-668">Не удалось найти контекст именования.</span><span class="sxs-lookup"><span data-stu-id="ad39a-668">The naming context could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**Ошибка \_ DS не \_ удается \_ найти \_ NC \_ в \_ кэше**</span><span class="sxs-lookup"><span data-stu-id="ad39a-669"><span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR\_DS\_CANT\_FIND\_NC\_IN\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-670">8421 (0x20E5)</span><span class="sxs-lookup"><span data-stu-id="ad39a-670">8421 (0x20E5)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-671">Не удалось найти контекст именования в кэше.</span><span class="sxs-lookup"><span data-stu-id="ad39a-671">The naming context could not be found in the cache.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**Ошибка \_ DS не \_ удается \_ получить \_ дочерний элемент**</span><span class="sxs-lookup"><span data-stu-id="ad39a-672"><span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR\_DS\_CANT\_RETRIEVE\_CHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-673">8422 (0x20E6)</span><span class="sxs-lookup"><span data-stu-id="ad39a-673">8422 (0x20E6)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-674">Не удалось получить дочерний объект.</span><span class="sxs-lookup"><span data-stu-id="ad39a-674">The child object could not be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**Ошибка \_ при \_ \_ недопустимом \_ изменении безопасности DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-675"><span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR\_DS\_SECURITY\_ILLEGAL\_MODIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-676">8423 (0x20E7)</span><span class="sxs-lookup"><span data-stu-id="ad39a-676">8423 (0x20E7)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-677">Это изменение не было разрешено в целях безопасности.</span><span class="sxs-lookup"><span data-stu-id="ad39a-677">The modification was not permitted for security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**Ошибка \_ DS не \_ удается \_ заменить \_ скрытый \_ REC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-678"><span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR\_DS\_CANT\_REPLACE\_HIDDEN\_REC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-679">8424 (0x20E8)</span><span class="sxs-lookup"><span data-stu-id="ad39a-679">8424 (0x20E8)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-680">Операция не может заменить скрытую запись.</span><span class="sxs-lookup"><span data-stu-id="ad39a-680">The operation cannot replace the hidden record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**Ошибка \_ DS — \_ файл неправильной \_ иерархии \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-681"><span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERROR\_DS\_BAD\_HIERARCHY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-682">8425 (0x20E9)</span><span class="sxs-lookup"><span data-stu-id="ad39a-682">8425 (0x20E9)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-683">Недопустимый файл иерархии.</span><span class="sxs-lookup"><span data-stu-id="ad39a-683">The hierarchy file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**Ошибка \_ \_ \_ \_ при выполнении таблицы иерархии сборки DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-684"><span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR\_DS\_BUILD\_HIERARCHY\_TABLE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-685">8426 (0x20EA)</span><span class="sxs-lookup"><span data-stu-id="ad39a-685">8426 (0x20EA)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-686">Не удалось выполнить сборку таблицы иерархии.</span><span class="sxs-lookup"><span data-stu-id="ad39a-686">The attempt to build the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**Ошибка \_ в \_ \_ параметре конфигурации DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-687"><span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR\_DS\_CONFIG\_PARAM\_MISSING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-688">8427 (0x20EB)</span><span class="sxs-lookup"><span data-stu-id="ad39a-688">8427 (0x20EB)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-689">В реестре отсутствует параметр конфигурации каталога.</span><span class="sxs-lookup"><span data-stu-id="ad39a-689">The directory configuration parameter is missing from the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**Ошибка \_ \_ при подсчете \_ \_ индексов адресной книги \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-690"><span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR\_DS\_COUNTING\_AB\_INDICES\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-691">8428 (0x20EC)</span><span class="sxs-lookup"><span data-stu-id="ad39a-691">8428 (0x20EC)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-692">Попытка подсчитать индексы адресной книги не удалась.</span><span class="sxs-lookup"><span data-stu-id="ad39a-692">The attempt to count the address book indices failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**Ошибка \_ \_ \_ \_ malloc \_ при выполнении таблицы иерархии DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-693"><span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_MALLOC\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-694">8429 (со 0x20)</span><span class="sxs-lookup"><span data-stu-id="ad39a-694">8429 (0x20ED)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-695">Не удалось выделить таблицу иерархии.</span><span class="sxs-lookup"><span data-stu-id="ad39a-695">The allocation of the hierarchy table failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**Ошибка \_ \_ внутреннего \_ сбоя DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-696"><span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR\_DS\_INTERNAL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-697">8430 (0x20)</span><span class="sxs-lookup"><span data-stu-id="ad39a-697">8430 (0x20EE)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-698">Произошла внутренняя ошибка службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-698">The directory service encountered an internal failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**Ошибка \_ DS \_ Unknown \_ Error**</span><span class="sxs-lookup"><span data-stu-id="ad39a-699"><span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**ERROR\_DS\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-700">8431 (0x20EF)</span><span class="sxs-lookup"><span data-stu-id="ad39a-700">8431 (0x20EF)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-701">Произошла неизвестная ошибка службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-701">The directory service encountered an unknown failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**\_корень DS \_ ошибки \_ требует указания \_ класса \_ Top**</span><span class="sxs-lookup"><span data-stu-id="ad39a-702"><span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERROR\_DS\_ROOT\_REQUIRES\_CLASS\_TOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-703">8432 (0x20F0)</span><span class="sxs-lookup"><span data-stu-id="ad39a-703">8432 (0x20F0)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-704">Для корневого объекта требуется класс "Top".</span><span class="sxs-lookup"><span data-stu-id="ad39a-704">A root object requires a class of 'top'.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**\_службы DS, которые \_ отказывается от \_ \_ ролей FSMO**</span><span class="sxs-lookup"><span data-stu-id="ad39a-705"><span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR\_DS\_REFUSING\_FSMO\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-706">8433 (0x20F1)</span><span class="sxs-lookup"><span data-stu-id="ad39a-706">8433 (0x20F1)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-707">Сервер каталогов завершает работу и не может стать владельцем новых ролей операций с плавающей операцией с одним хозяином.</span><span class="sxs-lookup"><span data-stu-id="ad39a-707">This directory server is shutting down, and cannot take ownership of new floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**в \_ DS \_ отсутствуют \_ \_ Параметры FSMO**</span><span class="sxs-lookup"><span data-stu-id="ad39a-708"><span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR\_DS\_MISSING\_FSMO\_SETTINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-709">8434 (0x20F2)</span><span class="sxs-lookup"><span data-stu-id="ad39a-709">8434 (0x20F2)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-710">В службе каталогов отсутствуют обязательные сведения о конфигурации, и ей не удается определить принадлежность ролей операций с плавающей операцией с одним хозяином.</span><span class="sxs-lookup"><span data-stu-id="ad39a-710">The directory service is missing mandatory configuration information, and is unable to determine the ownership of floating single-master operation roles.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**Ошибка \_ DS \_ при \_ \_ суррендерии \_ ролей**</span><span class="sxs-lookup"><span data-stu-id="ad39a-711"><span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR\_DS\_UNABLE\_TO\_SURRENDER\_ROLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-712">8435 (0x20F3)</span><span class="sxs-lookup"><span data-stu-id="ad39a-712">8435 (0x20F3)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-713">Службе каталогов не удалось переместить владение одной или несколькими ролями операций с плавающей точкой на другие серверы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-713">The directory service was unable to transfer ownership of one or more floating single-master operation roles to other servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**Ошибка \_ \_ Generic DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-714"><span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR\_DS\_DRA\_GENERIC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-715">8436 (0x20F4)</span><span class="sxs-lookup"><span data-stu-id="ad39a-715">8436 (0x20F4)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-716">Сбой операции репликации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-716">The replication operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**Ошибка \_ \_ \_ недопустимого параметра DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-717"><span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR\_DS\_DRA\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-718">8437 (0x20F5)</span><span class="sxs-lookup"><span data-stu-id="ad39a-718">8437 (0x20F5)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-719">Для этой операции репликации указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ad39a-719">An invalid parameter was specified for this replication operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**Ошибка \_ " \_ занят DS DRA" \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-720"><span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR\_DS\_DRA\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-721">8438 (0x20F6)</span><span class="sxs-lookup"><span data-stu-id="ad39a-721">8438 (0x20F6)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-722">Служба каталогов слишком занята для завершения операции репликации в данный момент.</span><span class="sxs-lookup"><span data-stu-id="ad39a-722">The directory service is too busy to complete the replication operation at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**Ошибка \_ DS \_ DRA с \_ неправильным \_ DN**</span><span class="sxs-lookup"><span data-stu-id="ad39a-723"><span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR\_DS\_DRA\_BAD\_DN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-724">8439 (0x20F7)</span><span class="sxs-lookup"><span data-stu-id="ad39a-724">8439 (0x20F7)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-725">Указано недопустимое различающееся имя для этой операции репликации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-725">The distinguished name specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**Ошибка \_ \_ \_ неверного \_ NC DRA DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-726"><span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR\_DS\_DRA\_BAD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-727">8440 (0x20F8)</span><span class="sxs-lookup"><span data-stu-id="ad39a-727">8440 (0x20F8)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-728">Для этой операции репликации указан недопустимый контекст именования.</span><span class="sxs-lookup"><span data-stu-id="ad39a-728">The naming context specified for this replication operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**Ошибка \_ доменных служб DS \_ DRA \_ с именем \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-729"><span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR\_DS\_DRA\_DN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-730">8441 (0x20F9)</span><span class="sxs-lookup"><span data-stu-id="ad39a-730">8441 (0x20F9)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-731">Различающееся имя, указанное для этой операции репликации, уже существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-731">The distinguished name specified for this replication operation already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**Ошибка \_ \_ \_ внутренней ошибки DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-732"><span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**ERROR\_DS\_DRA\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-733">8442 (0x20FA)</span><span class="sxs-lookup"><span data-stu-id="ad39a-733">8442 (0x20FA)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-734">В системе репликации произошла внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="ad39a-734">The replication system encountered an internal error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**Ошибка \_ DS \_ DRA не \_ согласуется с \_ деревом каталогов**</span><span class="sxs-lookup"><span data-stu-id="ad39a-735"><span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR\_DS\_DRA\_INCONSISTENT\_DIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-736">8443 (0x20FB)</span><span class="sxs-lookup"><span data-stu-id="ad39a-736">8443 (0x20FB)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-737">При выполнении операции репликации возникла несогласованность базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad39a-737">The replication operation encountered a database inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**Ошибка \_ \_ \_ при подключении DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-738"><span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR\_DS\_DRA\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-739">8444 (0x20FC)</span><span class="sxs-lookup"><span data-stu-id="ad39a-739">8444 (0x20FC)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-740">Не удалось связаться с сервером, указанным для этой операции репликации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-740">The server specified for this replication operation could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**Ошибка \_ \_ \_ неправильного \_ типа экземпляра DRA DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-741"><span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR\_DS\_DRA\_BAD\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-742">8445 (0x20FD)</span><span class="sxs-lookup"><span data-stu-id="ad39a-742">8445 (0x20FD)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-743">Операция репликации обнаружила объект с недопустимым типом экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ad39a-743">The replication operation encountered an object with an invalid instance type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**Ошибка \_ \_ \_ вне \_ \_ памяти DS DRA**</span><span class="sxs-lookup"><span data-stu-id="ad39a-744"><span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR\_DS\_DRA\_OUT\_OF\_MEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-745">8446 (0x20FE)</span><span class="sxs-lookup"><span data-stu-id="ad39a-745">8446 (0x20FE)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-746">Операции репликации не удалось выделить память.</span><span class="sxs-lookup"><span data-stu-id="ad39a-746">The replication operation failed to allocate memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**Ошибка \_ \_ \_ электронной почты DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-747"><span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR\_DS\_DRA\_MAIL\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-748">8447 (0x20FF)</span><span class="sxs-lookup"><span data-stu-id="ad39a-748">8447 (0x20FF)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-749">Операция репликации обнаружила ошибку в почтовой системе.</span><span class="sxs-lookup"><span data-stu-id="ad39a-749">The replication operation encountered an error with the mail system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**Ошибка \_ " \_ ссылка DS DRA" \_ \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="ad39a-750"><span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERROR\_DS\_DRA\_REF\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-751">8448 (0x2100)</span><span class="sxs-lookup"><span data-stu-id="ad39a-751">8448 (0x2100)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-752">Сведения о ссылке репликации для целевого сервера уже существуют.</span><span class="sxs-lookup"><span data-stu-id="ad39a-752">The replication reference information for the target server already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**Ошибка \_ " \_ ссылка DS DRA \_ \_ не \_ найдена"**</span><span class="sxs-lookup"><span data-stu-id="ad39a-753"><span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR\_DS\_DRA\_REF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-754">8449 (0x2101)</span><span class="sxs-lookup"><span data-stu-id="ad39a-754">8449 (0x2101)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-755">Сведения о ссылке репликации для целевого сервера не существуют.</span><span class="sxs-lookup"><span data-stu-id="ad39a-755">The replication reference information for the target server does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**Ошибка \_ DS \_ DRA \_ obj \_ — \_ \_ источник представителя**</span><span class="sxs-lookup"><span data-stu-id="ad39a-756"><span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR\_DS\_DRA\_OBJ\_IS\_REP\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-757">8450 (0x2102)</span><span class="sxs-lookup"><span data-stu-id="ad39a-757">8450 (0x2102)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-758">Невозможно удалить контекст именования, так как он реплицируется на другой сервер.</span><span class="sxs-lookup"><span data-stu-id="ad39a-758">The naming context cannot be removed because it is replicated to another server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**Ошибка \_ \_ \_ базы данных DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-759"><span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**ERROR\_DS\_DRA\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-760">8451 (0x2103)</span><span class="sxs-lookup"><span data-stu-id="ad39a-760">8451 (0x2103)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-761">При выполнении операции репликации произошла ошибка базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad39a-761">The replication operation encountered a database error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**Ошибка \_ DS \_ DRA \_ без \_ реплики**</span><span class="sxs-lookup"><span data-stu-id="ad39a-762"><span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR\_DS\_DRA\_NO\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-763">8452 (0x2104)</span><span class="sxs-lookup"><span data-stu-id="ad39a-763">8452 (0x2104)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-764">Контекст именования находится в процессе удаления или не реплицируется с указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="ad39a-764">The naming context is in the process of being removed or is not replicated from the specified server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**Ошибка \_ \_ \_ отказа в доступе DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-765"><span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR\_DS\_DRA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-766">8453 (0x2105)</span><span class="sxs-lookup"><span data-stu-id="ad39a-766">8453 (0x2105)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-767">Отказано в доступе к репликации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-767">Replication access was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**Ошибка \_ DS \_ DRA \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="ad39a-768"><span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR\_DS\_DRA\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-769">8454 (0x2106)</span><span class="sxs-lookup"><span data-stu-id="ad39a-769">8454 (0x2106)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-770">Запрошенная операция не поддерживается этой версией службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-770">The requested operation is not supported by this version of the directory service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**Ошибка \_ при \_ \_ отмене RPC DRA DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-771"><span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR\_DS\_DRA\_RPC\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-772">8455 (0x2107)</span><span class="sxs-lookup"><span data-stu-id="ad39a-772">8455 (0x2107)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-773">Удаленный вызов процедуры репликации был отменен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-773">The replication remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**Ошибка \_ " \_ источник DRA DS \_ \_ отключен"**</span><span class="sxs-lookup"><span data-stu-id="ad39a-774"><span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERROR\_DS\_DRA\_SOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-775">8456 (0x2108)</span><span class="sxs-lookup"><span data-stu-id="ad39a-775">8456 (0x2108)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-776">Исходный сервер в настоящий момент отвергает запросы на репликацию.</span><span class="sxs-lookup"><span data-stu-id="ad39a-776">The source server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**Ошибка \_ при \_ \_ отключении приемника DRA DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-777"><span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR\_DS\_DRA\_SINK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-778">8457 (0x2109)</span><span class="sxs-lookup"><span data-stu-id="ad39a-778">8457 (0x2109)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-779">Целевой сервер в настоящий момент отвергает запросы на репликацию.</span><span class="sxs-lookup"><span data-stu-id="ad39a-779">The destination server is currently rejecting replication requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**Ошибка \_ при \_ \_ конфликте имен DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-780"><span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERROR\_DS\_DRA\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-781">8458 (0x210A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-781">8458 (0x210A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-782">Сбой операции репликации из-за конфликта имен объектов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-782">The replication operation failed due to a collision of object names.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**Ошибка \_ при \_ \_ \_ повторной установке источника DRA DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-783"><span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR\_DS\_DRA\_SOURCE\_REINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-784">8459 (0x210B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-784">8459 (0x210B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-785">Источник репликации был переустановлен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-785">The replication source has been reinstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**Ошибка \_ DS \_ DRA с \_ отсутствующим \_ родителем**</span><span class="sxs-lookup"><span data-stu-id="ad39a-786"><span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR\_DS\_DRA\_MISSING\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-787">8460 (0x210C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-787">8460 (0x210C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-788">Сбой операции репликации из-за отсутствия обязательного родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-788">The replication operation failed because a required parent object is missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**Ошибка \_ DS \_ DRA с \_ вытеснением**</span><span class="sxs-lookup"><span data-stu-id="ad39a-789"><span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR\_DS\_DRA\_PREEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-790">8461 (0x210D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-790">8461 (0x210D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-791">Операция репликации была прервана.</span><span class="sxs-lookup"><span data-stu-id="ad39a-791">The replication operation was preempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**Ошибка \_ при \_ \_ \_ синхронизации несинхронизированных DS DRA**</span><span class="sxs-lookup"><span data-stu-id="ad39a-792"><span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR\_DS\_DRA\_ABANDON\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-793">8462 (0x210E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-793">8462 (0x210E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-794">Попытка синхронизации репликации была прервана из-за отсутствия обновлений.</span><span class="sxs-lookup"><span data-stu-id="ad39a-794">The replication synchronization attempt was abandoned because of a lack of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**Ошибка \_ при \_ \_ завершении работы DS DRA**</span><span class="sxs-lookup"><span data-stu-id="ad39a-795"><span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR\_DS\_DRA\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-796">8463 (0x210F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-796">8463 (0x210F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-797">Операция репликации была прервана, так как система завершает работу.</span><span class="sxs-lookup"><span data-stu-id="ad39a-797">The replication operation was terminated because the system is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**Ошибка \_ при \_ \_ \_ частичном наборе несовместимости DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-798"><span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR\_DS\_DRA\_INCOMPATIBLE\_PARTIAL\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-799">8464 (0x2110)</span><span class="sxs-lookup"><span data-stu-id="ad39a-799">8464 (0x2110)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-800">Попытка синхронизации завершилась сбоем, так как целевой контроллер домена ожидает синхронизации новых частичных атрибутов из источника.</span><span class="sxs-lookup"><span data-stu-id="ad39a-800">Synchronization attempt failed because the destination DC is currently waiting to synchronize new partial attributes from source.</span></span> <span data-ttu-id="ad39a-801">Это состояние является нормальным, если Последнее изменение схемы изменило набор атрибутов partial.</span><span class="sxs-lookup"><span data-stu-id="ad39a-801">This condition is normal if a recent schema change modified the partial attribute set.</span></span> <span data-ttu-id="ad39a-802">Целевой частичный набор атрибутов не является подмножеством частичного набора атрибутов источника.</span><span class="sxs-lookup"><span data-stu-id="ad39a-802">The destination partial attribute set is not a subset of source partial attribute set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**Ошибка \_ \_ \_ : источник DRA DS \_ является \_ частичной \_ репликой**</span><span class="sxs-lookup"><span data-stu-id="ad39a-803"><span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERROR\_DS\_DRA\_SOURCE\_IS\_PARTIAL\_REPLICA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-804">8465 (0x2111)</span><span class="sxs-lookup"><span data-stu-id="ad39a-804">8465 (0x2111)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-805">Попытка синхронизации репликации завершилась сбоем, так как Главная реплика попыталась выполнить синхронизацию из частичной реплики.</span><span class="sxs-lookup"><span data-stu-id="ad39a-805">The replication synchronization attempt failed because a master replica attempted to sync from a partial replica.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**Ошибка \_ \_ \_ \_ при подключении екстн DS \_ DRA**</span><span class="sxs-lookup"><span data-stu-id="ad39a-806"><span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR\_DS\_DRA\_EXTN\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-807">8466 (0x2112)</span><span class="sxs-lookup"><span data-stu-id="ad39a-807">8466 (0x2112)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-808">Для сервера, указанного для этой операции репликации, установлен контакт, но серверу не удалось связаться с дополнительным сервером, необходимым для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="ad39a-808">The server specified for this replication operation was contacted, but that server was unable to contact an additional server needed to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**Ошибка \_ при \_ установке \_ несоответствия схемы службы DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-809"><span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR\_DS\_INSTALL\_SCHEMA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-810">8467 (0x2113)</span><span class="sxs-lookup"><span data-stu-id="ad39a-810">8467 (0x2113)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-811">Версия схемы службы каталогов исходного леса несовместима с версией службы каталогов на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ad39a-811">The version of the directory service schema of the source forest is not compatible with the version of directory service on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**Ошибка \_ DS \_ DUP \_ Link \_ ID**</span><span class="sxs-lookup"><span data-stu-id="ad39a-812"><span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERROR\_DS\_DUP\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-813">8468 (0x2114)</span><span class="sxs-lookup"><span data-stu-id="ad39a-813">8468 (0x2114)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-814">Сбой обновления схемы: атрибут с таким идентификатором связи уже существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-814">Schema update failed: An attribute with the same link identifier already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**Ошибка \_ при \_ \_ \_ разрешении имени DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-815"><span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR\_DS\_NAME\_ERROR\_RESOLVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-816">8469 (0x2115)</span><span class="sxs-lookup"><span data-stu-id="ad39a-816">8469 (0x2115)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-817">Преобразование имен: Общая ошибка обработки.</span><span class="sxs-lookup"><span data-stu-id="ad39a-817">Name translation: Generic processing error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**Ошибка \_ \_ имени DS \_ \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-818"><span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-819">8470 (0x2116)</span><span class="sxs-lookup"><span data-stu-id="ad39a-819">8470 (0x2116)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-820">Преобразование имени: не удалось найти имя или недостаточно прав для просмотра имени.</span><span class="sxs-lookup"><span data-stu-id="ad39a-820">Name translation: Could not find the name or insufficient right to see name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**Ошибка \_ \_ имени DS \_ не \_ является \_ уникальной**</span><span class="sxs-lookup"><span data-stu-id="ad39a-821"><span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR\_DS\_NAME\_ERROR\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-822">8471 (0x2117)</span><span class="sxs-lookup"><span data-stu-id="ad39a-822">8471 (0x2117)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-823">Преобразование имени: входное имя, сопоставленное более чем с одним выходным именем.</span><span class="sxs-lookup"><span data-stu-id="ad39a-823">Name translation: Input name mapped to more than one output name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**Ошибка \_ имени DS, \_ \_ Ошибка \_ без \_ сопоставления**</span><span class="sxs-lookup"><span data-stu-id="ad39a-824"><span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-825">8472 (0x2118)</span><span class="sxs-lookup"><span data-stu-id="ad39a-825">8472 (0x2118)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-826">Преобразование имени: обнаружено входное имя, но не соответствующий выходной формат.</span><span class="sxs-lookup"><span data-stu-id="ad39a-826">Name translation: Input name found, but not the associated output format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**Ошибка \_ DS \_ имя \_ \_ только домен \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-827"><span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERROR\_DS\_NAME\_ERROR\_DOMAIN\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-828">8473 (0x2119)</span><span class="sxs-lookup"><span data-stu-id="ad39a-828">8473 (0x2119)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-829">Преобразование имен: не удается полностью разрешить, найден только домен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-829">Name translation: Unable to resolve completely, only the domain was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**Ошибка \_ имени DS, \_ \_ Ошибка \_ без \_ синтаксического \_ сопоставления**</span><span class="sxs-lookup"><span data-stu-id="ad39a-830"><span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR\_DS\_NAME\_ERROR\_NO\_SYNTACTICAL\_MAPPING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-831">8474 (0x211A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-831">8474 (0x211A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-832">Преобразование имен: не удается выполнить чистое синтаксическое сопоставление на клиенте без перехода к сети.</span><span class="sxs-lookup"><span data-stu-id="ad39a-832">Name translation: Unable to perform purely syntactical mapping at the client without going out to the wire.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**произошла ошибка \_ DS, \_ созданная \_ Атри \_ Mod**</span><span class="sxs-lookup"><span data-stu-id="ad39a-833"><span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR\_DS\_CONSTRUCTED\_ATT\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-834">8475 (0x211B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-834">8475 (0x211B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-835">Изменение сконструированного атрибута не допускается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-835">Modification of a constructed attribute is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**Ошибка \_ DS \_ - \_ неправильный \_ класс obj-объект \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-836"><span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR\_DS\_WRONG\_OM\_OBJ\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-837">8476 (0x211C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-837">8476 (0x211C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-838">Указанный объект OM-Object-Class неверен для атрибута с указанным синтаксисом.</span><span class="sxs-lookup"><span data-stu-id="ad39a-838">The OM-Object-Class specified is incorrect for an attribute with the specified syntax.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**произошла ошибка \_ \_ \_ \_ в ожидании DS DRA REPL**</span><span class="sxs-lookup"><span data-stu-id="ad39a-839"><span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR\_DS\_DRA\_REPL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-840">8477 (0x211D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-840">8477 (0x211D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-841">Запрос на репликацию отправлен; Ожидание ответа.</span><span class="sxs-lookup"><span data-stu-id="ad39a-841">The replication request has been posted; waiting for reply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**произошла ошибка доменных служб \_ DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-842"><span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR\_DS\_DS\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-843">8478 (0x211E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-843">8478 (0x211E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-844">Для запрошенной операции требуется служба каталогов, но она недоступна.</span><span class="sxs-lookup"><span data-stu-id="ad39a-844">The requested operation requires a directory service, and none was available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**Ошибка \_ DS \_ недопустимое \_ \_ отображаемое \_ имя LDAP**</span><span class="sxs-lookup"><span data-stu-id="ad39a-845"><span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR\_DS\_INVALID\_LDAP\_DISPLAY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-846">8479 (0x211F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-846">8479 (0x211F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-847">Отображаемое имя LDAP класса или атрибута содержит символы, отличные от ASCII.</span><span class="sxs-lookup"><span data-stu-id="ad39a-847">The LDAP display name of the class or attribute contains non-ASCII characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**Ошибка \_ поиска в DS \_ без \_ базовой службы \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-848"><span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR\_DS\_NON\_BASE\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-849">8480 (0x2120)</span><span class="sxs-lookup"><span data-stu-id="ad39a-849">8480 (0x2120)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-850">Запрошенная операция поиска поддерживается только для базовых поисков.</span><span class="sxs-lookup"><span data-stu-id="ad39a-850">The requested search operation is only supported for base searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**Ошибка \_ DS не \_ удается \_ получить \_ АТТС**</span><span class="sxs-lookup"><span data-stu-id="ad39a-851"><span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR\_DS\_CANT\_RETRIEVE\_ATTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-852">8481 (0x2121)</span><span class="sxs-lookup"><span data-stu-id="ad39a-852">8481 (0x2121)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-853">Поиск не смог получить атрибуты из базы данных.</span><span class="sxs-lookup"><span data-stu-id="ad39a-853">The search failed to retrieve attributes from the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**Ошибка \_ DS \_ посмотрите \_ без \_ компоновки**</span><span class="sxs-lookup"><span data-stu-id="ad39a-854"><span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR\_DS\_BACKLINK\_WITHOUT\_LINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-855">8482 (0x2122)</span><span class="sxs-lookup"><span data-stu-id="ad39a-855">8482 (0x2122)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-856">Операция обновления схемы попыталась добавить атрибут обратной ссылки, который не имеет соответствующей ссылки вперед.</span><span class="sxs-lookup"><span data-stu-id="ad39a-856">The schema update operation tried to add a backward link attribute that has no corresponding forward link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**Ошибка \_ при \_ несоответствии эпохи DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-857"><span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR\_DS\_EPOCH\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-858">8483 (0x2123)</span><span class="sxs-lookup"><span data-stu-id="ad39a-858">8483 (0x2123)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-859">Источник и назначение междоменного перемещения не согласуются с номером эпохи объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-859">Source and destination of a cross-domain move do not agree on the object's epoch number.</span></span> <span data-ttu-id="ad39a-860">Источник или назначение не имеют последней версии объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-860">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии имени src в DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-861"><span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR\_DS\_SRC\_NAME\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-862">8484 (0x2124)</span><span class="sxs-lookup"><span data-stu-id="ad39a-862">8484 (0x2124)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-863">Источник и назначение междоменного перемещения не согласуются с текущим именем объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-863">Source and destination of a cross-domain move do not agree on the object's current name.</span></span> <span data-ttu-id="ad39a-864">Источник или назначение не имеют последней версии объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-864">Either source or destination does not have the latest version of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**Ошибка \_ при \_ \_ идентичности DS src и \_ DST \_ NC \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-865"><span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR\_DS\_SRC\_AND\_DST\_NC\_IDENTICAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-866">8485 (0x2125)</span><span class="sxs-lookup"><span data-stu-id="ad39a-866">8485 (0x2125)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-867">Источник и назначение для операции междоменного перемещения идентичны.</span><span class="sxs-lookup"><span data-stu-id="ad39a-867">Source and destination for the cross-domain move operation are identical.</span></span> <span data-ttu-id="ad39a-868">Вызывающий объект должен использовать операцию локального перемещения вместо операции перемещения между доменами.</span><span class="sxs-lookup"><span data-stu-id="ad39a-868">Caller should use local move operation instead of cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**Ошибка \_ при \_ \_ \_ несоответствии NC в DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-869"><span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR\_DS\_DST\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-870">8486 (0x2126)</span><span class="sxs-lookup"><span data-stu-id="ad39a-870">8486 (0x2126)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-871">Источник и назначение для междоменного перемещения не согласованы с контекстами именования в лесу.</span><span class="sxs-lookup"><span data-stu-id="ad39a-871">Source and destination for a cross-domain move are not in agreement on the naming contexts in the forest.</span></span> <span data-ttu-id="ad39a-872">Источник или назначение не имеют последней версии контейнера секций.</span><span class="sxs-lookup"><span data-stu-id="ad39a-872">Either source or destination does not have the latest version of the Partitions container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**Ошибка \_ DS \_ , \_ не \_ аусоритиве \_ для \_ NC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-873"><span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR\_DS\_NOT\_AUTHORITIVE\_FOR\_DST\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-874">8487 (0x2127)</span><span class="sxs-lookup"><span data-stu-id="ad39a-874">8487 (0x2127)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-875">Назначение для перемещения между доменами не является полномочным для контекста именования назначения.</span><span class="sxs-lookup"><span data-stu-id="ad39a-875">Destination of a cross-domain move is not authoritative for the destination naming context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**\_несоответствие \_ \_ идентификатора GUID \_ src в DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-876"><span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR\_DS\_SRC\_GUID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-877">8488 (0x2128)</span><span class="sxs-lookup"><span data-stu-id="ad39a-877">8488 (0x2128)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-878">Источник и назначение междоменного перемещения не согласуются с удостоверением исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-878">Source and destination of a cross-domain move do not agree on the identity of the source object.</span></span> <span data-ttu-id="ad39a-879">Источник или назначение не имеют последней версии исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-879">Either source or destination does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**Ошибка \_ DS не \_ удается \_ Переместить \_ Удаленный \_ объект**</span><span class="sxs-lookup"><span data-stu-id="ad39a-880"><span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR\_DS\_CANT\_MOVE\_DELETED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-881">8489 (0x2129)</span><span class="sxs-lookup"><span data-stu-id="ad39a-881">8489 (0x2129)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-882">Объект, перемещаемый между доменами, уже удален целевым сервером.</span><span class="sxs-lookup"><span data-stu-id="ad39a-882">Object being moved across-domains is already known to be deleted by the destination server.</span></span> <span data-ttu-id="ad39a-883">На исходном сервере не установлена последняя версия исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-883">The source server does not have the latest version of the source object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**произошла ошибка \_ \_ при выполнении операции PDC DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-884"><span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR\_DS\_PDC\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-885">8490 (0x212A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-885">8490 (0x212A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-886">Уже выполняется другая операция, которая требует монопольного доступа к FSMO PDC.</span><span class="sxs-lookup"><span data-stu-id="ad39a-886">Another operation which requires exclusive access to the PDC FSMO is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**Ошибка \_ при \_ \_ очистке междоменной службы DS \_ \_ рекд**</span><span class="sxs-lookup"><span data-stu-id="ad39a-887"><span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR\_DS\_CROSS\_DOMAIN\_CLEANUP\_REQD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-888">8491 (0x212B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-888">8491 (0x212B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-889">Операция междоменного перемещения завершилась сбоем, так как существует две версии перемещенного объекта — по одному в исходном и конечном доменах.</span><span class="sxs-lookup"><span data-stu-id="ad39a-889">A cross-domain move operation failed such that two versions of the moved object exist - one each in the source and destination domains.</span></span> <span data-ttu-id="ad39a-890">Целевой объект необходимо удалить для восстановления системы в целостное состояние.</span><span class="sxs-lookup"><span data-stu-id="ad39a-890">The destination object needs to be removed to restore the system to a consistent state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**Ошибка \_ DS \_ недопустимой \_ \_ операции перемещения ксдом \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-891"><span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR\_DS\_ILLEGAL\_XDOM\_MOVE\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-892">8492 (0x212C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-892">8492 (0x212C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-893">Этот объект не может быть перемещен между границами домена, так как перемещение между доменами для этого класса запрещено, или у объекта есть некоторые особые характеристики, например: учетная запись доверия или ограниченный RID, предотвращающий его перемещение.</span><span class="sxs-lookup"><span data-stu-id="ad39a-893">This object may not be moved across domain boundaries either because cross-domain moves for this class are disallowed, or the object has some special characteristics, e.g.: trust account or restricted RID, which prevent its move.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**Ошибка \_ DS \_ не \_ удается \_ с \_ мембершпс группы acct \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-894"><span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR\_DS\_CANT\_WITH\_ACCT\_GROUP\_MEMBERSHPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-895">8493 (0x212D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-895">8493 (0x212D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-896">Невозможно переместить объекты с членством в границах домена, так как после перемещения это приведет к нарушению условий членства в группе учетных записей.</span><span class="sxs-lookup"><span data-stu-id="ad39a-896">Can't move objects with memberships across domain boundaries as once moved, this would violate the membership conditions of the account group.</span></span> <span data-ttu-id="ad39a-897">Удалите объект из любого членства в группах учетных записей и повторите попытку.</span><span class="sxs-lookup"><span data-stu-id="ad39a-897">Remove the object from any account group memberships and retry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**Ошибка \_ NC DS Active Directory \_ \_ должна \_ иметь \_ \_ родителя NC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-898"><span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERROR\_DS\_NC\_MUST\_HAVE\_NC\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-899">8494 (0x212E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-899">8494 (0x212E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-900">Заголовок контекста именования должен быть прямым дочерним элементом другого заголовка контекста именования, а не внутреннего узла.</span><span class="sxs-lookup"><span data-stu-id="ad39a-900">A naming context head must be the immediate child of another naming context head, not of an interior node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**Ошибка \_ \_ \_ \_ \_ проверки подлинности CR в DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-901"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-902">8495 (0x212F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-902">8495 (0x212F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-903">Каталог не может проверить предложенное имя контекста именования, так как он не содержит реплики контекста именования выше предложенного контекста именования.</span><span class="sxs-lookup"><span data-stu-id="ad39a-903">The directory cannot validate the proposed naming context name because it does not hold a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="ad39a-904">Убедитесь, что роль хозяина именования доменов удерживается сервером, настроенным в качестве сервера глобального каталога, и что сервер обновлен с партнерами по репликации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-904">Please ensure that the domain naming master role is held by a server that is configured as a global catalog server, and that the server is up to date with its replication partners.</span></span> <span data-ttu-id="ad39a-905">(Относится только к хозяинам именования доменов Windows 2000.)</span><span class="sxs-lookup"><span data-stu-id="ad39a-905">(Applies only to Windows 2000 Domain Naming masters.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**\_домен ошибок DS \_ DST не является \_ \_ \_ собственным**</span><span class="sxs-lookup"><span data-stu-id="ad39a-906"><span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR\_DS\_DST\_DOMAIN\_NOT\_NATIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-907">8496 (0x2130)</span><span class="sxs-lookup"><span data-stu-id="ad39a-907">8496 (0x2130)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-908">Конечный домен должен находиться в собственном режиме.</span><span class="sxs-lookup"><span data-stu-id="ad39a-908">Destination domain must be in native mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**Ошибка в \_ DS с \_ отсутствующим \_ \_ контейнером инфраструктуры**</span><span class="sxs-lookup"><span data-stu-id="ad39a-909"><span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR\_DS\_MISSING\_INFRASTRUCTURE\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-910">8497 (0x2131)</span><span class="sxs-lookup"><span data-stu-id="ad39a-910">8497 (0x2131)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-911">Невозможно выполнить операцию, так как сервер не имеет контейнера инфраструктуры в предметной области.</span><span class="sxs-lookup"><span data-stu-id="ad39a-911">The operation cannot be performed because the server does not have an infrastructure container in the domain of interest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**Ошибка \_ DS не \_ удается \_ Переместить \_ группу учетных записей \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-912"><span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR\_DS\_CANT\_MOVE\_ACCOUNT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-913">8498 (0x2132)</span><span class="sxs-lookup"><span data-stu-id="ad39a-913">8498 (0x2132)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-914">Перемещение между доменами непустых групп учетных записей не допускается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-914">Cross-domain move of non-empty account groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**Ошибка \_ DS \_ не \_ удается \_ Переместить \_ группу ресурсов**</span><span class="sxs-lookup"><span data-stu-id="ad39a-915"><span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR\_DS\_CANT\_MOVE\_RESOURCE\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-916">8499 (0x2133)</span><span class="sxs-lookup"><span data-stu-id="ad39a-916">8499 (0x2133)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-917">Перемещение между доменами непустых групп ресурсов не допускается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-917">Cross-domain move of non-empty resource groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**Ошибка \_ DS \_ Недопустимый \_ \_ флаг поиска**</span><span class="sxs-lookup"><span data-stu-id="ad39a-918"><span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-919">8500 (0x2134)</span><span class="sxs-lookup"><span data-stu-id="ad39a-919">8500 (0x2134)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-920">Недопустимые флаги поиска для атрибута.</span><span class="sxs-lookup"><span data-stu-id="ad39a-920">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="ad39a-921">Бит ANR допустим только для атрибутов строк Юникода или Teletex.</span><span class="sxs-lookup"><span data-stu-id="ad39a-921">The ANR bit is valid only on attributes of Unicode or Teletex strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**Ошибка \_ DS \_ без \_ дерева \_ Удаление \_ выше \_ сетевого контроллера**</span><span class="sxs-lookup"><span data-stu-id="ad39a-922"><span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR\_DS\_NO\_TREE\_DELETE\_ABOVE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-923">8501 (0x2135)</span><span class="sxs-lookup"><span data-stu-id="ad39a-923">8501 (0x2135)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-924">Удаление дерева, начиная с объекта, имеющего заголовок NC в качестве потомка, запрещено.</span><span class="sxs-lookup"><span data-stu-id="ad39a-924">Tree deletions starting at an object which has an NC head as a descendant are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**Ошибка \_ DS \_ не удалось \_ блокировать \_ дерево блокировки \_ для \_ удаления**</span><span class="sxs-lookup"><span data-stu-id="ad39a-925"><span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR\_DS\_COULDNT\_LOCK\_TREE\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-926">8502 (0x2136)</span><span class="sxs-lookup"><span data-stu-id="ad39a-926">8502 (0x2136)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-927">Службе каталогов не удалось заблокировать дерево при подготовке к удалению дерева, так как это дерево используется.</span><span class="sxs-lookup"><span data-stu-id="ad39a-927">The directory service failed to lock a tree in preparation for a tree deletion because the tree was in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**Ошибка \_ DS \_ не удалось \_ определяет \_ объекты \_ для \_ \_ удаления дерева**</span><span class="sxs-lookup"><span data-stu-id="ad39a-928"><span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR\_DS\_COULDNT\_IDENTIFY\_OBJECTS\_FOR\_TREE\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-929">8503 (0x2137)</span><span class="sxs-lookup"><span data-stu-id="ad39a-929">8503 (0x2137)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-930">Службе каталогов не удалось опознать список объектов для удаления при попытке удаления дерева.</span><span class="sxs-lookup"><span data-stu-id="ad39a-930">The directory service failed to identify the list of objects to delete while attempting a tree deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**Ошибка \_ \_ \_ при инициализации SAM \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-931"><span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-932">8504 (0x2138)</span><span class="sxs-lookup"><span data-stu-id="ad39a-932">8504 (0x2138)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-933">Не удалось инициализировать диспетчер учетных записей безопасности из-за следующей ошибки: %1.</span><span class="sxs-lookup"><span data-stu-id="ad39a-933">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="ad39a-934">Состояние ошибки: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="ad39a-934">Error Status: 0x%2.</span></span> <span data-ttu-id="ad39a-935">Завершите работу системы и перезагрузите ее в режим восстановления служб каталогов. подробные сведения см. в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="ad39a-935">Please shutdown this system and reboot into Directory Services Restore Mode, check the event log for more detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**Ошибка \_ при \_ \_ нарушении чувствительности группы DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-936"><span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR\_DS\_SENSITIVE\_GROUP\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-937">8505 (0x2139)</span><span class="sxs-lookup"><span data-stu-id="ad39a-937">8505 (0x2139)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-938">Только администратор может изменить список членов административной группы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-938">Only an administrator can modify the membership list of an administrative group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**Ошибка \_ DS \_ не \_ удается \_ примариграупид mod**</span><span class="sxs-lookup"><span data-stu-id="ad39a-939"><span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR\_DS\_CANT\_MOD\_PRIMARYGROUPID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-940">8506 (0x213A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-940">8506 (0x213A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-941">Невозможно изменить идентификатор основной группы учетной записи контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-941">Cannot change the primary group ID of a domain controller account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**Ошибка \_ DS \_ недопустимой \_ базовой \_ схемы \_ Mod**</span><span class="sxs-lookup"><span data-stu-id="ad39a-942"><span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR\_DS\_ILLEGAL\_BASE\_SCHEMA\_MOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-943">8507 (0x213B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-943">8507 (0x213B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-944">Предпринята попытка изменить базовую схему.</span><span class="sxs-lookup"><span data-stu-id="ad39a-944">An attempt is made to modify the base schema.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**Ошибка \_ \_ ненадежного \_ изменения схемы DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-945"><span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR\_DS\_NONSAFE\_SCHEMA\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-946">8508 (0x213C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-946">8508 (0x213C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-947">Добавление нового обязательного атрибута к существующему классу, удаление обязательного атрибута из существующего класса или Добавление дополнительного атрибута к Специальному классу Top, который не является атрибутом посмотрите (например, добавление или удаление вспомогательного класса), не допускается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-947">Adding a new mandatory attribute to an existing class, deleting a mandatory attribute from an existing class, or adding an optional attribute to the special class Top that is not a backlink attribute (directly or through inheritance, for example, by adding or deleting an auxiliary class) is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**Ошибка \_ \_ \_ запрещенного обновления схемы DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-948"><span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR\_DS\_SCHEMA\_UPDATE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-949">8509 (0x213D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-949">8509 (0x213D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-950">Обновление схемы не разрешено на этом контроллере домена, так как контроллер домена не является владельцем роли FSMO схемы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-950">Schema update is not allowed on this DC because the DC is not the schema FSMO Role Owner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**Ошибка "не \_ \_ удается создать службу DS \_ \_ в \_ схеме"**</span><span class="sxs-lookup"><span data-stu-id="ad39a-951"><span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR\_DS\_CANT\_CREATE\_UNDER\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-952">8510 (0x213E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-952">8510 (0x213E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-953">Объект этого класса не может быть создан в контейнере схемы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-953">An object of this class cannot be created under the schema container.</span></span> <span data-ttu-id="ad39a-954">В контейнере схемы можно создавать только объекты Attribute-Schema и class-schema.</span><span class="sxs-lookup"><span data-stu-id="ad39a-954">You can only create attribute-schema and class-schema objects under the schema container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**Ошибка \_ DS \_ Install \_ . \_ \_ версия исходного SCH \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-955"><span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR\_DS\_INSTALL\_NO\_SRC\_SCH\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-956">8511 (0x213F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-956">8511 (0x213F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-957">Установка реплики или дочернего элемента не смогла получить атрибут Обжектверсион в контейнере схемы на исходном контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-957">The replica/child install failed to get the objectVersion attribute on the schema container on the source DC.</span></span> <span data-ttu-id="ad39a-958">Либо атрибут отсутствует в контейнере схемы, либо предоставленные учетные данные не имеют разрешения на его чтение.</span><span class="sxs-lookup"><span data-stu-id="ad39a-958">Either the attribute is missing on the schema container or the credentials supplied do not have permission to read it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**Ошибка \_ DS \_ Install \_ не \_ установлена \_ версия SCH \_ в \_ инифиле**</span><span class="sxs-lookup"><span data-stu-id="ad39a-959"><span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR\_DS\_INSTALL\_NO\_SCH\_VERSION\_IN\_INIFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-960">8512 (0x2140)</span><span class="sxs-lookup"><span data-stu-id="ad39a-960">8512 (0x2140)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-961">При установке реплики или дочерней части не удалось прочитать атрибут Обжектверсион в разделе схемы файла schema.ini в каталоге System32.</span><span class="sxs-lookup"><span data-stu-id="ad39a-961">The replica/child install failed to read the objectVersion attribute in the SCHEMA section of the file schema.ini in the system32 directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**Ошибка \_ DS — \_ Недопустимый \_ \_ Тип группы**</span><span class="sxs-lookup"><span data-stu-id="ad39a-962"><span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR\_DS\_INVALID\_GROUP\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-963">8513 (0x2141)</span><span class="sxs-lookup"><span data-stu-id="ad39a-963">8513 (0x2141)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-964">Указан недопустимый тип группы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-964">The specified group type is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**Ошибка \_ DS \_ без \_ вложенных \_ глобалграуп \_ в \_ микседдомаин**</span><span class="sxs-lookup"><span data-stu-id="ad39a-965"><span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_GLOBALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-966">8514 (0x2142)</span><span class="sxs-lookup"><span data-stu-id="ad39a-966">8514 (0x2142)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-967">Нельзя вложить глобальные группы в смешанный домен, если включена безопасность группы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-967">You cannot nest global groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**Ошибка \_ DS \_ без \_ вложения \_ локальной группы \_ в \_ микседдомаин**</span><span class="sxs-lookup"><span data-stu-id="ad39a-968"><span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR\_DS\_NO\_NEST\_LOCALGROUP\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-969">8515 (0x2143)</span><span class="sxs-lookup"><span data-stu-id="ad39a-969">8515 (0x2143)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-970">Невозможно вложить локальные группы в смешанный домен, если включена безопасность группы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-970">You cannot nest local groups in a mixed domain if the group is security-enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**\_глобальный домен \_ ошибок \_ \_ не могу иметь \_ локального \_ участника**</span><span class="sxs-lookup"><span data-stu-id="ad39a-971"><span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-972">8516 (0x2144)</span><span class="sxs-lookup"><span data-stu-id="ad39a-972">8516 (0x2144)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-973">Глобальная группа не может иметь локальную группу в качестве члена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-973">A global group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**в \_ глобальном DS "ошибка" \_ \_ \_ не удается использовать \_ универсальный \_ член**</span><span class="sxs-lookup"><span data-stu-id="ad39a-974"><span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-975">8517 (0x2145)</span><span class="sxs-lookup"><span data-stu-id="ad39a-975">8517 (0x2145)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-976">Глобальная группа не может иметь универсальную группу в качестве члена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-976">A global group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**Ошибка \_ \_ универсальной службы DS \_ \_ не удается иметь \_ локального \_ участника**</span><span class="sxs-lookup"><span data-stu-id="ad39a-977"><span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR\_DS\_UNIVERSAL\_CANT\_HAVE\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-978">8518 (0x2146)</span><span class="sxs-lookup"><span data-stu-id="ad39a-978">8518 (0x2146)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-979">Универсальная группа не может иметь локальную группу в качестве члена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-979">A universal group cannot have a local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**в \_ Глобальной службе ошибок DS \_ \_ \_ нет \_ \_ члена CROSSDOMAIN**</span><span class="sxs-lookup"><span data-stu-id="ad39a-980"><span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR\_DS\_GLOBAL\_CANT\_HAVE\_CROSSDOMAIN\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-981">8519 (0x2147)</span><span class="sxs-lookup"><span data-stu-id="ad39a-981">8519 (0x2147)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-982">Глобальная группа не может иметь междоменного члена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-982">A global group cannot have a cross-domain member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**" \_ Ошибка \_ локальной службы DS \_ \_ не удается иметь \_ \_ локальный \_ член CROSSDOMAIN"**</span><span class="sxs-lookup"><span data-stu-id="ad39a-983"><span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR\_DS\_LOCAL\_CANT\_HAVE\_CROSSDOMAIN\_LOCAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-984">8520 (0x2148)</span><span class="sxs-lookup"><span data-stu-id="ad39a-984">8520 (0x2148)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-985">Локальная группа в локальной группе не может быть членом другой локальной группы домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-985">A local group cannot have another cross domain local group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**Служба "ошибки \_ DS" \_ имеет \_ основные \_ Участники**</span><span class="sxs-lookup"><span data-stu-id="ad39a-986"><span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERROR\_DS\_HAVE\_PRIMARY\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-987">8521 (0x2149)</span><span class="sxs-lookup"><span data-stu-id="ad39a-987">8521 (0x2149)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-988">Группу с основными участниками нельзя изменить на группу с отключенной безопасностью.</span><span class="sxs-lookup"><span data-stu-id="ad39a-988">A group with primary members cannot change to a security-disabled group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**Ошибка \_ \_ \_ \_ при преобразовании SD строки DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-989"><span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR\_DS\_STRING\_SD\_CONVERSION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-990">8522 (0x214A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-990">8522 (0x214A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-991">При загрузке кэша схемы не удалось преобразовать строку SD по умолчанию для объекта class-schema.</span><span class="sxs-lookup"><span data-stu-id="ad39a-991">The schema cache load failed to convert the string default SD on a class-schema object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**Ошибка \_ при \_ именовании \_ хозяина имен DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-992"><span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR\_DS\_NAMING\_MASTER\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-993">8523 (0x214B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-993">8523 (0x214B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-994">Только DSA, настроенные на серверы глобального каталога, должны иметь роль хозяина именования доменов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-994">Only DSAs configured to be Global Catalog servers should be allowed to hold the Domain Naming Master FSMO role.</span></span> <span data-ttu-id="ad39a-995">(Применяется только к серверам Windows 2000.)</span><span class="sxs-lookup"><span data-stu-id="ad39a-995">(Applies only to Windows 2000 servers.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**Ошибка \_ \_ \_ уточняющего запроса DNS DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-996"><span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR\_DS\_DNS\_LOOKUP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-997">8524 (0x214C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-997">8524 (0x214C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-998">Операция DSA не может быть продолжена из-за ошибки уточняющего запроса DNS.</span><span class="sxs-lookup"><span data-stu-id="ad39a-998">The DSA operation is unable to proceed because of a DNS lookup failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**Ошибка \_ DS \_ не удалось \_ Update \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="ad39a-999"><span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERROR\_DS\_COULDNT\_UPDATE\_SPNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1000">8525 (0x214D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1000">8525 (0x214D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1001">При обработке изменения имени узла DNS для объекта значения имени субъекта-службы не могут быть синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1001">While processing a change to the DNS Host Name for an object, the Service Principal Name values could not be kept in sync.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**Ошибка \_ DS не \_ удается \_ получить \_ SD**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1002"><span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR\_DS\_CANT\_RETRIEVE\_SD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1003">8526 (0x214E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1003">8526 (0x214E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1004">Не удалось прочитать атрибут дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1004">The Security Descriptor attribute could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ОШИБОЧный \_ \_ ключ DS \_ не является \_ уникальным**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1005"><span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR\_DS\_KEY\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1006">8527 (0x214F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1006">8527 (0x214F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1007">Запрошенный объект не найден, но найден объект с этим ключом.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1007">The object requested was not found, but an object with that key was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**Ошибка \_ DS \_ . \_ неправильный \_ синтаксис связанного Атри \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1008"><span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR\_DS\_WRONG\_LINKED\_ATT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1009">8528 (0x2150)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1009">8528 (0x2150)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1010">Неправильный синтаксис добавляемого связанного атрибута.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1010">The syntax of the linked attribute being added is incorrect.</span></span> <span data-ttu-id="ad39a-1011">Прямые ссылки могут иметь только синтаксис 2.5.5.1, 2.5.5.7 и 2.5.5.14, а одноадресные ссылки могут иметь только синтаксис 2.5.5.1.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1011">Forward links can only have syntax 2.5.5.1, 2.5.5.7, and 2.5.5.14, and backlinks can only have syntax 2.5.5.1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**Ошибка \_ DS \_ SAM \_ : \_ требуется \_ пароль буткэй**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1012"><span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1013">8529 (0x2151)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1013">8529 (0x2151)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1014">Диспетчеру учетных записей безопасности необходимо получить пароль для загрузки.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1014">Security Account Manager needs to get the boot password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**Ошибка \_ DS \_ SAM: \_ требуется \_ буткэй флоппи- \_ дисковод**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1015"><span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR\_DS\_SAM\_NEED\_BOOTKEY\_FLOPPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1016">8530 (0x2152)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1016">8530 (0x2152)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1017">Диспетчеру учетных записей безопасности необходимо получить загрузочный ключ с дискеты.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1017">Security Account Manager needs to get the boot key from floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**Ошибка \_ \_ запуска DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1018"><span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR\_DS\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1019">8531 (0x2153)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1019">8531 (0x2153)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1020">Не удается запустить службу каталогов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1020">Directory Service cannot start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**Ошибка \_ \_ при инициализации \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1021"><span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR\_DS\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1022">8532 (0x2154)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1022">8532 (0x2154)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1023">Не удалось запустить службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1023">Directory Services could not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**Ошибка \_ DS \_ без общедоступной \_ \_ политики конфиденциальности \_ при \_ подключении**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1024"><span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR\_DS\_NO\_PKT\_PRIVACY\_ON\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1025">8533 (0x2155)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1025">8533 (0x2155)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1026">Соединение между клиентом и сервером требует конфиденциальности пакетов или более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1026">The connection between client and server requires packet privacy or better.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**Ошибка \_ \_ исходного \_ домена DS \_ в \_ лесу**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1027"><span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERROR\_DS\_SOURCE\_DOMAIN\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1028">8534 (0x2156)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1028">8534 (0x2156)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1029">Исходный домен может не находиться в том же лесу, что и назначение.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1029">The source domain may not be in the same forest as destination.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**Ошибка \_ \_ конечного домена DS, \_ \_ не \_ в \_ лесу**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1030"><span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR\_DS\_DESTINATION\_DOMAIN\_NOT\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1031">8535 (0x2157)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1031">8535 (0x2157)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1032">Конечный домен должен находиться в лесу.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1032">The destination domain must be in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**\_Аудит ошибок \_ назначения \_ DS \_ не \_ включен**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1033"><span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR\_DS\_DESTINATION\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1034">8536 (0x2158)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1034">8536 (0x2158)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1035">Для операции требуется включить аудит конечного домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1035">The operation requires that destination domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**Ошибка \_ DS не \_ удается \_ найти контроллер домена \_ \_ для \_ src \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1036"><span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR\_DS\_CANT\_FIND\_DC\_FOR\_SRC\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1037">8537 (0x2159)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1037">8537 (0x2159)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1038">Операции не удалось нахождение контроллера домена для исходного домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1038">The operation couldn't locate a DC for the source domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**Ошибка \_ DS \_ src \_ \_ , не \_ Группа \_ или \_ пользователь**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1039"><span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR\_DS\_SRC\_OBJ\_NOT\_GROUP\_OR\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1040">8538 (0x215A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1040">8538 (0x215A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1041">Исходный объект должен быть группой или пользователем.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1041">The source object must be a group or user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**\_ \_ \_ \_ \_ в \_ лесу существует ошибка ИД безопасности src DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1042"><span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR\_DS\_SRC\_SID\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1043">8539 (0x215B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1043">8539 (0x215B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1044">Идентификатор безопасности исходного объекта уже существует в целевом лесу.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1044">The source object's SID already exists in destination forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**Ошибка \_ при \_ \_ \_ \_ \_ \_ несовпадении класса объектов src и DST в DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1045"><span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR\_DS\_SRC\_AND\_DST\_OBJECT\_CLASS\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1046">8540 (0x215C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1046">8540 (0x215C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1047">Исходный и целевой объекты должны иметь один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1047">The source and destination object must be of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**Ошибка \_ \_ при инициализации ошибки SAM \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1048"><span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR\_SAM\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1049">8541 (0x215D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1049">8541 (0x215D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1050">Не удалось инициализировать диспетчер учетных записей безопасности из-за следующей ошибки: %1.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1050">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="ad39a-1051">Состояние ошибки: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1051">Error Status: 0x%2.</span></span> <span data-ttu-id="ad39a-1052">Нажмите кнопку ОК, чтобы завершить работу системы и перезагрузить компьютер в защищенном режиме.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1052">Click OK to shut down the system and reboot into Safe Mode.</span></span> <span data-ttu-id="ad39a-1053">Подробные сведения см. в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1053">Check the event log for detailed information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**Ошибка \_ при \_ \_ \_ отправке сведений о схеме DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1054"><span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR\_DS\_DRA\_SCHEMA\_INFO\_SHIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1055">8542 (0x215E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1055">8542 (0x215E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1056">Не удалось добавить сведения о схеме в запрос на репликацию.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1056">Schema information could not be included in the replication request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**Ошибка \_ при \_ \_ конфликте схемы DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1057"><span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERROR\_DS\_DRA\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1058">8543 (0x215F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1058">8543 (0x215F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1059">Не удалось завершить операцию репликации из-за несовместимости схемы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1059">The replication operation could not be completed due to a schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**произошла ошибка при \_ \_ \_ \_ конфликте схемы DS DRA более ранней версии \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1060"><span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERROR\_DS\_DRA\_EARLIER\_SCHEMA\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1061">8544 (0x2160)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1061">8544 (0x2160)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1062">Не удалось завершить операцию репликации из-за несовместимости предыдущей схемы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1062">The replication operation could not be completed due to a previous schema incompatibility.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**Ошибка \_ при \_ \_ \_ несовпадении NC obj DS DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1063"><span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR\_DS\_DRA\_OBJ\_NC\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1064">8545 (0x2161)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1064">8545 (0x2161)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1065">Не удалось применить обновление репликации, поскольку источник или назначение еще не получили сведения о последней операции перемещения между доменами.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1065">The replication update could not be applied because either the source or the destination has not yet received information regarding a recent cross-domain move operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**Ошибка \_ \_ NC DS \_ по-прежнему \_ имеет \_ DSA**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1066"><span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERROR\_DS\_NC\_STILL\_HAS\_DSAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1067">8546 (0x2162)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1067">8546 (0x2162)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1068">Не удалось удалить запрошенный домен, так как существуют контроллеры домена, на которых все еще размещен этот домен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1068">The requested domain could not be deleted because there exist domain controllers that still host this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**\_требуется ошибка \_ GC \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1069"><span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR\_DS\_GC\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1070">8547 (0x2163)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1070">8547 (0x2163)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1071">Запрошенную операцию можно выполнить только на сервере глобального каталога.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1071">The requested operation can be performed only on a global catalog server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**Ошибка \_ \_ локальный \_ член \_ локальной \_ \_ службы DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1072"><span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR\_DS\_LOCAL\_MEMBER\_OF\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1073">8548 (0x2164)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1073">8548 (0x2164)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1074">Локальная группа может быть членом только других локальных групп в том же домене.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1074">A local group can only be a member of other local groups in the same domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**Ошибка \_ DS \_ No \_ FPO \_ в \_ универсальных \_ группах**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1075"><span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR\_DS\_NO\_FPO\_IN\_UNIVERSAL\_GROUPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1076">8549 (0x2165)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1076">8549 (0x2165)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1077">Участники внешней безопасности не могут быть членами универсальных групп.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1077">Foreign security principals cannot be members of universal groups.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**Ошибка \_ DS не \_ удается \_ Добавить \_ в \_ GC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1078"><span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR\_DS\_CANT\_ADD\_TO\_GC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1079">8550 (0x2166)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1079">8550 (0x2166)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1080">Атрибут не может быть реплицирован в GC по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1080">The attribute is not allowed to be replicated to the GC because of security reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**Ошибка \_ DS \_ без \_ контрольной точки \_ с \_ основным контроллером домена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1081"><span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR\_DS\_NO\_CHECKPOINT\_WITH\_PDC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1082">8551 (0x2167)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1082">8551 (0x2167)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1083">Не удалось выполнить контрольную точку с основным контроллером домена, так как в настоящее время обрабатывается слишком много изменений.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1083">The checkpoint with the PDC could not be taken because there too many modifications being processed currently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**Ошибка \_ \_ аудита исходного кода DS \_ \_ не \_ включена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1084"><span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR\_DS\_SOURCE\_AUDITING\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1085">8552 (0x2168)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1085">8552 (0x2168)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1086">Для операции требуется включить аудит исходного домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1086">The operation requires that source domain auditing be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**Ошибка \_ \_ создания DS \_ \_ в \_ недомене \_ NC**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1087"><span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR\_DS\_CANT\_CREATE\_IN\_NONDOMAIN\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1088">8553 (0x2169)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1088">8553 (0x2169)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1089">Объекты субъектов безопасности могут создаваться только внутри контекстов именования доменов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1089">Security principal objects can only be created inside domain naming contexts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**Ошибка \_ DS \_ недопустимое \_ имя \_ \_ SPN**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1090"><span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR\_DS\_INVALID\_NAME\_FOR\_SPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1091">8554 (0x216A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1091">8554 (0x216A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1092">Не удалось создать имя субъекта-службы (SPN), так как указанное имя узла имеет формат, отличный от требуемого.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1092">A Service Principal Name (SPN) could not be constructed because the provided hostname is not in the necessary format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**Ошибка \_ \_ фильтра DS \_ использует \_ создается \_ attr**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1093"><span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERROR\_DS\_FILTER\_USES\_CONTRUCTED\_ATTRS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1094">8555 (0x216B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1094">8555 (0x216B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1095">Передан фильтр, использующий сконструированные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1095">A Filter was passed that uses constructed attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**Ошибка \_ DS \_ UNICODEPWD \_ не \_ в \_ кавычках**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1096"><span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR\_DS\_UNICODEPWD\_NOT\_IN\_QUOTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1097">8556 (0x216C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1097">8556 (0x216C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1098">Значение атрибута unicodePwd должно быть заключено в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1098">The unicodePwd attribute value must be enclosed in double quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**\_ \_ \_ \_ превышена квота учетной записи виртуальной машины DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1099"><span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1100">8557 (0x216D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1100">8557 (0x216D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1101">Не удалось присоединить компьютер к домену.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1101">Your computer could not be joined to the domain.</span></span> <span data-ttu-id="ad39a-1102">Превышено максимальное число учетных записей компьютеров, которое вы можете создать в этом домене.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1102">You have exceeded the maximum number of computer accounts you are allowed to create in this domain.</span></span> <span data-ttu-id="ad39a-1103">Чтобы сбросить или увеличить этот предел, обратитесь к системному администратору.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1103">Contact your system administrator to have this limit reset or increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**\_ \_ \_ \_ \_ на \_ летнем \_ контроллере домена должна выполняться ошибка DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1104"><span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**ERROR\_DS\_MUST\_BE\_RUN\_ON\_DST\_DC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1105">8558 (0x216E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1105">8558 (0x216E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1106">По соображениям безопасности операция должна выполняться на целевом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1106">For security reasons, the operation must be run on the destination DC.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**Ошибка \_ \_ \_ , так как для DS src DC \_ требуется \_ \_ пакет обновления 4 \_ или \_ более поздней версии**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1107"><span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR\_DS\_SRC\_DC\_MUST\_BE\_SP4\_OR\_GREATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1108">8559 (0x216F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1108">8559 (0x216F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1109">По соображениям безопасности исходный контроллер домена должен быть NT4SP4 или выше.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1109">For security reasons, the source DC must be NT4SP4 or greater.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**Ошибка \_ DS "не \_ удается \_ \_ удалить дерево удаление \_ критического \_ obj"**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1110"><span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR\_DS\_CANT\_TREE\_DELETE\_CRITICAL\_OBJ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1111">8560 (0x2170)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1111">8560 (0x2170)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1112">Критические системные объекты службы каталогов невозможно удалить во время операций удаления дерева.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1112">Critical Directory Service System objects cannot be deleted during tree delete operations.</span></span> <span data-ttu-id="ad39a-1113">Удаление дерева может быть выполнено частично.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1113">The tree delete may have been partially performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**Ошибка \_ \_ при инициализации \_ \_ оснастки DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1114"><span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR\_DS\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1115">8561 (0x2171)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1115">8561 (0x2171)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1116">Не удалось запустить службы каталогов из-за следующей ошибки: %1.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1116">Directory Services could not start because of the following error: %1.</span></span> <span data-ttu-id="ad39a-1117">Состояние ошибки: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1117">Error Status: 0x%2.</span></span> <span data-ttu-id="ad39a-1118">Нажмите кнопку "ОК", чтобы завершить работу системы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1118">Please click OK to shutdown the system.</span></span> <span data-ttu-id="ad39a-1119">Для дальнейшей диагностики системы можно использовать консоль восстановления.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1119">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**Ошибка \_ \_ \_ \_ при инициализации \_ консоли DS SAM**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1120"><span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR\_DS\_SAM\_INIT\_FAILURE\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1121">8562 (0x2172)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1121">8562 (0x2172)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1122">Не удалось инициализировать диспетчер учетных записей безопасности из-за следующей ошибки: %1.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1122">Security Accounts Manager initialization failed because of the following error: %1.</span></span> <span data-ttu-id="ad39a-1123">Состояние ошибки: 0x %2.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1123">Error Status: 0x%2.</span></span> <span data-ttu-id="ad39a-1124">Нажмите кнопку "ОК", чтобы завершить работу системы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1124">Please click OK to shutdown the system.</span></span> <span data-ttu-id="ad39a-1125">Для дальнейшей диагностики системы можно использовать консоль восстановления.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1125">You can use the recovery console to diagnose the system further.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**\_ \_ \_ \_ слишком высокая версия леса DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1126"><span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1127">8563 (0x2173)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1127">8563 (0x2173)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1128">Версия операционной системы несовместима с текущим режимом работы AD DSного леса или AD LDS режимом работы набора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1128">The version of the operating system is incompatible with the current AD DS forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="ad39a-1129">Необходимо выполнить обновление до новой версии операционной системы, чтобы этот сервер мог стать AD DS контроллером домена или добавить экземпляр AD LDS в этом AD DS лесу или в наборе конфигурации AD LDS.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1129">You must upgrade to a new version of the operating system before this server can become an AD DS Domain Controller or add an AD LDS Instance in this AD DS Forest or AD LDS Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**\_ \_ \_ \_ слишком высокая версия домена DS \_ с ошибками**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1130"><span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_HIGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1131">8564 (0x2174)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1131">8564 (0x2174)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1132">Установленная версия операционной системы несовместима с текущим режимом работы домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1132">The version of the operating system installed is incompatible with the current domain functional level.</span></span> <span data-ttu-id="ad39a-1133">Необходимо выполнить обновление до новой версии операционной системы, чтобы этот сервер мог стать контроллером домена в этом домене.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1133">You must upgrade to a new version of the operating system before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**\_нехватка \_ \_ версии леса \_ DS \_ с ошибкой**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1134"><span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR\_DS\_FOREST\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1135">8565 (0x2175)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1135">8565 (0x2175)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1136">Версия операционной системы, установленной на этом сервере, больше не поддерживает текущий функциональный уровень AD DS леса или AD LDS режим работы набора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1136">The version of the operating system installed on this server no longer supports the current AD DS Forest functional level or AD LDS Configuration Set functional level.</span></span> <span data-ttu-id="ad39a-1137">Чтобы этот сервер мог стать AD DS контроллером домена или экземпляром AD LDS в этом лесу или наборе конфигураций, необходимо повысить режим работы AD DSного леса или AD LDSного набора конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1137">You must raise the AD DS Forest functional level or AD LDS Configuration Set functional level before this server can become an AD DS Domain Controller or an AD LDS Instance in this Forest or Configuration Set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**\_ \_ \_ \_ слишком низкая версия домена DS \_ с ошибками**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1138"><span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR\_DS\_DOMAIN\_VERSION\_TOO\_LOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1139">8566 (0x2176)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1139">8566 (0x2176)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1140">Версия операционной системы, установленной на этом сервере, больше не поддерживает текущий режим работы домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1140">The version of the operating system installed on this server no longer supports the current domain functional level.</span></span> <span data-ttu-id="ad39a-1141">Чтобы этот сервер мог стать контроллером домена в этом домене, необходимо повысить режим работы домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1141">You must raise the domain functional level before this server can become a domain controller in this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**Ошибка \_ \_ несовместимая \_ версия DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1142"><span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR\_DS\_INCOMPATIBLE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1143">8567 (0x2177)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1143">8567 (0x2177)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1144">Версия операционной системы, установленной на этом сервере, несовместима с функциональным уровнем домена или леса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1144">The version of the operating system installed on this server is incompatible with the functional level of the domain or forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**\_нехватка \_ \_ версии DSA \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1145"><span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR\_DS\_LOW\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1146">8568 (0x2178)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1146">8568 (0x2178)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1147">Режим работы домена (или леса) не может быть повышен до запрошенного значения, так как в домене (или лесу) существует один или несколько контроллеров домена, которые имеют более низкий несовместимый функциональный уровень.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1147">The functional level of the domain (or forest) cannot be raised to the requested value, because there exist one or more domain controllers in the domain (or forest) that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**Ошибка \_ DS \_ без \_ \_ версии поведения \_ в \_ микседдомаин**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1148"><span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR\_DS\_NO\_BEHAVIOR\_VERSION\_IN\_MIXEDDOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1149">8569 (0x2179)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1149">8569 (0x2179)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1150">Режим работы леса не может быть повышен до запрошенного значения, так как один или несколько доменов по-прежнему находятся в режиме смешанного домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1150">The forest functional level cannot be raised to the requested value since one or more domains are still in mixed domain mode.</span></span> <span data-ttu-id="ad39a-1151">Для повышения функционального уровня леса все домены леса должны находиться в собственном режиме.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1151">All domains in the forest must be in native mode, for you to raise the forest functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**\_ \_ \_ неподдерживаемый \_ порядок сортировки \_ в DS.**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1152"><span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR\_DS\_NOT\_SUPPORTED\_SORT\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1153">8570 (0x217A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1153">8570 (0x217A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1154">Запрошенный порядок сортировки не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1154">The sort order requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**\_имя DS \_ ошибки \_ не является \_ уникальным**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1155"><span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR\_DS\_NAME\_NOT\_UNIQUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1156">8571 (0x217B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1156">8571 (0x217B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1157">Запрошенное имя уже существует в качестве уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1157">The requested name already exists as a unique identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**Ошибка \_ \_ учетной записи виртуальной машины DS, \_ \_ созданной \_ PRENT4**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1158"><span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR\_DS\_MACHINE\_ACCOUNT\_CREATED\_PRENT4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1159">8572 (0x217C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1159">8572 (0x217C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1160">Учетная запись компьютера была создана до NT4.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1160">The machine account was created pre-NT4.</span></span> <span data-ttu-id="ad39a-1161">Учетная запись должна быть создана повторно.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1161">The account needs to be recreated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**Ошибка \_ DS \_ из \_ \_ хранилища версий \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1162"><span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR\_DS\_OUT\_OF\_VERSION\_STORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1163">8573 (0x217D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1163">8573 (0x217D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1164">База данных находится вне хранилища версий.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1164">The database is out of version store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**\_используется ошибка \_ несовместимых \_ элементов управления \_ в DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1165"><span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR\_DS\_INCOMPATIBLE\_CONTROLS\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1166">8574 (0x217E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1166">8574 (0x217E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1167">Не удалось продолжить операцию, так как использовались несколько конфликтующих элементов управления.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1167">Unable to continue operation because multiple conflicting controls were used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**Ошибка \_ DS \_ без \_ \_ домена ссылок**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1168"><span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR\_DS\_NO\_REF\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1169">8575 (0x217F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1169">8575 (0x217F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1170">Не удалось найти допустимый домен ссылки на дескриптор безопасности для этой секции.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1170">Unable to find a valid security descriptor reference domain for this partition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**Ошибка \_ \_ зарезервированного \_ ИД ссылки DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1171"><span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERROR\_DS\_RESERVED\_LINK\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1172">8576 (0x2180)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1172">8576 (0x2180)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1173">Сбой обновления схемы: идентификатор ссылки зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1173">Schema update failed: The link identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**\_идентификатор ссылки DS "ошибка \_ \_ \_ \_ недоступен"**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1174"><span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERROR\_DS\_LINK\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1175">8577 (0x2181)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1175">8577 (0x2181)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1176">Не удалось обновить схему: нет доступных идентификаторов ссылок.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1176">Schema update failed: There are no link identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**Ошибка \_ \_ группы доступности \_ DS \_ не удается использовать \_ универсальный \_ член**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1177"><span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR\_DS\_AG\_CANT\_HAVE\_UNIVERSAL\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1178">8578 (0x2182)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1178">8578 (0x2182)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1179">Группа учетных записей не может иметь универсальную группу в качестве члена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1179">An account group cannot have a universal group as a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**Ошибка \_ DS \_ МОДИФИДН \_ , запрещенная \_ \_ типом экземпляра \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1180"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_INSTANCE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1181">8579 (0x2183)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1181">8579 (0x2183)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1182">Операции переименования или перемещения при именовании заголовков контекста или объектов, доступных только для чтения, запрещены.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1182">Rename or move operations on naming context heads or read-only objects are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**Ошибка \_ DS \_ без \_ \_ перемещения объектов \_ в \_ \_ NC схемы**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1183"><span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR\_DS\_NO\_OBJECT\_MOVE\_IN\_SCHEMA\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1184">8580 (0x2184)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1184">8580 (0x2184)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1185">Операции перемещения с объектами в контексте именования схемы не допускаются.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1185">Move operations on objects in the schema naming context are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**Ошибка \_ DS \_ МОДИФИДН \_ , запрещенная \_ \_ флагом**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1186"><span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR\_DS\_MODIFYDN\_DISALLOWED\_BY\_FLAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1187">8581 (0x2185)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1187">8581 (0x2185)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1188">Для объекта был установлен системный флаг, который не допускает перемещение или переименование объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1188">A system flag has been set on the object and does not allow the object to be moved or renamed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**Ошибка \_ DS \_ модифидн \_ неправильной \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1189"><span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR\_DS\_MODIFYDN\_WRONG\_GRANDPARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1190">8582 (0x2186)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1190">8582 (0x2186)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1191">Этому объекту запрещено изменять свой контейнер "бабушке".</span><span class="sxs-lookup"><span data-stu-id="ad39a-1191">This object is not allowed to change its grandparent container.</span></span> <span data-ttu-id="ad39a-1192">Перемещения для этого объекта запрещены, но ограничены одноуровневыми контейнерами.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1192">Moves are not forbidden on this object, but are restricted to sibling containers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**Ошибка \_ \_ имя DS \_ Ошибка \_ в \_ ссылке доверия**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1193"><span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERROR\_DS\_NAME\_ERROR\_TRUST\_REFERRAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1194">8583 (0x2187)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1194">8583 (0x2187)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1195">Не удалось полностью разрешить, создается ссылка на другой лес.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1195">Unable to resolve completely, a referral to another forest is generated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**Ошибка \_ не \_ поддерживается \_ на \_ стандартном \_ сервере**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1196"><span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR\_NOT\_SUPPORTED\_ON\_STANDARD\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1197">8584 (0x2188)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1197">8584 (0x2188)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1198">Запрошенное действие не поддерживается на стандартном сервере.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1198">The requested action is not supported on standard server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**Ошибка \_ DS не \_ удается \_ получить доступ к \_ удаленной \_ части \_ \_ AD**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1199"><span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR\_DS\_CANT\_ACCESS\_REMOTE\_PART\_OF\_AD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1200">8585 (0x2189)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1200">8585 (0x2189)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1201">Не удалось получить доступ к разделу службы каталогов, расположенной на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1201">Could not access a partition of the directory service located on a remote server.</span></span> <span data-ttu-id="ad39a-1202">Убедитесь, что по крайней мере один сервер работает для рассматриваемого раздела.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1202">Make sure at least one server is running for the partition in question.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**Ошибка \_ DS \_ CR \_ при \_ \_ проверке \_ v2**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1203"><span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR\_DS\_CR\_IMPOSSIBLE\_TO\_VALIDATE\_V2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1204">8586 (0x218A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1204">8586 (0x218A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1205">Каталог не может проверить предложенное имя контекста именования (или раздела), так как он не содержит реплики и не может связаться с репликой контекста именования выше предложенного контекста именования.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1205">The directory cannot validate the proposed naming context (or partition) name because it does not hold a replica nor can it contact a replica of the naming context above the proposed naming context.</span></span> <span data-ttu-id="ad39a-1206">Убедитесь, что родительский контекст именования правильно зарегистрирован в DNS, и хотя бы одна реплика этого контекста именования достижима хозяином именования доменов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1206">Please ensure that the parent naming context is properly registered in DNS, and at least one replica of this naming context is reachable by the Domain Naming master.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**\_ \_ превышен предел для потоков DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1207"><span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERROR\_DS\_THREAD\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1208">8587 (0x218B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1208">8587 (0x218B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1209">Превышено ограничение потока для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1209">The thread limit for this request was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**Ошибка \_ DS, \_ не \_ Ближайшая к**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1210"><span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR\_DS\_NOT\_CLOSEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1211">8588 (0x218C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1211">8588 (0x218C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1212">Сервер глобального каталога не находится на ближайшем сайте.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1212">The Global catalog server is not in the closest site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**Ошибка \_ DS \_ \_ не удается наследовать \_ SPN \_ без \_ ссылки на сервер \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1213"><span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_WITHOUT\_SERVER\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1214">8589 (0x218D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1214">8589 (0x218D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1215">DS не может наследовать имя участника-службы (SPN) для взаимной проверки подлинности целевого сервера, так как соответствующий объект сервера в локальной базе данных DS не имеет атрибута Серверреференце.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1215">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the corresponding server object in the local DS database has no serverReference attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**\_ \_ \_ сбой однопользовательского \_ режима \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1216"><span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR\_DS\_SINGLE\_USER\_MODE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1217">8590 (0x218E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1217">8590 (0x218E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1218">Службе каталогов не удалось войти в однопользовательский режим.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1218">The Directory Service failed to enter single user mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**Ошибка \_ при \_ \_ синтаксической \_ ошибке нтдскрипт DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1219"><span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**ERROR\_DS\_NTDSCRIPT\_SYNTAX\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1220">8591 (0x218F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1220">8591 (0x218F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1221">Службе каталогов не удается проанализировать скрипт из-за синтаксической ошибки.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1221">The Directory Service cannot parse the script because of a syntax error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**Ошибка \_ \_ процесса нтдскрипт \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1222"><span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERROR\_DS\_NTDSCRIPT\_PROCESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1223">8592 (0x2190)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1223">8592 (0x2190)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1224">Службе каталогов не удается обработать скрипт из-за ошибки.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1224">The Directory Service cannot process the script because of an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ОШИБКИ \_ DS \_ в \_ разных \_ эпохах REPL**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1225"><span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERROR\_DS\_DIFFERENT\_REPL\_EPOCHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1226">8593 (0x2191)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1226">8593 (0x2191)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1227">Службе каталогов не удается выполнить запрошенную операцию, так как вовлеченные серверы относятся к различным эпохам репликации (которые обычно связаны с выполняемым переименованием домена).</span><span class="sxs-lookup"><span data-stu-id="ad39a-1227">The directory service cannot perform the requested operation because the servers involved are of different replication epochs (which is usually related to a domain rename that is in progress).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**Ошибка \_ при \_ \_ изменении расширений DS DRS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1228"><span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERROR\_DS\_DRS\_EXTENSIONS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1229">8594 (0x2192)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1229">8594 (0x2192)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1230">Привязка службы каталогов должна быть повторно согласована из-за изменений в сведениях о серверных расширениях.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1230">The directory service binding must be renegotiated due to a change in the server extensions information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**\_ \_ \_ \_ \_ \_ \_ при \_ отключенном \_ CR не разрешено изменение набора реплик DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1231"><span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR\_DS\_REPLICA\_SET\_CHANGE\_NOT\_ALLOWED\_ON\_DISABLED\_CR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1232">8595 (0x2193)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1232">8595 (0x2193)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1233">Операция запрещена для отключенной перекрестной ссылки.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1233">Operation not allowed on a disabled cross ref.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**Ошибка \_ DS \_ нет \_ msDS \_ интид**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1234"><span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR\_DS\_NO\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1235">8596 (0x2194)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1235">8596 (0x2194)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1236">Ошибка обновления схемы: нет доступных значений для msDS-Интид.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1236">Schema update failed: No values for msDS-IntId are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**Ошибка \_ DS \_ DUP \_ msDS \_ интид**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1237"><span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR\_DS\_DUP\_MSDS\_INTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1238">8597 (0x2195)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1238">8597 (0x2195)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1239">Ошибка обновления схемы: повторяющаяся msDS-Интид.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1239">Schema update failed: Duplicate msDS-INtId.</span></span> <span data-ttu-id="ad39a-1240">Повторите операцию.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1240">Retry the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**\_ \_ \_ в \_ рднаттид существует ошибка DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1241"><span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERROR\_DS\_EXISTS\_IN\_RDNATTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1242">8598 (0x2196)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1242">8598 (0x2196)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1243">Сбой удаления схемы: атрибут используется в Рднаттид.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1243">Schema deletion failed: attribute is used in rDNAttID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**Ошибка \_ \_ авторизации DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1244"><span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR\_DS\_AUTHORIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1245">8599 (0x2197)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1245">8599 (0x2197)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1246">Службе каталогов не удалось авторизовать запрос.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1246">The directory service failed to authorize the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**Ошибка \_ \_ недопустимого \_ скрипта DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1247"><span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR\_DS\_INVALID\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1248">8600 (0x2198)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1248">8600 (0x2198)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1249">Службе каталогов не удается обработать скрипт, так как он недопустим.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1249">The Directory Service cannot process the script because it is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**Ошибка \_ \_ при удаленной \_ операции переcrossref DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1250"><span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR\_DS\_REMOTE\_CROSSREF\_OP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1251">8601 (0x2199)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1251">8601 (0x2199)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1252">Операция удаленного создания перекрестной ссылки завершилась сбоем в роли хозяина именования доменов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1252">The remote create cross reference operation failed on the Domain Naming Master FSMO.</span></span> <span data-ttu-id="ad39a-1253">Ошибка операции в расширенных данных.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1253">The operation's error is in the extended data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**Ошибка \_ " \_ Перекрестная ссылка DS" \_ \_ занята**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1254"><span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR\_DS\_CROSS\_REF\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1255">8602 (0x219A)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1255">8602 (0x219A)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1256">Перекрестная ссылка используется локально с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1256">A cross reference is in use locally with the same name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**Ошибка \_ DS не \_ удается \_ наследовать \_ SPN \_ для \_ удаленного \_ домена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1257"><span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR\_DS\_CANT\_DERIVE\_SPN\_FOR\_DELETED\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1258">8603 (0x219B)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1258">8603 (0x219B)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1259">ДОМЕНная служба не может наследовать имя участника-службы (SPN), с помощью которого осуществляется взаимная проверка подлинности целевого сервера, так как домен сервера был удален из леса.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1259">The DS cannot derive a service principal name (SPN) with which to mutually authenticate the target server because the server's domain has been deleted from the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**Ошибка \_ DS не \_ удается \_ понизить \_ с помощью NC с \_ возможностью записи \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1260"><span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR\_DS\_CANT\_DEMOTE\_WITH\_WRITEABLE\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1261">8604 (0x219C)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1261">8604 (0x219C)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1262">Доступные для записи NC предотвращают понижение роли контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1262">Writeable NCs prevent this DC from demoting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**\_ \_ обнаружена ошибка при дублировании \_ ИД DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1263"><span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR\_DS\_DUPLICATE\_ID\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1264">8605 (0x219D)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1264">8605 (0x219D)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1265">Запрошенный объект имеет неуникальный идентификатор и не может быть извлечен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1265">The requested object has a non-unique identifier and cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**Ошибка \_ DS \_ , недостаточная \_ \_ для \_ создания \_ объекта**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1266"><span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR\_DS\_INSUFFICIENT\_ATTR\_TO\_CREATE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1267">8606 (0x219E)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1267">8606 (0x219E)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1268">Предоставлено недостаточно атрибутов для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1268">Insufficient attributes were given to create an object.</span></span> <span data-ttu-id="ad39a-1269">Возможно, этот объект не существует, так как он был удален и уже собран сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1269">This object may not exist because it may have been deleted and already garbage collected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**Ошибка \_ \_ преобразования группы \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1270"><span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**ERROR\_DS\_GROUP\_CONVERSION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1271">8607 (0x219F)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1271">8607 (0x219F)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1272">Невозможно преобразовать группу из-за ограничений атрибута для запрошенного типа группы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1272">The group cannot be converted due to attribute restrictions on the requested group type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**Ошибка \_ DS \_ не \_ удается \_ Переместить \_ базовую \_ группу приложений**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1273"><span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_BASIC\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1274">8608 (0x21A0)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1274">8608 (0x21A0)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1275">Перемещение между доменами непустых основных групп приложений запрещено.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1275">Cross-domain move of non-empty basic application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**Ошибка \_ DS \_ не \_ удается \_ Переместить \_ группу запросов приложения \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1276"><span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR\_DS\_CANT\_MOVE\_APP\_QUERY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1277">8609 (0x21A1)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1277">8609 (0x21A1)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1278">Перемещение между доменами непустых групп приложений на основе запросов не допускается.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1278">Cross-domain move of non-empty query based application groups is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**роль DS с ОШИБКАми \_ \_ \_ не \_ проверена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1279"><span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERROR\_DS\_ROLE\_NOT\_VERIFIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1280">8610 (0x21A2)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1280">8610 (0x21A2)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1281">Не удалось проверить владение ролью FSMO, так как ее раздел каталога не был успешно реплицирован по крайней мере с одним партнером репликации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1281">The FSMO role ownership could not be verified because its directory partition has not replicated successfully with at least one replication partner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**\_ \_ контейнер ВКО DS \_ Error \_ не может \_ быть \_ Специальным**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1282"><span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERROR\_DS\_WKO\_CONTAINER\_CANNOT\_BE\_SPECIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1283">8611 (0x21A3)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1283">8611 (0x21A3)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1284">Целевой контейнер для перенаправления хорошо известного контейнера объектов еще не может быть специальным контейнером.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1284">The target container for a redirection of a well known object container cannot already be a special container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**Ошибка \_ \_ \_ при переименовании домена DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1285"><span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR\_DS\_DOMAIN\_RENAME\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1286">8612 (0x21A4)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1286">8612 (0x21A4)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1287">Службе каталогов не удается выполнить запрошенную операцию, поскольку выполняется операция переименования домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1287">The Directory Service cannot perform the requested operation because a domain rename operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**Ошибка \_ DS \_ существующий \_ \_ Дочерний \_ NC AD**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1288"><span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR\_DS\_EXISTING\_AD\_CHILD\_NC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1289">8613 (0x21A5)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1289">8613 (0x21A5)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1290">Служба каталогов обнаружила дочерний раздел под запрошенным именем секции.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1290">The directory service detected a child partition below the requested partition name.</span></span> <span data-ttu-id="ad39a-1291">Иерархия секций должна быть создана в нисходящем методе.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1291">The partition hierarchy must be created in a top down method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**\_ \_ \_ Превышено время существования DS REPL \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1292"><span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR\_DS\_REPL\_LIFETIME\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1293">8614 (0x21A6)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1293">8614 (0x21A6)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1294">Служба каталогов не может выполнить репликацию с этим сервером, так как время, прошедшее с момента последней репликации с этим сервером, превысило время существования захоронения.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1294">The directory service cannot replicate with this server because the time since the last replication with this server has exceeded the tombstone lifetime.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**\_ \_ \_ в \_ контейнере System запрещена \_ ошибка DS.**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1295"><span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR\_DS\_DISALLOWED\_IN\_SYSTEM\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1296">8615 (0x21A7)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1296">8615 (0x21A7)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1297">Запрошенная операция запрещена для объекта в контейнере системы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1297">The requested operation is not allowed on an object under the system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**Ошибка \_ \_ \_ \_ переполнения очереди отправки LDAP DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1298"><span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR\_DS\_LDAP\_SEND\_QUEUE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1299">8616 (0x21A8)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1299">8616 (0x21A8)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1300">Сетевая очередь отправки LDAP-серверов заполнена, так как клиент не обрабатывает результаты запросов достаточно быстро.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1300">The LDAP servers network send queue has filled up because the client is not processing the results of its requests fast enough.</span></span> <span data-ttu-id="ad39a-1301">Запросы больше не будут обрабатываться до тех пор, пока клиент не будет перехватываться.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1301">No more requests will be processed until the client catches up.</span></span> <span data-ttu-id="ad39a-1302">Если клиент не перехватится, он будет отключен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1302">If the client does not catch up then it will be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**Ошибка \_ в \_ \_ \_ \_ окне расписания DRA DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1303"><span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERROR\_DS\_DRA\_OUT\_SCHEDULE\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1304">8617 (0x21A9)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1304">8617 (0x21A9)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1305">Запланированная репликация не выполнялась, так как система слишком занята для выполнения запроса в окне расписания.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1305">The scheduled replication did not take place because the system was too busy to execute the request within the schedule window.</span></span> <span data-ttu-id="ad39a-1306">Очередь репликации перегружена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1306">The replication queue is overloaded.</span></span> <span data-ttu-id="ad39a-1307">Рекомендуется сократить число партнеров или уменьшить частоту запланированной репликации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1307">Consider reducing the number of partners or decreasing the scheduled replication frequency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**\_ \_ неизвестная политика DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1308"><span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR\_DS\_POLICY\_NOT\_KNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1309">8618 (0x21AA)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1309">8618 (0x21AA)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1310">В настоящее время невозможно определить, доступна ли политика репликации ветвей на контроллере домена концентратора.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1310">At this time, it cannot be determined if the branch replication policy is available on the hub domain controller.</span></span> <span data-ttu-id="ad39a-1311">Повторите попытку позже, чтобы учесть задержки репликации.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1311">Please retry at a later time to account for replication latencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**Ошибка \_ без \_ \_ объекта параметров \_ сайта**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1312"><span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR\_NO\_SITE\_SETTINGS\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1313">8619 (0x21AB)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1313">8619 (0x21AB)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1314">Объект параметров сайта для указанного сайта не существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1314">The site settings object for the specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**Ошибка \_ без \_ секретов**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1315"><span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR\_NO\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1316">8620 (0x21AC)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1316">8620 (0x21AC)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1317">Локальное хранилище учетных записей не содержит секретных материалов для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1317">The local account store does not contain secret material for the specified account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**Ошибка \_ не \_ \_ найден контроллер домена, доступный для записи \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1318"><span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR\_NO\_WRITABLE\_DC\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1319">8621 (0x21AD)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1319">8621 (0x21AD)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1320">Не удалось найти доступный для записи контроллер домена в домене.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1320">Could not find a writable domain controller in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**Ошибка \_ DS \_ без \_ \_ объекта сервера**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1321"><span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR\_DS\_NO\_SERVER\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1322">8622 (0x21AE)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1322">8622 (0x21AE)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1323">Объект сервера для контроллера домена не существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1323">The server object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**Ошибка \_ DS \_ без \_ объекта Ntdsa \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1324"><span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR\_DS\_NO\_NTDSA\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1325">8623 (0x21AF)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1325">8623 (0x21AF)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1326">Объект параметров NTDS для контроллера домена не существует.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1326">The NTDS Settings object for the domain controller does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**Ошибка \_ \_ поиска не \_ АСК \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1327"><span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR\_DS\_NON\_ASQ\_SEARCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1328">8624 (0x21B0)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1328">8624 (0x21B0)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1329">Запрошенная операция поиска не поддерживается для поиска АСК.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1329">The requested search operation is not supported for ASQ searches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**Ошибка \_ \_ аудита DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1330"><span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR\_DS\_AUDIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1331">8625 (0x21B1)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1331">8625 (0x21B1)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1332">Не удалось создать обязательное событие аудита для операции.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1332">A required audit event could not be generated for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**Ошибка \_ DS \_ недопустимое \_ \_ поддерево флага поиска \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1333"><span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_SUBTREE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1334">8626 (0x21B2)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1334">8626 (0x21B2)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1335">Недопустимые флаги поиска для атрибута.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1335">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="ad39a-1336">Бит индекса поддерева допустим только для атрибутов с одним значением.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1336">The subtree index bit is valid only on single valued attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**Ошибка \_ DS \_ Недопустимый \_ \_ кортеж флага поиска \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1337"><span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR\_DS\_INVALID\_SEARCH\_FLAG\_TUPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1338">8627 (0x21B3)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1338">8627 (0x21B3)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1339">Недопустимые флаги поиска для атрибута.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1339">The search flags for the attribute are invalid.</span></span> <span data-ttu-id="ad39a-1340">Бит индекса кортежа допустим только для атрибутов строк Юникода.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1340">The tuple index bit is valid only on attributes of Unicode strings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**\_ \_ \_ \_ слишком глубокая таблица иерархии \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1341"><span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR\_DS\_HIERARCHY\_TABLE\_TOO\_DEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1342">8628 (0x21B4)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1342">8628 (0x21B4)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1343">Слишком глубокая вложенность адресных книг.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1343">The address books are nested too deeply.</span></span> <span data-ttu-id="ad39a-1344">Не удалось построить таблицу иерархии.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1344">Failed to build the hierarchy table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**Ошибка \_ DS \_ DRA \_ поврежденный \_ \_ вектор УТД**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1345"><span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR\_DS\_DRA\_CORRUPT\_UTD\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1346">8629 (0x21B5)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1346">8629 (0x21B5)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1347">Указанный вектор rvalue характеристики для обновления поврежден.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1347">The specified up-to-date-ness vector is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**Ошибка \_ \_ секреты DS \_ DRA \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1348"><span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR\_DS\_DRA\_SECRETS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1349">8630 (0x21B6)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1349">8630 (0x21B6)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1350">Запрос на репликацию секретов запрещен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1350">The request to replicate secrets is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**Ошибка \_ \_ зарезервированного \_ идентификатора MAPI DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1351"><span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR\_DS\_RESERVED\_MAPI\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1352">8631 (0x21B7)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1352">8631 (0x21B7)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1353">Сбой обновления схемы: Идентификатор MAPI зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1353">Schema update failed: The MAPI identifier is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**\_ \_ Идентификатор MAPI DS \_ Error \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1354"><span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR\_DS\_MAPI\_ID\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1355">8632 (0x21B8)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1355">8632 (0x21B8)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1356">Ошибка обновления схемы: нет доступных идентификаторов MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1356">Schema update failed: There are no MAPI identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**Ошибка \_ при \_ \_ отсутствии \_ \_ секрета KRBTGT DS DRA**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1357"><span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR\_DS\_DRA\_MISSING\_KRBTGT\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1358">8633 (0x21B9)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1358">8633 (0x21B9)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1359">Сбой операции репликации из-за отсутствия необходимых атрибутов локального объекта KRBTGT.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1359">The replication operation failed because the required attributes of the local krbtgt object are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**\_имя домена службы "ошибка" \_ \_ \_ существует \_ в \_ лесу**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1360"><span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR\_DS\_DOMAIN\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1361">8634 (0x21BA)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1361">8634 (0x21BA)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1362">Доменное имя доверенного домена уже существует в лесу.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1362">The domain name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**\_ \_ \_ \_ \_ в \_ лесу существует ошибка "неструктурированное имя DS"**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1363"><span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR\_DS\_FLAT\_NAME\_EXISTS\_IN\_FOREST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1364">8635 (0x21BB)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1364">8635 (0x21BB)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1365">Неструктурированное имя доверенного домена уже существует в лесу.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1365">The flat name of the trusted domain already exists in the forest.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**Ошибка \_ недопустимое \_ \_ имя участника-пользователя \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1366"><span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR\_INVALID\_USER\_PRINCIPAL\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1367">8636 (0x21BC)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1367">8636 (0x21BC)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1368">Недопустимое имя участника-пользователя (UPN).</span><span class="sxs-lookup"><span data-stu-id="ad39a-1368">The User Principal Name (UPN) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**Ошибка \_ \_ \_ сопоставленной \_ группы OID DS \_ \_ не удается иметь \_ членов**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1369"><span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR\_DS\_OID\_MAPPED\_GROUP\_CANT\_HAVE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1370">8637 (0x21BD)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1370">8637 (0x21BD)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1371">Сопоставленные группы OID не могут иметь членов.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1371">OID mapped groups cannot have members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**Ошибка \_ \_ OID DS \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1372"><span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR\_DS\_OID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1373">8638 (0x21BE)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1373">8638 (0x21BE)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1374">Не удается найти указанный OID.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1374">The specified OID cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**Ошибка \_ \_ \_ перезапуска \_ целевого объекта DRA DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1375"><span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERROR\_DS\_DRA\_RECYCLED\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1376">8639 (0x21BF)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1376">8639 (0x21BF)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1377">Операция репликации завершилась сбоем, так как целевой объект, на который ссылается значение ссылки, перезапущен.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1377">The replication operation failed because the target object referred by a link value is recycled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**Ошибка \_ \_ неразрешенного \_ \_ перенаправления NC DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1378"><span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR\_DS\_DISALLOWED\_NC\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1379">8640 (0x21C0)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1379">8640 (0x21C0)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1380">Сбой операции перенаправления, так как целевой объект находится в NC, отличном от контекста именования домена текущего контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1380">The redirect operation failed because the target object is in a NC different from the domain NC of the current domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**Ошибка \_ DS \_ High \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1381"><span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR\_DS\_HIGH\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1382">8641 (0x21C1)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1382">8641 (0x21C1)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1383">Функциональный уровень набора конфигурации AD LDS не может быть понижен до запрошенного значения.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1383">The functional level of the AD LDS configuration set cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**Ошибка \_ с \_ высокой \_ версией DSA DS \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1384"><span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR\_DS\_HIGH\_DSA\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1385">8642 (0x21C2)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1385">8642 (0x21C2)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1386">Режим работы домена (или леса) не может быть понижен до запрошенного значения.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1386">The functional level of the domain (or forest) cannot be lowered to the requested value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**Ошибка \_ DS \_ Low \_ ADLDS \_ FFL**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1387"><span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR\_DS\_LOW\_ADLDS\_FFL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1388">8643 (0x21C3)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1388">8643 (0x21C3)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1389">Функциональный уровень AD LDS набора конфигурации не может быть получен к запрошенному значению, так как существует один или несколько экземпляров ADLDS, которые имеют более низкий несовместимый функциональный уровень.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1389">The functional level of the AD LDS configuration set cannot be raised to the requested value, because there exist one or more ADLDS instances that are at a lower incompatible functional level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**Ошибка \_ \_ SID домена \_ , совпадающее \_ с именем \_ локальной \_ рабочей станции**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1390"><span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**ERROR\_DOMAIN\_SID\_SAME\_AS\_LOCAL\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1391">8644 (0x21C4)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1391">8644 (0x21C4)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1392">Не удается выполнить присоединение к домену, так как идентификатор безопасности домена, который вы пытались присоединить, идентичен идентификатору безопасности этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1392">The domain join cannot be completed because the SID of the domain you attempted to join was identical to the SID of this machine.</span></span> <span data-ttu-id="ad39a-1393">Это симптом неправильной клонированной установки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1393">This is a symptom of an improperly cloned operating system install.</span></span> <span data-ttu-id="ad39a-1394">Для создания нового идентификатора безопасности компьютера необходимо запустить Sysprep на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1394">You should run sysprep on this machine in order to generate a new machine SID.</span></span> <span data-ttu-id="ad39a-1395">Дополнительные сведения см. по адресу <https://go.microsoft.com/fwlink/p/?linkid=168895>.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1395">Please see <https://go.microsoft.com/fwlink/p/?linkid=168895> for more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**Ошибка \_ \_ \_ при удалении проверки SAM \_ \_ в DS**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1396"><span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR\_DS\_UNDELETE\_SAM\_VALIDATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1397">8645 (0x21C5)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1397">8645 (0x21C5)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1398">Операция отмены удаления завершилась сбоем, так как имя учетной записи SAM или дополнительное имя учетной записи SAM объекта, для которого выполняется восстановление, конфликтует с существующим динамическим объектом.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1398">The undelete operation failed because the Sam Account Name or Additional Sam Account Name of the object being undeleted conflicts with an existing live object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ad39a-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**Ошибка при \_ неправильном \_ типе учетной записи \_**</span><span class="sxs-lookup"><span data-stu-id="ad39a-1399"><span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR\_INCORRECT\_ACCOUNT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad39a-1400">8646 (0x21C6)</span><span class="sxs-lookup"><span data-stu-id="ad39a-1400">8646 (0x21C6)</span></span>
</dt> <dt>



<span data-ttu-id="ad39a-1401">Система не является полномочным для указанной учетной записи и поэтому не может завершить операцию.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1401">The system is not authoritative for the specified account and therefore cannot complete the operation.</span></span> <span data-ttu-id="ad39a-1402">Повторите операцию, используя поставщик, связанный с этой учетной записью.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1402">Please retry the operation using the provider associated with this account.</span></span> <span data-ttu-id="ad39a-1403">Если это поставщик в Интернете, используйте сайт поставщика в Интернете.</span><span class="sxs-lookup"><span data-stu-id="ad39a-1403">If this is an online provider please use the provider's online site.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="ad39a-1404">Требования</span><span class="sxs-lookup"><span data-stu-id="ad39a-1404">Requirements</span></span>



| <span data-ttu-id="ad39a-1405">Требование</span><span class="sxs-lookup"><span data-stu-id="ad39a-1405">Requirement</span></span> | <span data-ttu-id="ad39a-1406">Значение</span><span class="sxs-lookup"><span data-stu-id="ad39a-1406">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad39a-1407">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad39a-1407">Minimum supported client</span></span><br/> | <span data-ttu-id="ad39a-1408">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ad39a-1408">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ad39a-1409">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad39a-1409">Minimum supported server</span></span><br/> | <span data-ttu-id="ad39a-1410">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad39a-1410">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad39a-1411">Header</span><span class="sxs-lookup"><span data-stu-id="ad39a-1411">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad39a-1412"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad39a-1412"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad39a-1413">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad39a-1413">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad39a-1414">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="ad39a-1414">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




