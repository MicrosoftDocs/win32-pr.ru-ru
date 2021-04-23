---
title: Метод Енаблерекуестсох класса Win32_TSGatewayServerSettings
description: Енаблерекуестсох больше не доступен.
ms.assetid: 4feb7530-cced-4ead-a1fb-679b81442bb3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблерекуестсох
- Службы удаленных рабочих столов метода Енаблерекуестсох, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Енаблерекуестсох
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableRequestSOH
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90ed6a3929b50d13a27ec559aab534f9e06f738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672820"
---
# <a name="enablerequestsoh-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="ad3bc-106">Метод Енаблерекуестсох \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="ad3bc-106">EnableRequestSOH method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="ad3bc-107">\[Метод **енаблерекуестсох** больше не доступен в Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="ad3bc-107">\[The **EnableRequestSOH** method is no longer available as of Windows Server 2016.\]</span></span>

<span data-ttu-id="ad3bc-108">Включает или отключает запросы состояния работоспособности (SoH).</span><span class="sxs-lookup"><span data-stu-id="ad3bc-108">Enables or disables requests for a Statement of Health (SoH).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad3bc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad3bc-109">Syntax</span></span>


```mof
uint32 EnableRequestSOH(
  [in] boolean RequestSOH
);
```



## <a name="parameters"></a><span data-ttu-id="ad3bc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad3bc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad3bc-111">*Рекуестсох* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad3bc-111">*RequestSOH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad3bc-112">Укажите **значение true** , чтобы включить функцию, или **значение false** , чтобы отключить эту функцию.</span><span class="sxs-lookup"><span data-stu-id="ad3bc-112">Specify **TRUE** to enable the feature or **FALSE** to disable the feature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad3bc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad3bc-113">Return value</span></span>

<span data-ttu-id="ad3bc-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="ad3bc-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ad3bc-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="ad3bc-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ad3bc-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ad3bc-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ad3bc-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad3bc-117">Remarks</span></span>

<span data-ttu-id="ad3bc-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="ad3bc-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ad3bc-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ad3bc-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ad3bc-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ad3bc-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ad3bc-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ad3bc-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ad3bc-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ad3bc-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad3bc-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ad3bc-123">Requirements</span></span>



| <span data-ttu-id="ad3bc-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ad3bc-124">Requirement</span></span> | <span data-ttu-id="ad3bc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ad3bc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad3bc-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad3bc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ad3bc-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ad3bc-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ad3bc-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad3bc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ad3bc-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad3bc-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ad3bc-130">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="ad3bc-130">End of server support</span></span><br/>    | <span data-ttu-id="ad3bc-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ad3bc-131">Windows Server 2012 R2</span></span><br/>                                                        |
| <span data-ttu-id="ad3bc-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ad3bc-132">Namespace</span></span><br/>                | <span data-ttu-id="ad3bc-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="ad3bc-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ad3bc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ad3bc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad3bc-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad3bc-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad3bc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ad3bc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad3bc-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad3bc-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ad3bc-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad3bc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad3bc-139">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="ad3bc-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

