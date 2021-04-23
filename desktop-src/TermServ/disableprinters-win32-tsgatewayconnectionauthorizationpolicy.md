---
title: Метод Дисаблепринтерс класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Принтерсдисаблед. Если свойство Девицередиректионтипе имеет значение \ 0034; 2 \ 0034;, свойство Принтерсдисаблед управляет перенаправлением принтеров для сеансов, установленных с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: bf58d226-e3de-4c2b-aaa9-9e7ddbf49d31
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисаблепринтерс
- Службы удаленных рабочих столов метода Дисаблепринтерс, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Дисаблепринтерс
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePrinters
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1625425170bd5e29b953db8299048261e9351bff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672512"
---
# <a name="disableprinters-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="2d518-107">Метод Дисаблепринтерс \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="2d518-107">DisablePrinters method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="2d518-108">Задает свойство **принтерсдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="2d518-108">Sets the **PrintersDisabled** property.</span></span> <span data-ttu-id="2d518-109">Если свойство **девицередиректионтипе** имеет значение 2, то свойство **принтерсдисаблед** управляет перенаправлением принтеров для сеансов, которые устанавливаются с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="2d518-109">If the **DeviceRedirectionType** property has a value of "2", the **PrintersDisabled** property controls redirection of the printers for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d518-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d518-110">Syntax</span></span>


```mof
uint32 DisablePrinters(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="2d518-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d518-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d518-112">*Отключено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d518-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d518-113">Новое значение для свойства **принтерсдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="2d518-113">New value for the **PrintersDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d518-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d518-114">Return value</span></span>

<span data-ttu-id="2d518-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="2d518-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2d518-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="2d518-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2d518-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2d518-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d518-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d518-118">Remarks</span></span>

<span data-ttu-id="2d518-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="2d518-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2d518-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="2d518-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2d518-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="2d518-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2d518-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="2d518-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2d518-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2d518-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d518-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2d518-124">Requirements</span></span>



| <span data-ttu-id="2d518-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2d518-125">Requirement</span></span> | <span data-ttu-id="2d518-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2d518-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d518-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d518-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2d518-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2d518-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2d518-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d518-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2d518-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d518-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2d518-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2d518-131">Namespace</span></span><br/>                | <span data-ttu-id="2d518-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="2d518-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2d518-133">MOF</span><span class="sxs-lookup"><span data-stu-id="2d518-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d518-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d518-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d518-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2d518-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d518-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d518-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2d518-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d518-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d518-138">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="2d518-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

