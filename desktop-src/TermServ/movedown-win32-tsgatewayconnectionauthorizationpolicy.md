---
title: Метод вниз класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Перемещает текущую политику авторизации подключений удаленный рабочий стол (RD \ 160; CAP) на одну точку вниз в том порядке, в котором RD \ 160; Вычисляются ограничения.
ms.assetid: 57349e59-e200-4789-bbcb-d474eacde39d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода вниз
- Службы удаленных рабочих столов метода вниз, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод вниз
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e5b2e2b56a60d78f827f8989c0317cb003e511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672876"
---
# <a name="movedown-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="d52a6-106">Метод вниз \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="d52a6-106">MoveDown method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="d52a6-107">Перемещает текущую политику авторизации подключений удаленный рабочий стол (RD CAP) на одну точку вниз в порядке оценки политик удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="d52a6-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position down in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="d52a6-108">Этот метод увеличивает свойство **Order** текущей политики авторизации подключений к удаленному рабочему столу и уменьшает свойство **Order** политики авторизации подключений удаленных рабочих столов, за которым следует текущая политика авторизации подключений удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="d52a6-108">This method increments the **Order** property of the current RD CAP and decrements the **Order** property of the RD CAP that followed the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="d52a6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d52a6-109">Syntax</span></span>


```mof
uint32 MoveDown();
```



## <a name="parameters"></a><span data-ttu-id="d52a6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d52a6-110">Parameters</span></span>

<span data-ttu-id="d52a6-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d52a6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d52a6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d52a6-112">Return value</span></span>

<span data-ttu-id="d52a6-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="d52a6-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d52a6-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="d52a6-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d52a6-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d52a6-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d52a6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d52a6-116">Remarks</span></span>

<span data-ttu-id="d52a6-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="d52a6-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d52a6-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d52a6-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d52a6-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="d52a6-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d52a6-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="d52a6-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d52a6-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d52a6-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d52a6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d52a6-122">Requirements</span></span>



| <span data-ttu-id="d52a6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d52a6-123">Requirement</span></span> | <span data-ttu-id="d52a6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d52a6-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d52a6-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d52a6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d52a6-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d52a6-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d52a6-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d52a6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d52a6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d52a6-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d52a6-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d52a6-129">Namespace</span></span><br/>                | <span data-ttu-id="d52a6-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="d52a6-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d52a6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d52a6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d52a6-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d52a6-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d52a6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d52a6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d52a6-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d52a6-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d52a6-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d52a6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d52a6-136">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="d52a6-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="d52a6-137">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="d52a6-137">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

