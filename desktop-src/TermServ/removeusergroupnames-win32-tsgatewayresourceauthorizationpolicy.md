---
title: Метод Ремовеусерграупнамес класса Win32_TSGatewayResourceAuthorizationPolicy
description: Удаляет указанные имена групп пользователей из существующих групп пользователей в свойстве Усерграупнамес.
ms.assetid: 8538e41a-b9ae-43ce-b19a-40a40f9a12f5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовеусерграупнамес
- Службы удаленных рабочих столов метода Ремовеусерграупнамес, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Ремовеусерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.RemoveUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6746eaa9d6a7c3cfd82512a4b9f632c873bc9f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672658"
---
# <a name="removeusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="e6cda-106">Метод Ремовеусерграупнамес \_ класса Win32 тсгатевайресаурцеаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="e6cda-106">RemoveUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="e6cda-107">Удаляет указанные имена групп пользователей из существующих групп пользователей в свойстве **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="e6cda-107">Removes the specified user group names from the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6cda-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6cda-108">Syntax</span></span>


```mof
uint32 RemoveUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="e6cda-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6cda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6cda-110">*Усерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6cda-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6cda-111">Разделенный точками с запятой список имен групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="e6cda-111">Semicolon-separated list of user group names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6cda-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6cda-112">Return value</span></span>

<span data-ttu-id="e6cda-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e6cda-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e6cda-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e6cda-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e6cda-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e6cda-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6cda-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e6cda-116">Remarks</span></span>

<span data-ttu-id="e6cda-117">Если в параметре *усерграупнамес* указано несколько имен групп пользователей и одно из имен не может быть обработано, никакие имена не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="e6cda-117">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="e6cda-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="e6cda-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e6cda-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e6cda-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e6cda-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="e6cda-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e6cda-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e6cda-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e6cda-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e6cda-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6cda-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e6cda-123">Requirements</span></span>



| <span data-ttu-id="e6cda-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e6cda-124">Requirement</span></span> | <span data-ttu-id="e6cda-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e6cda-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6cda-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6cda-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e6cda-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e6cda-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e6cda-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6cda-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e6cda-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6cda-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e6cda-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e6cda-130">Namespace</span></span><br/>                | <span data-ttu-id="e6cda-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e6cda-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e6cda-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e6cda-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6cda-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6cda-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6cda-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e6cda-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6cda-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6cda-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e6cda-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6cda-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6cda-137">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="e6cda-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

