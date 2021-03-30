---
title: Метод Рдвмигратевмтодифференсост класса Win32_RdvhManagement
description: Инициирует динамическую миграцию виртуальной машины на указанный узел.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рдвмигратевмтодифференсост
- Службы удаленных рабочих столов метода Рдвмигратевмтодифференсост, класс Win32_RdvhManagement
- Класс Win32_RdvhManagement службы удаленных рабочих столов, метод Рдвмигратевмтодифференсост
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3def1be6332397fb3830ffe8c90f324afc9f1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802272"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="28ea2-106">Метод Рдвмигратевмтодифференсост \_ класса Win32 рдвхманажемент</span><span class="sxs-lookup"><span data-stu-id="28ea2-106">RdvMigrateVmToDifferentHost method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="28ea2-107">Инициирует динамическую миграцию виртуальной машины на указанный узел.</span><span class="sxs-lookup"><span data-stu-id="28ea2-107">Initiates a live migration of a virtual machine to a specified host.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ea2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28ea2-108">Syntax</span></span>


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a><span data-ttu-id="28ea2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="28ea2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ea2-110">*VmName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28ea2-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ea2-111">Имя виртуальной машины для миграции.</span><span class="sxs-lookup"><span data-stu-id="28ea2-111">Name of the virtual machine to migrate.</span></span>

</dd> <dt>

<span data-ttu-id="28ea2-112">*Дестинатионхост* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28ea2-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ea2-113">имя узла назначения.</span><span class="sxs-lookup"><span data-stu-id="28ea2-113">name of the destination host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28ea2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28ea2-114">Return value</span></span>

<span data-ttu-id="28ea2-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="28ea2-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="28ea2-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="28ea2-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ea2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="28ea2-117">Requirements</span></span>



| <span data-ttu-id="28ea2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="28ea2-118">Requirement</span></span> | <span data-ttu-id="28ea2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="28ea2-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="28ea2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28ea2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28ea2-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="28ea2-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="28ea2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28ea2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28ea2-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28ea2-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="28ea2-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="28ea2-124">Namespace</span></span><br/>                | <span data-ttu-id="28ea2-125">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="28ea2-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="28ea2-126">MOF</span><span class="sxs-lookup"><span data-stu-id="28ea2-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28ea2-127"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28ea2-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="28ea2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="28ea2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28ea2-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28ea2-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ea2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28ea2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ea2-131">**\_Рдвхманажемент Win32**</span><span class="sxs-lookup"><span data-stu-id="28ea2-131">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





