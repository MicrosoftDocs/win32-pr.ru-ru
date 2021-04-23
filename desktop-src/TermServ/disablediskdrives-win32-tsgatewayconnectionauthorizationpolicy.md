---
title: Метод Дисабледискдривес класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Задает свойство Дискдривесдисаблед.
ms.assetid: bdc4a923-bda7-464a-95eb-95231374ac93
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Дисабледискдривес
- Службы удаленных рабочих столов метода Дисабледискдривес, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Дисабледискдривес
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.DisableDiskDrives
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63938ccae6e93e23bd754c1d18ede0008fe92257
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414937"
---
# <a name="disablediskdrives-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="0087d-106">Метод Дисабледискдривес \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="0087d-106">DisableDiskDrives method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="0087d-107">Задает свойство **дискдривесдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="0087d-107">Sets the **DiskDrivesDisabled** property.</span></span> <span data-ttu-id="0087d-108">Если свойство **девицередиректионтипе** имеет значение 2, то свойство **дискдривесдисаблед** управляет перенаправлением дисковых дисков клиента для сеансов, установленных с помощью сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="0087d-108">If the **DeviceRedirectionType** property has a value of "2", the **DiskDrivesDisabled** property controls redirection of the client disk drives for sessions that are established through the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0087d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0087d-109">Syntax</span></span>


```mof
uint32 DisableDiskDrives(
  [in] boolean Disabled
);
```



## <a name="parameters"></a><span data-ttu-id="0087d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0087d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0087d-111">*Отключено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0087d-111">*Disabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0087d-112">Новое значение для свойства **дискдривесдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="0087d-112">New value for the **DiskDrivesDisabled** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0087d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0087d-113">Return value</span></span>

<span data-ttu-id="0087d-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="0087d-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0087d-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0087d-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0087d-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0087d-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0087d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0087d-117">Remarks</span></span>

<span data-ttu-id="0087d-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="0087d-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0087d-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0087d-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0087d-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="0087d-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0087d-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0087d-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0087d-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0087d-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0087d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0087d-123">Requirements</span></span>



| <span data-ttu-id="0087d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0087d-124">Requirement</span></span> | <span data-ttu-id="0087d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0087d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0087d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0087d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0087d-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0087d-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0087d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0087d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0087d-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0087d-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0087d-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0087d-130">Namespace</span></span><br/>                | <span data-ttu-id="0087d-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0087d-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0087d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0087d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0087d-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0087d-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0087d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0087d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0087d-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0087d-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0087d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0087d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0087d-137">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="0087d-137">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

