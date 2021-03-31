---
title: Метод Истранспортенаблед класса Win32_TSGatewayServerSettings
description: Определяет, включен ли указанный транспорт.
ms.assetid: 3f08a206-5800-4088-a113-bb3f0cc826f2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Истранспортенаблед
- Службы удаленных рабочих столов метода Истранспортенаблед, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Истранспортенаблед
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsTransportEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da152499138f6c1aba1ff6477c719aa0e787deee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135755"
---
# <a name="istransportenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="e4705-106">Метод Истранспортенаблед \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="e4705-106">IsTransportEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="e4705-107">Определяет, включен ли указанный транспорт.</span><span class="sxs-lookup"><span data-stu-id="e4705-107">Determines whether the specified transport is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4705-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4705-108">Syntax</span></span>


```mof
uint32 IsTransportEnabled(
  [in]  uint16  TransportType,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="e4705-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4705-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4705-110">*TransportType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4705-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4705-111">Указывает тип транспорта.</span><span class="sxs-lookup"><span data-stu-id="e4705-111">Specifies the transport type.</span></span> <span data-ttu-id="e4705-112">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e4705-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="e4705-113">0</span><span class="sxs-lookup"><span data-stu-id="e4705-113">0</span></span>
</dt> <dd>

<span data-ttu-id="e4705-114">Транспорт RPC через HTTP.</span><span class="sxs-lookup"><span data-stu-id="e4705-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="e4705-115">1</span><span class="sxs-lookup"><span data-stu-id="e4705-115">1</span></span>
</dt> <dd>

<span data-ttu-id="e4705-116">Транспорт HTTP.</span><span class="sxs-lookup"><span data-stu-id="e4705-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="e4705-117">2</span><span class="sxs-lookup"><span data-stu-id="e4705-117">2</span></span>
</dt> <dd>

<span data-ttu-id="e4705-118">Транспорт UDP.</span><span class="sxs-lookup"><span data-stu-id="e4705-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e4705-119">*Включено* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e4705-119">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4705-120">**Логическое** значение, указывающее, включен ли транспорт.</span><span class="sxs-lookup"><span data-stu-id="e4705-120">A **boolean** value that indicates whether the transport is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4705-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4705-121">Return value</span></span>

<span data-ttu-id="e4705-122">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e4705-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e4705-123">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e4705-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e4705-124">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4705-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4705-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e4705-125">Requirements</span></span>



| <span data-ttu-id="e4705-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e4705-126">Requirement</span></span> | <span data-ttu-id="e4705-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e4705-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4705-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4705-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e4705-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e4705-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e4705-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4705-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e4705-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4705-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="e4705-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e4705-132">Namespace</span></span><br/>                | <span data-ttu-id="e4705-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e4705-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e4705-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e4705-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4705-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4705-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4705-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e4705-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4705-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4705-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e4705-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4705-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4705-139">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="e4705-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





