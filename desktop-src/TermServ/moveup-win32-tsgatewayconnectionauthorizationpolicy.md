---
title: Метод MoveUp класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Перемещает текущую политику авторизации подключений удаленный рабочий стол (RD \ 160; CAP) на одну точку вверх в том порядке, в котором RD \ 160; Вычисляются ограничения.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода MoveUp
- Службы удаленных рабочих столов метода MoveUp, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81973261d156328aa1f306c26dd8bd9bdd20511f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492987"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="3997b-106">Метод MoveUp \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="3997b-106">MoveUp method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="3997b-107">Перемещает текущую политику авторизации подключений удаленный рабочий стол (RD CAP) на одну точку вверх в порядке оценки политик удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3997b-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position up in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="3997b-108">Этот метод уменьшает свойство **Order** текущей политики авторизации подключений к удаленному рабочему столу и увеличивает свойство **Order** политики авторизации подключений удаленных рабочих столов, предшествующее текущему ограничению удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3997b-108">This method decrements the **Order** property of the current RD CAP and increments the **Order** property of the RD CAP that preceded the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="3997b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3997b-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="3997b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3997b-110">Parameters</span></span>

<span data-ttu-id="3997b-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3997b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3997b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3997b-112">Return value</span></span>

<span data-ttu-id="3997b-113">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3997b-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3997b-114">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3997b-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3997b-115">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3997b-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3997b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3997b-116">Remarks</span></span>

<span data-ttu-id="3997b-117">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="3997b-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3997b-118">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="3997b-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3997b-119">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="3997b-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3997b-120">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="3997b-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3997b-121">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3997b-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3997b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3997b-122">Requirements</span></span>



| <span data-ttu-id="3997b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3997b-123">Requirement</span></span> | <span data-ttu-id="3997b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3997b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3997b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3997b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3997b-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3997b-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3997b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3997b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3997b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3997b-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3997b-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3997b-129">Namespace</span></span><br/>                | <span data-ttu-id="3997b-130">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="3997b-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3997b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="3997b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3997b-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3997b-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3997b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3997b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3997b-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3997b-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3997b-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3997b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3997b-136">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="3997b-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="3997b-137">**Вниз**</span><span class="sxs-lookup"><span data-stu-id="3997b-137">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

