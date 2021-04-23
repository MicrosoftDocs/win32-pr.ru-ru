---
title: Метод Сетдевицередиректионтипе класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Девицередиректионтипе, которое управляет тем, какие устройства будут перенаправляться.
ms.assetid: d97a0a7d-a08e-4703-b0f0-ba5d20688dc8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетдевицередиректионтипе
- Службы удаленных рабочих столов метода Сетдевицередиректионтипе, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Сетдевицередиректионтипе
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetDeviceRedirectionType
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98b369e0b6031aa503e2f7f55860d004f63b7f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988572"
---
# <a name="setdeviceredirectiontype-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="93ebb-106">Метод Сетдевицередиректионтипе \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="93ebb-106">SetDeviceRedirectionType method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="93ebb-107">Задает свойство **девицередиректионтипе** , которое управляет тем, какие устройства будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="93ebb-107">Sets the **DeviceRedirectionType** property, which controls which devices will be redirected.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ebb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93ebb-108">Syntax</span></span>


```mof
uint32 SetDeviceRedirectionType(
  [in] uint32 DeviceRedirectionType
);
```



## <a name="parameters"></a><span data-ttu-id="93ebb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="93ebb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93ebb-110">*Девицередиректионтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="93ebb-110">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ebb-111">Тип перенаправления устройства.</span><span class="sxs-lookup"><span data-stu-id="93ebb-111">The device redirection type.</span></span>

<dt>

<span data-ttu-id="93ebb-112">0</span><span class="sxs-lookup"><span data-stu-id="93ebb-112">0</span></span>
</dt> <dd>

<span data-ttu-id="93ebb-113">Все устройства будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="93ebb-113">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="93ebb-114">1</span><span class="sxs-lookup"><span data-stu-id="93ebb-114">1</span></span>
</dt> <dd>

<span data-ttu-id="93ebb-115">Устройства не будут перенаправлены.</span><span class="sxs-lookup"><span data-stu-id="93ebb-115">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="93ebb-116">2</span><span class="sxs-lookup"><span data-stu-id="93ebb-116">2</span></span>
</dt> <dd>

<span data-ttu-id="93ebb-117">Указанные устройства не будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="93ebb-117">Specified devices will not be redirected.</span></span> <span data-ttu-id="93ebb-118">Свойства **дискдривесдисаблед**, **принтерсдисаблед**, **сериалпортсдисаблед**, **клипбоарддисаблед** и **плугандплайдевицесдисаблед** определяют, какие устройства не будут перенаправляться.</span><span class="sxs-lookup"><span data-stu-id="93ebb-118">The **DiskDrivesDisabled**, **PrintersDisabled**, **SerialPortsDisabled**, **ClipboardDisabled**, and **PlugAndPlayDevicesDisabled** properties control which devices will not be redirected.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93ebb-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93ebb-119">Return value</span></span>

<span data-ttu-id="93ebb-120">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="93ebb-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="93ebb-121">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="93ebb-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="93ebb-122">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="93ebb-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="93ebb-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93ebb-123">Remarks</span></span>

<span data-ttu-id="93ebb-124">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="93ebb-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="93ebb-125">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="93ebb-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="93ebb-126">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="93ebb-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="93ebb-127">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="93ebb-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="93ebb-128">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="93ebb-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="93ebb-129">Требования</span><span class="sxs-lookup"><span data-stu-id="93ebb-129">Requirements</span></span>



| <span data-ttu-id="93ebb-130">Требование</span><span class="sxs-lookup"><span data-stu-id="93ebb-130">Requirement</span></span> | <span data-ttu-id="93ebb-131">Значение</span><span class="sxs-lookup"><span data-stu-id="93ebb-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ebb-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93ebb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="93ebb-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="93ebb-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="93ebb-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93ebb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="93ebb-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93ebb-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="93ebb-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93ebb-136">Namespace</span></span><br/>                | <span data-ttu-id="93ebb-137">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="93ebb-137">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="93ebb-138">MOF</span><span class="sxs-lookup"><span data-stu-id="93ebb-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93ebb-139"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93ebb-139"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="93ebb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="93ebb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93ebb-141"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93ebb-141"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="93ebb-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93ebb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ebb-143">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="93ebb-143">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

