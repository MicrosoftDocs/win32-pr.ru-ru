---
title: Метод Сетипандпорт класса Win32_TSGatewayServerSettings
description: Задает IP-адрес прослушивания и номер порта для указанного транспорта.
ms.assetid: f46f4660-31ce-4513-b93d-acd50b42ae0a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетипандпорт
- Службы удаленных рабочих столов метода Сетипандпорт, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Сетипандпорт
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88870cce628a94ca34b38ccf315edc87a1a734b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534073"
---
# <a name="setipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="e44f0-106">Метод Сетипандпорт \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="e44f0-106">SetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="e44f0-107">Задает IP-адрес прослушивания и номер порта для указанного транспорта.</span><span class="sxs-lookup"><span data-stu-id="e44f0-107">Sets the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44f0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e44f0-108">Syntax</span></span>


```mof
uint32 SetIPAndPort(
  [in] uint16  TransportType,
  [in] string  IPAddress,
  [in] uint16  Port,
  [in] boolean OverrideExisting
);
```



## <a name="parameters"></a><span data-ttu-id="e44f0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e44f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e44f0-110">*TransportType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44f0-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44f0-111">Указывает тип транспорта.</span><span class="sxs-lookup"><span data-stu-id="e44f0-111">Specifies the transport type.</span></span> <span data-ttu-id="e44f0-112">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e44f0-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="e44f0-113">0</span><span class="sxs-lookup"><span data-stu-id="e44f0-113">0</span></span>
</dt> <dd>

<span data-ttu-id="e44f0-114">Транспорт RPC через HTTP.</span><span class="sxs-lookup"><span data-stu-id="e44f0-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="e44f0-115">1</span><span class="sxs-lookup"><span data-stu-id="e44f0-115">1</span></span>
</dt> <dd>

<span data-ttu-id="e44f0-116">Транспорт HTTP.</span><span class="sxs-lookup"><span data-stu-id="e44f0-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="e44f0-117">2</span><span class="sxs-lookup"><span data-stu-id="e44f0-117">2</span></span>
</dt> <dd>

<span data-ttu-id="e44f0-118">Транспорт UDP.</span><span class="sxs-lookup"><span data-stu-id="e44f0-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e44f0-119">*IP-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44f0-119">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44f0-120">Указывает IP-адрес прослушивания в виде октета (например, "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="e44f0-120">Specifies the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="e44f0-121">*Порт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44f0-121">*Port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44f0-122">Указывает номер прослушивающего порта.</span><span class="sxs-lookup"><span data-stu-id="e44f0-122">Specifies the listening port number.</span></span>

</dd> <dt>

<span data-ttu-id="e44f0-123">*Оверридиксистинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e44f0-123">*OverrideExisting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e44f0-124">Указывает, переопределять ли существующую привязку IP/Port для HTTP.</span><span class="sxs-lookup"><span data-stu-id="e44f0-124">Indicates whether to override the existing IP/Port binding for HTTP.</span></span> <span data-ttu-id="e44f0-125">Этот параметр используется только в том случае, если параметр *TransportType* содержит значение 0 (RPC по HTTP) или 1 (http).</span><span class="sxs-lookup"><span data-stu-id="e44f0-125">This parameter is only used if the *TransportType* parameter contains 0 (RPC over HTTP) or 1 (HTTP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e44f0-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e44f0-126">Return value</span></span>

<span data-ttu-id="e44f0-127">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e44f0-127">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e44f0-128">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e44f0-128">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e44f0-129">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e44f0-129">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e44f0-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e44f0-130">Requirements</span></span>



| <span data-ttu-id="e44f0-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e44f0-131">Requirement</span></span> | <span data-ttu-id="e44f0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e44f0-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e44f0-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e44f0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e44f0-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e44f0-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e44f0-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e44f0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e44f0-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e44f0-136">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="e44f0-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e44f0-137">Namespace</span></span><br/>                | <span data-ttu-id="e44f0-138">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e44f0-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e44f0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e44f0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e44f0-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e44f0-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e44f0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e44f0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e44f0-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e44f0-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e44f0-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e44f0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e44f0-144">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="e44f0-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





