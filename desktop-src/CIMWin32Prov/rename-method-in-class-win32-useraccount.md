---
description: Переименовывает имя учетной записи пользователя.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Метод Rename класса Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142322"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a><span data-ttu-id="ace2d-103">Метод Rename класса Win32 \_ UserAccount</span><span class="sxs-lookup"><span data-stu-id="ace2d-103">Rename method of the Win32\_UserAccount class</span></span>

<span data-ttu-id="ace2d-104">Метод класса **Rename** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) переименовывает имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="ace2d-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a user account name.</span></span>

<span data-ttu-id="ace2d-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="ace2d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ace2d-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ace2d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ace2d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ace2d-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="ace2d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ace2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace2d-109">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ace2d-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-110">Новое имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ace2d-110">New account name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace2d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ace2d-111">Return value</span></span>

<span data-ttu-id="ace2d-112">Возвращает одно из значений, перечисленных в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="ace2d-112">Returns one of the values listed in the following list.</span></span> <span data-ttu-id="ace2d-113">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ace2d-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ace2d-114">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ace2d-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ace2d-115">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="ace2d-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-116">0</span><span class="sxs-lookup"><span data-stu-id="ace2d-116">0</span></span>

<span data-ttu-id="ace2d-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ace2d-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-118">**Экземпляр не найден**</span><span class="sxs-lookup"><span data-stu-id="ace2d-118">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-119">1</span><span class="sxs-lookup"><span data-stu-id="ace2d-119">1</span></span>

<span data-ttu-id="ace2d-120">Экземпляр не найден.</span><span class="sxs-lookup"><span data-stu-id="ace2d-120">Instance not found.</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-121">**Требуется экземпляр**</span><span class="sxs-lookup"><span data-stu-id="ace2d-121">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-122">2</span><span class="sxs-lookup"><span data-stu-id="ace2d-122">2</span></span>

<span data-ttu-id="ace2d-123">Требуется экземпляр.</span><span class="sxs-lookup"><span data-stu-id="ace2d-123">Instance required.</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-124">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="ace2d-124">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-125">3</span><span class="sxs-lookup"><span data-stu-id="ace2d-125">3</span></span>

<span data-ttu-id="ace2d-126">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ace2d-126">Invalid parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-127">**Пользователь не найден**</span><span class="sxs-lookup"><span data-stu-id="ace2d-127">**User not found**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-128">4</span><span class="sxs-lookup"><span data-stu-id="ace2d-128">4</span></span>

<span data-ttu-id="ace2d-129">Пользователь не найден.</span><span class="sxs-lookup"><span data-stu-id="ace2d-129">User not found.</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-130">**Домен не найден**</span><span class="sxs-lookup"><span data-stu-id="ace2d-130">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-131">5</span><span class="sxs-lookup"><span data-stu-id="ace2d-131">5</span></span>

<span data-ttu-id="ace2d-132">Домен не найден.</span><span class="sxs-lookup"><span data-stu-id="ace2d-132">Domain not found.</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-133">**Операция разрешена только на основном контроллере домена**</span><span class="sxs-lookup"><span data-stu-id="ace2d-133">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-134">6</span><span class="sxs-lookup"><span data-stu-id="ace2d-134">6</span></span>

<span data-ttu-id="ace2d-135">Операция разрешена только на основном контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="ace2d-135">Operation is allowed only on the primary domain controller of the domain.</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-136">**Операция не разрешена для последней учетной записи администратора.**</span><span class="sxs-lookup"><span data-stu-id="ace2d-136">**Operation is not allowed on the last administrative account.**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-137">7</span><span class="sxs-lookup"><span data-stu-id="ace2d-137">7</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-138">**Операция не разрешена для указанных специальных групп. пользователь, администратор, локальный или гость.**</span><span class="sxs-lookup"><span data-stu-id="ace2d-138">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-139">8</span><span class="sxs-lookup"><span data-stu-id="ace2d-139">8</span></span>

<span data-ttu-id="ace2d-140">Операция запрещена для указанных специальных групп: пользователь, администратор, локальный или гость.</span><span class="sxs-lookup"><span data-stu-id="ace2d-140">Operation is not allowed on specified special groups: user, admin, local, or guest.</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-141">**Другая ошибка API**</span><span class="sxs-lookup"><span data-stu-id="ace2d-141">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-142">9</span><span class="sxs-lookup"><span data-stu-id="ace2d-142">9</span></span>

<span data-ttu-id="ace2d-143">Другая ошибка API.</span><span class="sxs-lookup"><span data-stu-id="ace2d-143">Other API error.</span></span>

</dd> <dt>

<span data-ttu-id="ace2d-144">**Внутренняя ошибка**</span><span class="sxs-lookup"><span data-stu-id="ace2d-144">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="ace2d-145">10</span><span class="sxs-lookup"><span data-stu-id="ace2d-145">10</span></span>

<span data-ttu-id="ace2d-146">Внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="ace2d-146">Internal error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ace2d-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ace2d-147">Remarks</span></span>

<span data-ttu-id="ace2d-148">Эта функция реализуется как метод для предоставления отдельного контекста для нового имени, которое отличается от значения свойства ключа для имени, связанного с изменяемым экземпляром.</span><span class="sxs-lookup"><span data-stu-id="ace2d-148">This functionality is implemented as a method to provide a separate context for the new name that is distinguishable from the key property value for Name that is associated with the instance to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace2d-149">Требования</span><span class="sxs-lookup"><span data-stu-id="ace2d-149">Requirements</span></span>



| <span data-ttu-id="ace2d-150">Требование</span><span class="sxs-lookup"><span data-stu-id="ace2d-150">Requirement</span></span> | <span data-ttu-id="ace2d-151">Значение</span><span class="sxs-lookup"><span data-stu-id="ace2d-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ace2d-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ace2d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ace2d-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ace2d-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ace2d-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ace2d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ace2d-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ace2d-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ace2d-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ace2d-156">Namespace</span></span><br/>                | <span data-ttu-id="ace2d-157">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ace2d-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ace2d-158">MOF</span><span class="sxs-lookup"><span data-stu-id="ace2d-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ace2d-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ace2d-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ace2d-160">DLL</span><span class="sxs-lookup"><span data-stu-id="ace2d-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace2d-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace2d-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ace2d-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ace2d-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace2d-163">**\_UserAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="ace2d-163">**Win32\_UserAccount**</span></span>](win32-useraccount.md)
</dt> <dt>

<span data-ttu-id="ace2d-164">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ace2d-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

