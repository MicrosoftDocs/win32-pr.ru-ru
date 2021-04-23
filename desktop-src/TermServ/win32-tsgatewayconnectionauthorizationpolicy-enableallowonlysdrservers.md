---
title: Метод Енаблеалловонлисдрсерверс класса Win32_TSGatewayConnectionAuthorizationPolicy
description: Используется для переключения свойства Алловонлисдрсерверс.
ms.assetid: ec7f22bc-4e80-4ece-9567-5f405207480e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблеалловонлисдрсерверс
- Службы удаленных рабочих столов метода Енаблеалловонлисдрсерверс, класс Win32_TSGatewayConnectionAuthorizationPolicy
- Класс Win32_TSGatewayConnectionAuthorizationPolicy службы удаленных рабочих столов, метод Енаблеалловонлисдрсерверс
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.EnableAllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f031cff46e0fafdce80a995d2d4778875c1d56f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802092"
---
# <a name="enableallowonlysdrservers-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="c5089-106">Метод Енаблеалловонлисдрсерверс \_ класса Win32 тсгатевайконнектионаусоризатионполици</span><span class="sxs-lookup"><span data-stu-id="c5089-106">EnableAllowOnlySDRServers method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="c5089-107">Используется для переключения свойства **алловонлисдрсерверс** .</span><span class="sxs-lookup"><span data-stu-id="c5089-107">Used to toggle the **AllowOnlySDRServers** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5089-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5089-108">Syntax</span></span>


```mof
uint32 EnableAllowOnlySDRServers(
  [in] boolean AllowOnlySDRServers
);
```



## <a name="parameters"></a><span data-ttu-id="c5089-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5089-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5089-110">*Алловонлисдрсерверс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5089-110">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5089-111">Если задано значение **true**, подключения будут разрешены только для защиты RDS-серверов перенаправления устройств (SDR).</span><span class="sxs-lookup"><span data-stu-id="c5089-111">If set to **True**, connections will be allowed only to secure device redirection (SDR) RDS servers.</span></span> <span data-ttu-id="c5089-112">Если задано значение **false**, то подключения будут разрешены более старым СЕРВЕРАм RDS.</span><span class="sxs-lookup"><span data-stu-id="c5089-112">If set to **False**, connections will be allowed to older RDS servers also</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5089-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5089-113">Return value</span></span>

<span data-ttu-id="c5089-114">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="c5089-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c5089-115">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c5089-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c5089-116">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c5089-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5089-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c5089-117">Requirements</span></span>



| <span data-ttu-id="c5089-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c5089-118">Requirement</span></span> | <span data-ttu-id="c5089-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c5089-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5089-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5089-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c5089-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c5089-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c5089-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5089-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c5089-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c5089-123">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="c5089-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c5089-124">Namespace</span></span><br/>                | <span data-ttu-id="c5089-125">КОРНЕВой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c5089-125">ROOT\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c5089-126">MOF</span><span class="sxs-lookup"><span data-stu-id="c5089-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5089-127"><dt>TsGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5089-127"><dt>TsGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5089-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c5089-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5089-129"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5089-129"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c5089-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5089-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5089-131">**\_Тсгатевайконнектионаусоризатионполици Win32**</span><span class="sxs-lookup"><span data-stu-id="c5089-131">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

 





