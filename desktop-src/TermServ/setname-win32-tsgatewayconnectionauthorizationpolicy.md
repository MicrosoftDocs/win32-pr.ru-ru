---
title: Метод SetName класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает новое имя для этой удаленный рабочий стол политики авторизации подключений (RD \ 160; CAP).
ms.assetid: 4a3b71d4-9b1c-46ea-b14a-fcbe32af37b5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetName
- Службы удаленных рабочих столов метода SetName, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15fa4c374f5686f8cddbe99b5a464e6f84b4a12a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802111"
---
# <a name="setname-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="6e5ef-106">Метод SetName \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="6e5ef-106">SetName method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="6e5ef-107">Задает новое имя для этой удаленный рабочий стол политики авторизации подключений (RD CAP).</span><span class="sxs-lookup"><span data-stu-id="6e5ef-107">Sets a new name for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e5ef-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e5ef-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="6e5ef-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e5ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e5ef-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6e5ef-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e5ef-111">Имя политики авторизации подключений к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-111">Name of the RD CAP.</span></span> <span data-ttu-id="6e5ef-112">Имя должно содержать 64 символов или меньше, уникально (регистр игнорируется) и не может включать следующие зарезервированные символы:</span><span class="sxs-lookup"><span data-stu-id="6e5ef-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="6e5ef-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="6e5ef-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="6e5ef-114">\*\[Вкладка\]</span><span class="sxs-lookup"><span data-stu-id="6e5ef-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e5ef-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e5ef-115">Return value</span></span>

<span data-ttu-id="6e5ef-116">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6e5ef-117">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6e5ef-118">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6e5ef-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6e5ef-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e5ef-119">Remarks</span></span>

<span data-ttu-id="6e5ef-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6e5ef-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6e5ef-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6e5ef-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="6e5ef-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6e5ef-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="6e5ef-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6e5ef-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6e5ef-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e5ef-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6e5ef-125">Requirements</span></span>



| <span data-ttu-id="6e5ef-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6e5ef-126">Requirement</span></span> | <span data-ttu-id="6e5ef-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6e5ef-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e5ef-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e5ef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6e5ef-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6e5ef-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6e5ef-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e5ef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6e5ef-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e5ef-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6e5ef-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e5ef-132">Namespace</span></span><br/>                | <span data-ttu-id="6e5ef-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="6e5ef-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6e5ef-134">MOF</span><span class="sxs-lookup"><span data-stu-id="6e5ef-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e5ef-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ef-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e5ef-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6e5ef-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e5ef-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e5ef-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6e5ef-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e5ef-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e5ef-139">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="6e5ef-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

