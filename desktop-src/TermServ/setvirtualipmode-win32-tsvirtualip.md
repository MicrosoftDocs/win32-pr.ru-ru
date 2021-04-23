---
title: Метод Сетвиртуалипмоде класса Win32_TSVirtualIP
description: Задает значение свойства Виртуалипмоде.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетвиртуалипмоде
- Службы удаленных рабочих столов метода Сетвиртуалипмоде, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Сетвиртуалипмоде
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681959"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="14c05-106">Метод Сетвиртуалипмоде \_ класса Win32 тсвиртуалип</span><span class="sxs-lookup"><span data-stu-id="14c05-106">SetVirtualIPMode method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="14c05-107">Задает значение свойства **виртуалипмоде** .</span><span class="sxs-lookup"><span data-stu-id="14c05-107">Sets the **VirtualIPMode** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c05-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14c05-108">Syntax</span></span>


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a><span data-ttu-id="14c05-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="14c05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c05-110">*Виртуалипмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14c05-110">*VirtualIPMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c05-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14c05-111">Type: **uint32**</span></span>

<span data-ttu-id="14c05-112">Указывает, какой режим виртуализации IP используется на сервере.</span><span class="sxs-lookup"><span data-stu-id="14c05-112">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="14c05-113">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="14c05-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="14c05-114">0</span><span class="sxs-lookup"><span data-stu-id="14c05-114">0</span></span>
</dt> <dd>

<span data-ttu-id="14c05-115">Режим виртуализации IP — для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="14c05-115">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span data-ttu-id="14c05-116">1</span><span class="sxs-lookup"><span data-stu-id="14c05-116">1</span></span>
</dt> <dd>

<span data-ttu-id="14c05-117">Режим виртуализации IP-адресов — "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="14c05-117">The IP virtualization mode is per-user.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c05-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14c05-118">Return value</span></span>

<span data-ttu-id="14c05-119">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="14c05-119">Type: **uint32**</span></span>

<span data-ttu-id="14c05-120">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="14c05-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="14c05-121">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="14c05-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="14c05-122">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="14c05-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c05-123">Требования</span><span class="sxs-lookup"><span data-stu-id="14c05-123">Requirements</span></span>



| <span data-ttu-id="14c05-124">Требование</span><span class="sxs-lookup"><span data-stu-id="14c05-124">Requirement</span></span> | <span data-ttu-id="14c05-125">Значение</span><span class="sxs-lookup"><span data-stu-id="14c05-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14c05-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14c05-126">Minimum supported client</span></span><br/> | <span data-ttu-id="14c05-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="14c05-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="14c05-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14c05-128">Minimum supported server</span></span><br/> | <span data-ttu-id="14c05-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14c05-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="14c05-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="14c05-130">Namespace</span></span><br/>                | <span data-ttu-id="14c05-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="14c05-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="14c05-132">MOF</span><span class="sxs-lookup"><span data-stu-id="14c05-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14c05-133"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14c05-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="14c05-134">DLL</span><span class="sxs-lookup"><span data-stu-id="14c05-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14c05-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14c05-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c05-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14c05-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c05-137">**\_Тсвиртуалип Win32**</span><span class="sxs-lookup"><span data-stu-id="14c05-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





