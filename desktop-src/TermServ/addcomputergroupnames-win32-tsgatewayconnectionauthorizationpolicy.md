---
title: Метод Аддкомпутерграупнамес класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Добавляет указанные имена групп компьютеров в свойство Компутерграупнамес.
ms.assetid: f0c440d6-0cc2-48b4-b656-65f12e652151
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддкомпутерграупнамес
- Службы удаленных рабочих столов метода Аддкомпутерграупнамес, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Аддкомпутерграупнамес
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72647ef66b9e2eeaed824b3e77c404214786b615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136339"
---
# <a name="addcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="4f73b-106">Метод Аддкомпутерграупнамес \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="4f73b-106">AddComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="4f73b-107">Добавляет указанные имена групп компьютеров в свойство **компутерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="4f73b-107">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f73b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f73b-108">Syntax</span></span>


```mof
uint32 AddComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="4f73b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f73b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f73b-110">*Компутерграупнамес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f73b-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f73b-111">Разделенный точками с запятой список имен групп компьютеров, добавляемых в свойство **компутерграупнамес** .</span><span class="sxs-lookup"><span data-stu-id="4f73b-111">Semicolon-separated list of computer group names to add to the **ComputerGroupNames** property.</span></span> <span data-ttu-id="4f73b-112">Имена групп компьютеров должны иметь формат *домена \\ компутерграупнаме*.</span><span class="sxs-lookup"><span data-stu-id="4f73b-112">Computer group names should be of the format *Domain\\ComputerGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f73b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f73b-113">Return value</span></span>

<span data-ttu-id="4f73b-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="4f73b-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4f73b-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="4f73b-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4f73b-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4f73b-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f73b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f73b-117">Remarks</span></span>

<span data-ttu-id="4f73b-118">Если в параметре *компутерграупнамес* указано несколько имен групп компьютеров и одно из имен не может быть обработано, никакие имена не будут обработаны.</span><span class="sxs-lookup"><span data-stu-id="4f73b-118">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="4f73b-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="4f73b-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4f73b-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4f73b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4f73b-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="4f73b-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4f73b-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4f73b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4f73b-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4f73b-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f73b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4f73b-124">Requirements</span></span>



| <span data-ttu-id="4f73b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4f73b-125">Requirement</span></span> | <span data-ttu-id="4f73b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4f73b-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f73b-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f73b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4f73b-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4f73b-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4f73b-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f73b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4f73b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f73b-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4f73b-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4f73b-131">Namespace</span></span><br/>                | <span data-ttu-id="4f73b-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="4f73b-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4f73b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="4f73b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f73b-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f73b-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f73b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4f73b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f73b-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f73b-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4f73b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f73b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f73b-138">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="4f73b-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

