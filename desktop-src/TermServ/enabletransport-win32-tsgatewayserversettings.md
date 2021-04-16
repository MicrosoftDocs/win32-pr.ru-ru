---
title: Метод Енаблетранспорт класса Win32_TSGatewayServerSettings
description: Включает или отключает указанный транспорт.
ms.assetid: 95c599d7-56c3-462a-9c7d-2ecf8fc55da1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Енаблетранспорт
- Службы удаленных рабочих столов метода Енаблетранспорт, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Енаблетранспорт
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableTransport
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a14e7ee94eb02e1358d66b9965ecc2323d5b773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672920"
---
# <a name="enabletransport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="fce46-106">Метод Енаблетранспорт \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="fce46-106">EnableTransport method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="fce46-107">Включает или отключает указанный транспорт.</span><span class="sxs-lookup"><span data-stu-id="fce46-107">Enables or disables the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce46-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fce46-108">Syntax</span></span>


```mof
uint32 EnableTransport(
  [in] uint16  TransportType,
  [in] boolean Enable
);
```



## <a name="parameters"></a><span data-ttu-id="fce46-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fce46-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce46-110">*TransportType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fce46-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fce46-111">Указывает тип транспорта.</span><span class="sxs-lookup"><span data-stu-id="fce46-111">Specifies the transport type.</span></span> <span data-ttu-id="fce46-112">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fce46-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="fce46-113">0</span><span class="sxs-lookup"><span data-stu-id="fce46-113">0</span></span>
</dt> <dd>

<span data-ttu-id="fce46-114">Транспорт RPC через HTTP.</span><span class="sxs-lookup"><span data-stu-id="fce46-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="fce46-115">1</span><span class="sxs-lookup"><span data-stu-id="fce46-115">1</span></span>
</dt> <dd>

<span data-ttu-id="fce46-116">Транспорт HTTP.</span><span class="sxs-lookup"><span data-stu-id="fce46-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="fce46-117">2</span><span class="sxs-lookup"><span data-stu-id="fce46-117">2</span></span>
</dt> <dd>

<span data-ttu-id="fce46-118">Транспорт UDP.</span><span class="sxs-lookup"><span data-stu-id="fce46-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fce46-119">*Включить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fce46-119">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fce46-120">Указывает, включен или отключен транспорт.</span><span class="sxs-lookup"><span data-stu-id="fce46-120">Specifies if the transport is enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce46-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fce46-121">Return value</span></span>

<span data-ttu-id="fce46-122">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="fce46-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fce46-123">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="fce46-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fce46-124">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fce46-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fce46-125">Требования</span><span class="sxs-lookup"><span data-stu-id="fce46-125">Requirements</span></span>



| <span data-ttu-id="fce46-126">Требование</span><span class="sxs-lookup"><span data-stu-id="fce46-126">Requirement</span></span> | <span data-ttu-id="fce46-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fce46-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fce46-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fce46-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fce46-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fce46-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fce46-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fce46-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fce46-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fce46-131">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="fce46-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fce46-132">Namespace</span></span><br/>                | <span data-ttu-id="fce46-133">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="fce46-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fce46-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fce46-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fce46-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fce46-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fce46-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fce46-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fce46-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fce46-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fce46-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fce46-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce46-139">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="fce46-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





