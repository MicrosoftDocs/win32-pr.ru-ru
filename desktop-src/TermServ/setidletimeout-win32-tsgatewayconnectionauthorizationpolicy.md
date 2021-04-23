---
title: Метод Сетидлетимеаут класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство IdleTimeout.
ms.assetid: 162224dd-e4d4-483f-9ec4-b87731bc5014
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетидлетимеаут
- Службы удаленных рабочих столов метода Сетидлетимеаут, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетидлетимеаут
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetIdleTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c166311477dc9de94ca6c9614e14ac98907b406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672861"
---
# <a name="setidletimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="c1773-106">Метод Сетидлетимеаут \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="c1773-106">SetIdleTimeout method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="c1773-107">Задает свойство **IdleTimeout** .</span><span class="sxs-lookup"><span data-stu-id="c1773-107">Sets the **IdleTimeout** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1773-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1773-108">Syntax</span></span>


```mof
uint32 SetIdleTimeout(
  [in] uint32 IdleTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="c1773-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1773-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1773-110">*IdleTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c1773-110">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1773-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1773-111">Type: **uint32**</span></span>

<span data-ttu-id="c1773-112">Новое значение времени ожидания в минутах.</span><span class="sxs-lookup"><span data-stu-id="c1773-112">The new timeout value, in minutes.</span></span> <span data-ttu-id="c1773-113">Значение 0 означает отсутствие времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="c1773-113">A value of 0 means there is no timeout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1773-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1773-114">Return value</span></span>

<span data-ttu-id="c1773-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1773-115">Type: **uint32**</span></span>

<span data-ttu-id="c1773-116">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="c1773-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c1773-117">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c1773-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c1773-118">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c1773-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c1773-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1773-119">Remarks</span></span>

<span data-ttu-id="c1773-120">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="c1773-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c1773-121">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c1773-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c1773-122">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="c1773-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c1773-123">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c1773-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c1773-124">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c1773-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1773-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c1773-125">Requirements</span></span>



| <span data-ttu-id="c1773-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c1773-126">Requirement</span></span> | <span data-ttu-id="c1773-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c1773-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1773-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1773-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c1773-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c1773-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c1773-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1773-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c1773-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1773-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c1773-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c1773-132">Namespace</span></span><br/>                | <span data-ttu-id="c1773-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c1773-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c1773-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c1773-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1773-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1773-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1773-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c1773-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1773-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1773-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c1773-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1773-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1773-139">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="c1773-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

