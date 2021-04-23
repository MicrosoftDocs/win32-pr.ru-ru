---
title: Метод Аддусерграупнамес класса Win32_TSGatewayResourceAuthorizationPolicy
description: Добавляет указанный разделенный точками с запятой список имен групп пользователей в существующие группы пользователей в свойстве Усерграупнамес.
ms.assetid: 9cd18ecd-ad56-49c7-954a-2d67bbd7b1db
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддусерграупнамес
- Службы удаленных рабочих столов метода Аддусерграупнамес, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Аддусерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c5c3fcb57c60ff2ca4c14d2e42ff0acdc84f0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988346"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="0c0eb-106">Метод Аддусерграупнамес \_ класса Win32 тсгатевайресаурцеаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="0c0eb-106">AddUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="0c0eb-107">Добавляет указанный разделенный точками с запятой список имен групп пользователей в существующие группы пользователей в свойстве **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="0c0eb-107">Adds the specified semicolon-separated list of user group names to the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c0eb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c0eb-108">Syntax</span></span>


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="0c0eb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c0eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c0eb-110">*Усерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c0eb-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c0eb-111">Разделенный точками с запятой список имен групп пользователей, добавляемых в свойство **усерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="0c0eb-111">Semicolon-separated list of user group names to add to the **UserGroupNames** property.</span></span> <span data-ttu-id="0c0eb-112">Имена групп пользователей должны иметь формат *домена \\ усерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c0eb-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c0eb-113">Return value</span></span>

<span data-ttu-id="0c0eb-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0c0eb-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0c0eb-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0c0eb-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0c0eb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c0eb-117">Remarks</span></span>

<span data-ttu-id="0c0eb-118">Если в параметре *усерграупнамес* указано несколько имен групп пользователей и одно из имен не может быть обработано, никакие имена не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="0c0eb-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0c0eb-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0c0eb-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0c0eb-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="0c0eb-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0c0eb-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0c0eb-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0c0eb-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c0eb-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0c0eb-124">Requirements</span></span>



| <span data-ttu-id="0c0eb-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0c0eb-125">Requirement</span></span> | <span data-ttu-id="0c0eb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0c0eb-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c0eb-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c0eb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0c0eb-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c0eb-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0c0eb-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c0eb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0c0eb-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c0eb-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0c0eb-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0c0eb-131">Namespace</span></span><br/>                | <span data-ttu-id="0c0eb-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0c0eb-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0c0eb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0c0eb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c0eb-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c0eb-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c0eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0c0eb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c0eb-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c0eb-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0c0eb-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c0eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c0eb-138">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="0c0eb-138">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

