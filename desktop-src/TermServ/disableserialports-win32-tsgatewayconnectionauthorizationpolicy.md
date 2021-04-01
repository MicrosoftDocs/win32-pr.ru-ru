---
title: Метод Дисаблесериалпортс класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Сериалпортсдисаблед.
ms.assetid: 95c027e3-f76d-4335-84ac-93a1c3718e66
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисаблесериалпортс
- Службы удаленных рабочих столов метода Дисаблесериалпортс, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Дисаблесериалпортс
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableSerialPorts
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a4f6941f8bc98d7f8e424a984922ad1f6631c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801462"
---
# <a name="disableserialports-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="e3ef7-106">Метод Дисаблесериалпортс \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="e3ef7-106">DisableSerialPorts method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="e3ef7-107">Задает свойство **сериалпортсдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="e3ef7-107">Sets the **SerialPortsDisabled** property.</span></span> <span data-ttu-id="e3ef7-108">Если свойство **девицередиректионтипе** имеет значение 2, то свойство **сериалпортсдисаблед** управляет перенаправлением последовательных портов для сеансов, установленных с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="e3ef7-108">If the **DeviceRedirectionType** property has a value of "2", the **SerialPortsDisabled** property controls redirection of the serial ports for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ef7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3ef7-109">Syntax</span></span>


```mof
uint32 DisableSerialPorts(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="e3ef7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3ef7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3ef7-111">*Отключено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3ef7-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3ef7-112">Новое значение для свойства **сериалпортсдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="e3ef7-112">New value for the **SerialPortsDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3ef7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3ef7-113">Return value</span></span>

<span data-ttu-id="e3ef7-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e3ef7-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e3ef7-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e3ef7-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e3ef7-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e3ef7-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e3ef7-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3ef7-117">Remarks</span></span>

<span data-ttu-id="e3ef7-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="e3ef7-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e3ef7-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e3ef7-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e3ef7-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="e3ef7-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e3ef7-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e3ef7-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e3ef7-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e3ef7-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ef7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e3ef7-123">Requirements</span></span>



| <span data-ttu-id="e3ef7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e3ef7-124">Requirement</span></span> | <span data-ttu-id="e3ef7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e3ef7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ef7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3ef7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e3ef7-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e3ef7-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e3ef7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3ef7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e3ef7-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3ef7-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e3ef7-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3ef7-130">Namespace</span></span><br/>                | <span data-ttu-id="e3ef7-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e3ef7-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e3ef7-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e3ef7-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3ef7-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3ef7-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3ef7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e3ef7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3ef7-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3ef7-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e3ef7-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3ef7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ef7-137">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="e3ef7-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

