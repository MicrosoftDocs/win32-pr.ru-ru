---
title: Метод Дисаблеплугандплайдевицес класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Плугандплайдевицесдисаблед.
ms.assetid: 0cfe9fea-da93-47fa-a9ea-868c78890a53
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисаблеплугандплайдевицес
- Службы удаленных рабочих столов метода Дисаблеплугандплайдевицес, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Дисаблеплугандплайдевицес
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisablePlugAndPlayDevices
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7432d69fc8cd088af5d5a44a07b90f9d697348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414936"
---
# <a name="disableplugandplaydevices-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="78560-106">Метод Дисаблеплугандплайдевицес \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="78560-106">DisablePlugAndPlayDevices method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="78560-107">Задает свойство **плугандплайдевицесдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="78560-107">Sets the **PlugAndPlayDevicesDisabled** property.</span></span> <span data-ttu-id="78560-108">Если свойство **девицередиректионтипе** имеет значение 2, свойство **плугандплайдевицесдисаблед** управляет перенаправлением Самонастраивающийся устройств для сеансов, установленных с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="78560-108">If the **DeviceRedirectionType** property has a value of "2", the **PlugAndPlayDevicesDisabled** property controls redirection of Plug and Play devices for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="78560-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78560-109">Syntax</span></span>


```mof
uint32 DisablePlugAndPlayDevices(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="78560-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="78560-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78560-111">*Отключено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78560-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78560-112">Новое значение для свойства **плугандплайдевицесдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="78560-112">New value for the **PlugAndPlayDevicesDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78560-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78560-113">Return value</span></span>

<span data-ttu-id="78560-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="78560-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="78560-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="78560-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="78560-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="78560-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78560-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78560-117">Remarks</span></span>

<span data-ttu-id="78560-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="78560-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="78560-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="78560-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="78560-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="78560-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="78560-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="78560-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="78560-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="78560-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="78560-123">Требования</span><span class="sxs-lookup"><span data-stu-id="78560-123">Requirements</span></span>



| <span data-ttu-id="78560-124">Требование</span><span class="sxs-lookup"><span data-stu-id="78560-124">Requirement</span></span> | <span data-ttu-id="78560-125">Значение</span><span class="sxs-lookup"><span data-stu-id="78560-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="78560-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78560-126">Minimum supported client</span></span><br/> | <span data-ttu-id="78560-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="78560-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="78560-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78560-128">Minimum supported server</span></span><br/> | <span data-ttu-id="78560-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78560-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="78560-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="78560-130">Namespace</span></span><br/>                | <span data-ttu-id="78560-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="78560-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="78560-132">MOF</span><span class="sxs-lookup"><span data-stu-id="78560-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78560-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78560-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="78560-134">DLL</span><span class="sxs-lookup"><span data-stu-id="78560-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78560-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78560-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="78560-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78560-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78560-137">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="78560-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

