---
title: Метод Сетвиртуализелупбаккаддрессесенаблед класса Win32_TSVirtualIP
description: Задает значение свойства Виртуализелупбаккаддрессесенаблед.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетвиртуализелупбаккаддрессесенаблед
- Службы удаленных рабочих столов метода Сетвиртуализелупбаккаддрессесенаблед, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Сетвиртуализелупбаккаддрессесенаблед
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672535"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="90a24-106">Метод Сетвиртуализелупбаккаддрессесенаблед \_ класса Win32 тсвиртуалип</span><span class="sxs-lookup"><span data-stu-id="90a24-106">SetVirtualizeLoopbackAddressesEnabled method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="90a24-107">Задает значение свойства **виртуализелупбаккаддрессесенаблед** .</span><span class="sxs-lookup"><span data-stu-id="90a24-107">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a24-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90a24-108">Syntax</span></span>


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="90a24-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="90a24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90a24-110">*Виртуализелупбаккаддрессесенаблед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="90a24-110">*VirtualizeLoopbackAddressesEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a24-111">Указывает, следует ли включить виртуализацию адресов замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="90a24-111">Specifies whether to enable loopback address virtualization.</span></span> <span data-ttu-id="90a24-112">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="90a24-112">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="90a24-113">0</span><span class="sxs-lookup"><span data-stu-id="90a24-113">0</span></span>
</dt> <dd>

<span data-ttu-id="90a24-114">Не включайте петлевой адрес виртуализации.</span><span class="sxs-lookup"><span data-stu-id="90a24-114">Do not enable loopback address virtualization.</span></span>

</dd> <dt>

<span data-ttu-id="90a24-115">1</span><span class="sxs-lookup"><span data-stu-id="90a24-115">1</span></span>
</dt> <dd>

<span data-ttu-id="90a24-116">Включить виртуализацию адресов замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="90a24-116">Enable loopback address virtualization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90a24-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90a24-117">Return value</span></span>

<span data-ttu-id="90a24-118">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="90a24-118">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="90a24-119">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="90a24-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="90a24-120">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="90a24-120">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a24-121">Требования</span><span class="sxs-lookup"><span data-stu-id="90a24-121">Requirements</span></span>



| <span data-ttu-id="90a24-122">Требование</span><span class="sxs-lookup"><span data-stu-id="90a24-122">Requirement</span></span> | <span data-ttu-id="90a24-123">Значение</span><span class="sxs-lookup"><span data-stu-id="90a24-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90a24-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90a24-124">Minimum supported client</span></span><br/> | <span data-ttu-id="90a24-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="90a24-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="90a24-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90a24-126">Minimum supported server</span></span><br/> | <span data-ttu-id="90a24-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90a24-127">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="90a24-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="90a24-128">Namespace</span></span><br/>                | <span data-ttu-id="90a24-129">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="90a24-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="90a24-130">MOF</span><span class="sxs-lookup"><span data-stu-id="90a24-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90a24-131"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90a24-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="90a24-132">DLL</span><span class="sxs-lookup"><span data-stu-id="90a24-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90a24-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90a24-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90a24-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90a24-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a24-135">**\_Тсвиртуалип Win32**</span><span class="sxs-lookup"><span data-stu-id="90a24-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





