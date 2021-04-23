---
title: Метод Сетусерграупнамес класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Усерграупнамес для политики авторизации подключений удаленный рабочий стол (RD \ 160; CAP).
ms.assetid: 03c9b2c5-8769-46f2-941f-302d798dd3a1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетусерграупнамес
- Службы удаленных рабочих столов метода Сетусерграупнамес, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетусерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ca948b63cd106e7284b00c2c5f9e54c6dfa86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672828"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="eef2a-106">Метод Сетусерграупнамес \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="eef2a-106">SetUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="eef2a-107">Задает свойство **усерграупнамес** для этой удаленный рабочий стол политики авторизации подключений (RD CAP).</span><span class="sxs-lookup"><span data-stu-id="eef2a-107">Sets the **UserGroupNames** property for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="eef2a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eef2a-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="eef2a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eef2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eef2a-110">*Усерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eef2a-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eef2a-111">Список имен групп пользователей, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="eef2a-111">List of semicolon-separated user group names.</span></span> <span data-ttu-id="eef2a-112">Имена имеют формат *домена \\ усерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="eef2a-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="eef2a-113">Если пользователь принадлежит к любой из этих групп пользователей, ему будет разрешен доступ к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="eef2a-113">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eef2a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eef2a-114">Return value</span></span>

<span data-ttu-id="eef2a-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="eef2a-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="eef2a-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="eef2a-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="eef2a-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="eef2a-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eef2a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eef2a-118">Remarks</span></span>

<span data-ttu-id="eef2a-119">Если в параметре *усерграупнамес* указано несколько имен групп пользователей и одно из имен не может быть обработано, никакие имена не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="eef2a-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="eef2a-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="eef2a-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="eef2a-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="eef2a-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eef2a-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="eef2a-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eef2a-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="eef2a-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eef2a-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eef2a-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eef2a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="eef2a-125">Requirements</span></span>



| <span data-ttu-id="eef2a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="eef2a-126">Requirement</span></span> | <span data-ttu-id="eef2a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="eef2a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef2a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eef2a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="eef2a-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="eef2a-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="eef2a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eef2a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="eef2a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eef2a-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="eef2a-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eef2a-132">Namespace</span></span><br/>                | <span data-ttu-id="eef2a-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="eef2a-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="eef2a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="eef2a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eef2a-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eef2a-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="eef2a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="eef2a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eef2a-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eef2a-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="eef2a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eef2a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef2a-139">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="eef2a-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

