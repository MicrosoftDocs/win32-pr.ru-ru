---
title: Метод Сеткомпутерграупнамес класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Компутерграупнамес.
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сеткомпутерграупнамес
- Службы удаленных рабочих столов метода Сеткомпутерграупнамес, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сеткомпутерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415440"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="d4665-106">Метод Сеткомпутерграупнамес \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="d4665-106">SetComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="d4665-107">Задает свойство **компутерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="d4665-107">Sets the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4665-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4665-108">Syntax</span></span>


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="d4665-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4665-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4665-110">*Компутерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4665-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4665-111">Список имен групп компьютеров, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="d4665-111">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="d4665-112">Это значение может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="d4665-112">This value can be empty.</span></span> <span data-ttu-id="d4665-113">Имена имеют формат *домена \\ компутерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="d4665-113">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="d4665-114">Если указано значение, клиентский компьютер должен принадлежать к одной из этих групп компьютеров, чтобы пользователь был доступен на сервере шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="d4665-114">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4665-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4665-115">Return value</span></span>

<span data-ttu-id="d4665-116">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="d4665-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d4665-117">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d4665-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d4665-118">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d4665-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4665-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4665-119">Remarks</span></span>

<span data-ttu-id="d4665-120">Если в параметре *компутерграупнамес* указано несколько имен групп компьютеров и одно из имен не может быть обработано, никакие имена не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="d4665-120">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="d4665-121">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="d4665-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d4665-122">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d4665-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d4665-123">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="d4665-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d4665-124">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="d4665-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d4665-125">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d4665-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4665-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d4665-126">Requirements</span></span>



| <span data-ttu-id="d4665-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d4665-127">Requirement</span></span> | <span data-ttu-id="d4665-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d4665-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4665-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4665-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d4665-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4665-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d4665-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4665-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d4665-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4665-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d4665-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d4665-133">Namespace</span></span><br/>                | <span data-ttu-id="d4665-134">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="d4665-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d4665-135">MOF</span><span class="sxs-lookup"><span data-stu-id="d4665-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4665-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4665-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4665-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d4665-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4665-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4665-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d4665-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4665-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4665-140">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="d4665-140">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

