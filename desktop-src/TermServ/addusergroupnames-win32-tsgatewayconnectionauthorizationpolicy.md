---
title: Метод Аддусерграупнамес класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Добавляет указанные имена групп пользователей в свойство Усерграупнамес.
ms.assetid: 01bbccc3-c2e4-46ad-8649-1a30e001c949
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддусерграупнамес
- Службы удаленных рабочих столов метода Аддусерграупнамес, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Аддусерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a4fe26b27f954e5ea9a0c7ac666592f74337a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415092"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="f7e49-106">Метод Аддусерграупнамес \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="f7e49-106">AddUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="f7e49-107">Добавляет указанные имена групп пользователей в свойство **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="f7e49-107">Adds the specified user group names to the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e49-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7e49-108">Syntax</span></span>


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="f7e49-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7e49-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7e49-110">*Усерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f7e49-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7e49-111">Разделенный точками с запятой список имен групп пользователей, добавляемых в свойство **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="f7e49-111">Semicolon-separated list of user group names to add to the **UserGroupNames** property.</span></span> <span data-ttu-id="f7e49-112">Имена групп пользователей должны иметь формат *домена \\ усерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="f7e49-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7e49-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7e49-113">Return value</span></span>

<span data-ttu-id="f7e49-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="f7e49-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f7e49-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f7e49-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f7e49-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f7e49-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7e49-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7e49-117">Remarks</span></span>

<span data-ttu-id="f7e49-118">Если в параметре *усерграупнамес* указано несколько имен групп пользователей и одно из имен не может быть обработано, никакие имена не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="f7e49-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="f7e49-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="f7e49-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f7e49-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f7e49-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f7e49-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f7e49-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f7e49-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f7e49-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f7e49-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f7e49-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7e49-124">Требования</span><span class="sxs-lookup"><span data-stu-id="f7e49-124">Requirements</span></span>



| <span data-ttu-id="f7e49-125">Требование</span><span class="sxs-lookup"><span data-stu-id="f7e49-125">Requirement</span></span> | <span data-ttu-id="f7e49-126">Значение</span><span class="sxs-lookup"><span data-stu-id="f7e49-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7e49-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7e49-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f7e49-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f7e49-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f7e49-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7e49-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f7e49-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7e49-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f7e49-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7e49-131">Namespace</span></span><br/>                | <span data-ttu-id="f7e49-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f7e49-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f7e49-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f7e49-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7e49-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7e49-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7e49-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f7e49-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7e49-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7e49-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f7e49-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7e49-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7e49-138">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="f7e49-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

