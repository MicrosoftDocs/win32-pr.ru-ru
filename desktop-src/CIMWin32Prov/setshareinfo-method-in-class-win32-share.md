---
description: Сетшареинфо&\# 8194; Метод класса WMI задает параметры общего ресурса.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Метод Сетшареинфо класса Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262774"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a><span data-ttu-id="aa2a4-103">Метод Сетшареинфо \_ класса общего ресурса Win32</span><span class="sxs-lookup"><span data-stu-id="aa2a4-103">SetShareInfo method of the Win32\_Share class</span></span>

<span data-ttu-id="aa2a4-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) сетшареинфо задает параметры общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-104">The **SetShareInfo** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the parameters of a shared resource.</span></span>

<span data-ttu-id="aa2a4-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="aa2a4-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="aa2a4-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="aa2a4-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa2a4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa2a4-107">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="aa2a4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa2a4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa2a4-109">*MaximumAllowed* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="aa2a4-109">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aa2a4-110">Максимальное число пользователей, которым разрешено использовать этот ресурс одновременно.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-110">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

<span data-ttu-id="aa2a4-111">Пример: 10.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-111">Example: 10.</span></span> <span data-ttu-id="aa2a4-112">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-112">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="aa2a4-113">*Описание* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="aa2a4-113">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aa2a4-114">Необязательный комментарий для описания ресурса, к которому предоставляется общий доступ.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-114">Optional comment to describe the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="aa2a4-115">*Доступ к* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="aa2a4-115">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aa2a4-116">Дескриптор безопасности для разрешений уровня пользователя.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-116">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="aa2a4-117">Дескриптор безопасности содержит сведения о разрешениях, владельце и доступе ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-117">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="aa2a4-118">Дополнительные сведения см. в разделе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="aa2a4-118">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa2a4-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa2a4-119">Return value</span></span>

<span data-ttu-id="aa2a4-120">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-120">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="aa2a4-121">**Успешно** (0)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-121">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-122">**Отказано в доступе** (2)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-122">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-123">**Неизвестный сбой** (8)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-123">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-124">**Недопустимое имя** (9)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-124">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-125">**Недопустимый уровень** (10)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-125">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-126">**Недопустимый параметр** (21)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-126">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-127">**Повторяющаяся общая папка** (22)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-127">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-128">**Путь перенаправления** (23)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-128">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-129">**Неизвестное устройство или каталог** (24)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-129">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-130">**Не найдено сетевое имя** (25)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-130">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="aa2a4-131">**Другие** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="aa2a4-131">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="aa2a4-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa2a4-132">Remarks</span></span>

<span data-ttu-id="aa2a4-133">Метод **сетшареинфо** является динамическим методом объекта и используется для вхождения этого класса.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-133">**SetShareInfo** method is a dynamic object method and is used on an occurrence of this class.</span></span>

<span data-ttu-id="aa2a4-134">Только члены локальной группы "Администраторы" или "Операторы учетных записей" или пользователи с членством в группе операторов связи, печати или сервера могут успешно выполнять **сетшареинфо**.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-134">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **SetShareInfo**.</span></span> <span data-ttu-id="aa2a4-135">Оператор Print может устанавливать только очереди принтера.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-135">The print operator can only set printer queues.</span></span> <span data-ttu-id="aa2a4-136">Оператор связи может устанавливать только очереди устройств связи.</span><span class="sxs-lookup"><span data-stu-id="aa2a4-136">The Communication operator can only set communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="aa2a4-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="aa2a4-137">Examples</span></span>

<span data-ttu-id="aa2a4-138">Следующий пример PowerShell обновляет имя общей папки **невшаре** .</span><span class="sxs-lookup"><span data-stu-id="aa2a4-138">The following PowerShell sample updates the name of the **newShare** share.</span></span>


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



## <a name="requirements"></a><span data-ttu-id="aa2a4-139">Требования</span><span class="sxs-lookup"><span data-stu-id="aa2a4-139">Requirements</span></span>



| <span data-ttu-id="aa2a4-140">Требование</span><span class="sxs-lookup"><span data-stu-id="aa2a4-140">Requirement</span></span> | <span data-ttu-id="aa2a4-141">Значение</span><span class="sxs-lookup"><span data-stu-id="aa2a4-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa2a4-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa2a4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="aa2a4-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa2a4-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa2a4-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa2a4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="aa2a4-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa2a4-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa2a4-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aa2a4-146">Namespace</span></span><br/>                | <span data-ttu-id="aa2a4-147">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aa2a4-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa2a4-148">MOF</span><span class="sxs-lookup"><span data-stu-id="aa2a4-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa2a4-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa2a4-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa2a4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="aa2a4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa2a4-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa2a4-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa2a4-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa2a4-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa2a4-153">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa2a4-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="aa2a4-154">**\_Общий ресурс Win32**</span><span class="sxs-lookup"><span data-stu-id="aa2a4-154">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

