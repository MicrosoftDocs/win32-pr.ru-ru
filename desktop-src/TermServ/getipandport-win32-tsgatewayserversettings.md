---
title: Метод Жетипандпорт класса Win32_TSGatewayServerSettings
description: Получает IP-адрес прослушивания и номер порта для указанного транспорта.
ms.assetid: e12451c3-2641-49e1-bd35-f7cab37865ae
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетипандпорт
- Службы удаленных рабочих столов метода Жетипандпорт, класс Win32_TSGatewayServerSettings
- Класс Win32_TSGatewayServerSettings службы удаленных рабочих столов, метод Жетипандпорт
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetIPAndPort
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260cc45961720ae8d175d4df3e84edc7a0c15c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340460"
---
# <a name="getipandport-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="3654a-106">Метод Жетипандпорт \_ класса Win32 тсгатевайсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="3654a-106">GetIPAndPort method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="3654a-107">Получает IP-адрес прослушивания и номер порта для указанного транспорта.</span><span class="sxs-lookup"><span data-stu-id="3654a-107">Obtains the listening IP address and port number for the specified transport.</span></span>

## <a name="syntax"></a><span data-ttu-id="3654a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3654a-108">Syntax</span></span>


```mof
uint32 GetIPAndPort(
  [in]  uint16 TransportType,
  [out] string IPAddress,
  [out] uint16 Port
);
```



## <a name="parameters"></a><span data-ttu-id="3654a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3654a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3654a-110">*TransportType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3654a-110">*TransportType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3654a-111">Указывает тип транспорта.</span><span class="sxs-lookup"><span data-stu-id="3654a-111">Specifies the transport type.</span></span> <span data-ttu-id="3654a-112">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3654a-112">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="3654a-113">0</span><span class="sxs-lookup"><span data-stu-id="3654a-113">0</span></span>
</dt> <dd>

<span data-ttu-id="3654a-114">Транспорт RPC через HTTP.</span><span class="sxs-lookup"><span data-stu-id="3654a-114">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="3654a-115">1</span><span class="sxs-lookup"><span data-stu-id="3654a-115">1</span></span>
</dt> <dd>

<span data-ttu-id="3654a-116">Транспорт HTTP.</span><span class="sxs-lookup"><span data-stu-id="3654a-116">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="3654a-117">2</span><span class="sxs-lookup"><span data-stu-id="3654a-117">2</span></span>
</dt> <dd>

<span data-ttu-id="3654a-118">Транспорт UDP.</span><span class="sxs-lookup"><span data-stu-id="3654a-118">UDP transport.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3654a-119">*IP-адрес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3654a-119">*IPAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3654a-120">Строка, которая получает IP-адрес прослушивания в виде октета (например, "192.168.1.1").</span><span class="sxs-lookup"><span data-stu-id="3654a-120">A string that receives the listening IP address, in octet form (for example, "192.168.1.1").</span></span>

</dd> <dt>

<span data-ttu-id="3654a-121">*Порт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3654a-121">*Port* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3654a-122">Указывает номер прослушивающего порта.</span><span class="sxs-lookup"><span data-stu-id="3654a-122">Specifies the listening port number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3654a-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3654a-123">Return value</span></span>

<span data-ttu-id="3654a-124">Если метод завершается с ошибкой, он возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3654a-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3654a-125">Если метод завершился неудачно, он возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3654a-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3654a-126">Список кодов ошибок см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3654a-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3654a-127">Требования</span><span class="sxs-lookup"><span data-stu-id="3654a-127">Requirements</span></span>



| <span data-ttu-id="3654a-128">Требование</span><span class="sxs-lookup"><span data-stu-id="3654a-128">Requirement</span></span> | <span data-ttu-id="3654a-129">Значение</span><span class="sxs-lookup"><span data-stu-id="3654a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3654a-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3654a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3654a-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3654a-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3654a-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3654a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3654a-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3654a-133">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="3654a-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3654a-134">Namespace</span></span><br/>                | <span data-ttu-id="3654a-135">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="3654a-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3654a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="3654a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3654a-137"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3654a-137"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3654a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3654a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3654a-139"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3654a-139"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3654a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3654a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3654a-141">**\_Тсгатевайсерверсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="3654a-141">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





