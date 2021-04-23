---
title: Метод Сетусерграупнамес класса Win32_TSGatewayResourceAuthorizationPolicy
description: Задает свойство Усерграупнамес для политики авторизации ресурсов удаленный рабочий стол (RD \ 160; RAP).
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетусерграупнамес
- Службы удаленных рабочих столов метода Сетусерграупнамес, класс Win32_TSGatewayResourceAuthorizationPolicy
- Класс Win32_TSGatewayResourceAuthorizationPolicy службы удаленных рабочих столов, метод Сетусерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708d3eb3a6cc08cd94ba56979fc482a92a530646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136306"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="b16d7-106">Метод Сетусерграупнамес \_ класса Win32 тсгатевайресаурцеаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="b16d7-106">SetUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="b16d7-107">Задает свойство **усерграупнамес** для политики авторизации ресурсов (RD RAP) удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="b16d7-107">Sets the **UserGroupNames** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="b16d7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b16d7-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="b16d7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b16d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b16d7-110">*Усерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b16d7-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b16d7-111">Разделенный точками с запятой список имен групп пользователей.</span><span class="sxs-lookup"><span data-stu-id="b16d7-111">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="b16d7-112">Имена имеют формат *домена \\ усерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="b16d7-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="b16d7-113">Если пользователь принадлежит к любой из этих групп пользователей, доступ будет разрешен.</span><span class="sxs-lookup"><span data-stu-id="b16d7-113">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b16d7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b16d7-114">Return value</span></span>

<span data-ttu-id="b16d7-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="b16d7-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b16d7-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b16d7-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b16d7-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b16d7-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b16d7-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b16d7-118">Remarks</span></span>

<span data-ttu-id="b16d7-119">Если в параметре *усерграупнамес* указано несколько имен групп пользователей и одно из имен не может быть обработано, никакие имена не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="b16d7-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="b16d7-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="b16d7-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b16d7-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b16d7-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b16d7-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="b16d7-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b16d7-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="b16d7-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b16d7-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b16d7-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b16d7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b16d7-125">Requirements</span></span>



| <span data-ttu-id="b16d7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b16d7-126">Requirement</span></span> | <span data-ttu-id="b16d7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b16d7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b16d7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b16d7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b16d7-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b16d7-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b16d7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b16d7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b16d7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b16d7-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b16d7-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b16d7-132">Namespace</span></span><br/>                | <span data-ttu-id="b16d7-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b16d7-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b16d7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b16d7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b16d7-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b16d7-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b16d7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b16d7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b16d7-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b16d7-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b16d7-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b16d7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b16d7-139">**\_Тсгатевайресаурцеаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="b16d7-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

