---
title: Метод Дисаблеклипбоард класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Клипбоарддисаблед. Если свойство Девицередиректионтипе имеет значение \ 0034; 2 \ 0034;, свойство Клипбоарддисаблед управляет перенаправлением буфера обмена для сеансов, установленных с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).
ms.assetid: c53fc802-958b-452d-9af9-0ce89ed46079
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисаблеклипбоард
- Службы удаленных рабочих столов метода Дисаблеклипбоард, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Дисаблеклипбоард
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableClipboard
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ae2070a35fa31f1c9d9ad31e9e632e31c0193f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681778"
---
# <a name="disableclipboard-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="26ebc-107">Метод Дисаблеклипбоард \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="26ebc-107">DisableClipboard method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="26ebc-108">Задает свойство **клипбоарддисаблед** .</span><span class="sxs-lookup"><span data-stu-id="26ebc-108">Sets the **ClipboardDisabled** property.</span></span> <span data-ttu-id="26ebc-109">Если свойство **девицередиректионтипе** имеет значение 2, то свойство **клипбоарддисаблед** управляет перенаправлением буфера обмена для сеансов, установленных с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="26ebc-109">If the **DeviceRedirectionType** property has a value of "2", the **ClipboardDisabled** property controls redirection of the clipboard for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ebc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26ebc-110">Syntax</span></span>


```mof
uint32 DisableClipboard(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="26ebc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="26ebc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ebc-112">*Отключено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26ebc-112">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ebc-113">Новое значение для свойства **клипбоарддисаблед** .</span><span class="sxs-lookup"><span data-stu-id="26ebc-113">New value for the **ClipboardDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ebc-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26ebc-114">Return value</span></span>

<span data-ttu-id="26ebc-115">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="26ebc-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="26ebc-116">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="26ebc-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="26ebc-117">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="26ebc-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="26ebc-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26ebc-118">Remarks</span></span>

<span data-ttu-id="26ebc-119">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="26ebc-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="26ebc-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="26ebc-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="26ebc-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="26ebc-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="26ebc-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="26ebc-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="26ebc-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="26ebc-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="26ebc-124">Требования</span><span class="sxs-lookup"><span data-stu-id="26ebc-124">Requirements</span></span>



| <span data-ttu-id="26ebc-125">Требование</span><span class="sxs-lookup"><span data-stu-id="26ebc-125">Requirement</span></span> | <span data-ttu-id="26ebc-126">Значение</span><span class="sxs-lookup"><span data-stu-id="26ebc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="26ebc-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26ebc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="26ebc-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="26ebc-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="26ebc-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26ebc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="26ebc-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26ebc-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="26ebc-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="26ebc-131">Namespace</span></span><br/>                | <span data-ttu-id="26ebc-132">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="26ebc-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="26ebc-133">MOF</span><span class="sxs-lookup"><span data-stu-id="26ebc-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26ebc-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26ebc-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="26ebc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="26ebc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26ebc-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26ebc-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="26ebc-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26ebc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ebc-138">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="26ebc-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

