---
title: Метод Delete класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Удаляет текущую политику авторизации подключений удаленный рабочий стол (RD \ 160; CAP).
ms.assetid: aef7216a-4459-492b-95cb-87ea760dcde9
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Delete
- Службы удаленных рабочих столов метода Delete, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26b99cf7856c31f2e45f026631beb974e61c481f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681780"
---
# <a name="delete-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="2ce42-106">Метод DELETE \_ класса Тсгатевайконнектионаусоризатионполици Win32</span><span class="sxs-lookup"><span data-stu-id="2ce42-106">Delete method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="2ce42-107">Удаляет текущую политику авторизации подключений удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="2ce42-107">Deletes the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce42-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ce42-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="2ce42-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ce42-109">Parameters</span></span>

<span data-ttu-id="2ce42-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2ce42-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ce42-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ce42-111">Return value</span></span>

<span data-ttu-id="2ce42-112">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="2ce42-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2ce42-113">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2ce42-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2ce42-114">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2ce42-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce42-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ce42-115">Remarks</span></span>

<span data-ttu-id="2ce42-116">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="2ce42-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2ce42-117">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="2ce42-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2ce42-118">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="2ce42-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2ce42-119">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="2ce42-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2ce42-120">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2ce42-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce42-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2ce42-121">Requirements</span></span>



| <span data-ttu-id="2ce42-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2ce42-122">Requirement</span></span> | <span data-ttu-id="2ce42-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2ce42-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce42-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ce42-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2ce42-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2ce42-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2ce42-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ce42-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2ce42-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ce42-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2ce42-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2ce42-128">Namespace</span></span><br/>                | <span data-ttu-id="2ce42-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="2ce42-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2ce42-130">MOF</span><span class="sxs-lookup"><span data-stu-id="2ce42-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ce42-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ce42-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ce42-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2ce42-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ce42-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ce42-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2ce42-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ce42-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce42-135">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="2ce42-135">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

