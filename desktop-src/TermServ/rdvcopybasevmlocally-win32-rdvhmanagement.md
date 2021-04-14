---
title: Метод Рдвкопибасевмлокалли класса Win32_RdvhManagement
description: Копирует локальную базовую виртуальную машину на указанный сервер узла виртуализации удаленных рабочих столов (RDV).
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рдвкопибасевмлокалли
- Службы удаленных рабочих столов метода Рдвкопибасевмлокалли, класс Win32_RdvhManagement
- Класс Win32_RdvhManagement службы удаленных рабочих столов, метод Рдвкопибасевмлокалли
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416045"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="64ca9-106">Метод Рдвкопибасевмлокалли \_ класса Win32 рдвхманажемент</span><span class="sxs-lookup"><span data-stu-id="64ca9-106">RdvCopyBaseVmLocally method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="64ca9-107">Копирует локальную базовую виртуальную машину на указанный сервер узла виртуализации удаленных рабочих столов (RDV).</span><span class="sxs-lookup"><span data-stu-id="64ca9-107">Copies a local base virtual machine to a specified remote desktop virtualization (RDV) host server.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ca9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64ca9-108">Syntax</span></span>


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a><span data-ttu-id="64ca9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="64ca9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64ca9-110">*Басевмлокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64ca9-110">*BaseVmLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64ca9-111">Расположение базовой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="64ca9-111">The base virtual machine location.</span></span>

</dd> <dt>

<span data-ttu-id="64ca9-112">*Фармнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64ca9-112">*FarmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64ca9-113">Имя фермы узлов, в которую производится копирование.</span><span class="sxs-lookup"><span data-stu-id="64ca9-113">The name of the host farm to copy to.</span></span>

</dd> <dt>

<span data-ttu-id="64ca9-114">*Голдкачелокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64ca9-114">*GoldCacheLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64ca9-115">Расположение кэша Gold.</span><span class="sxs-lookup"><span data-stu-id="64ca9-115">The gold cache location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64ca9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64ca9-116">Return value</span></span>

<span data-ttu-id="64ca9-117">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="64ca9-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="64ca9-118">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="64ca9-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="64ca9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="64ca9-119">Requirements</span></span>



| <span data-ttu-id="64ca9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="64ca9-120">Requirement</span></span> | <span data-ttu-id="64ca9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="64ca9-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="64ca9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64ca9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="64ca9-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="64ca9-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="64ca9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64ca9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="64ca9-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64ca9-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="64ca9-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="64ca9-126">Namespace</span></span><br/>                | <span data-ttu-id="64ca9-127">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="64ca9-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="64ca9-128">MOF</span><span class="sxs-lookup"><span data-stu-id="64ca9-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64ca9-129"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64ca9-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="64ca9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="64ca9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64ca9-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64ca9-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64ca9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64ca9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ca9-133">**\_Рдвхманажемент Win32**</span><span class="sxs-lookup"><span data-stu-id="64ca9-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





