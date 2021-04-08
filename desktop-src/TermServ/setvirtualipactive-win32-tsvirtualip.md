---
title: Метод Сетвиртуалипактиве класса Win32_TSVirtualIP
description: Задает значение свойства Виртуалипактиве.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетвиртуалипактиве
- Службы удаленных рабочих столов метода Сетвиртуалипактиве, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Сетвиртуалипактиве
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988851"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="06c8a-106">Метод Сетвиртуалипактиве \_ класса Win32 тсвиртуалип</span><span class="sxs-lookup"><span data-stu-id="06c8a-106">SetVirtualIPActive method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="06c8a-107">Задает значение свойства **виртуалипактиве** .</span><span class="sxs-lookup"><span data-stu-id="06c8a-107">Sets the **VirtualIPActive** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c8a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06c8a-108">Syntax</span></span>


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a><span data-ttu-id="06c8a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="06c8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c8a-110">*Виртуалипактиве* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06c8a-110">*VirtualIPActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06c8a-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06c8a-111">Type: **uint32**</span></span>

<span data-ttu-id="06c8a-112">Указывает, активна ли на сервере виртуализация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="06c8a-112">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="06c8a-113">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="06c8a-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="06c8a-114">нуль</span><span class="sxs-lookup"><span data-stu-id="06c8a-114">zero</span></span>
</dt> <dd>

<span data-ttu-id="06c8a-115">Виртуализация IP-адресов неактивна.</span><span class="sxs-lookup"><span data-stu-id="06c8a-115">IP virtualization is not active.</span></span>

</dd> <dt>

<span data-ttu-id="06c8a-116">отличные</span><span class="sxs-lookup"><span data-stu-id="06c8a-116">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="06c8a-117">Виртуализация IP-адресов активна.</span><span class="sxs-lookup"><span data-stu-id="06c8a-117">IP virtualization is active.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c8a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06c8a-118">Return value</span></span>

<span data-ttu-id="06c8a-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06c8a-119">Type: **uint32**</span></span>

<span data-ttu-id="06c8a-120">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="06c8a-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="06c8a-121">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="06c8a-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="06c8a-122">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="06c8a-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c8a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="06c8a-123">Requirements</span></span>



| <span data-ttu-id="06c8a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="06c8a-124">Requirement</span></span> | <span data-ttu-id="06c8a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="06c8a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06c8a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06c8a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06c8a-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="06c8a-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="06c8a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06c8a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06c8a-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="06c8a-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="06c8a-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="06c8a-130">Namespace</span></span><br/>                | <span data-ttu-id="06c8a-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="06c8a-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="06c8a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="06c8a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06c8a-133"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06c8a-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="06c8a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="06c8a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06c8a-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06c8a-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c8a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06c8a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c8a-137">**\_Тсвиртуалип Win32**</span><span class="sxs-lookup"><span data-stu-id="06c8a-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





