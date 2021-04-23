---
title: Метод СетлоадбаланЦингстате класса Win32_TSSessionDirectory
description: Задает значение, указывающее, будет ли сервер участвовать в балансировке нагрузки подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода СетлоадбаланЦингстате
- Службы удаленных рабочих столов метода СетлоадбаланЦингстате, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод СетлоадбаланЦингстате
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681826"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="a7573-106">Метод СетлоадбаланЦингстате \_ класса Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="a7573-106">SetLoadBalancingState method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="a7573-107">Задает значение, указывающее, будет ли сервер участвовать в балансировке нагрузки подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="a7573-107">Sets the value to indicate whether the server will participate in Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7573-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7573-108">Syntax</span></span>


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a><span data-ttu-id="a7573-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7573-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7573-110">*Статевалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7573-110">*StateValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7573-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a7573-111">Type: **uint32**</span></span>

<span data-ttu-id="a7573-112">Указывает, будет ли сервер участвовать в балансировке нагрузки RDCB.</span><span class="sxs-lookup"><span data-stu-id="a7573-112">Indicates whether the server will participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="a7573-113">0</span><span class="sxs-lookup"><span data-stu-id="a7573-113">0</span></span>
</dt> <dd>

<span data-ttu-id="a7573-114">Сервер не будет участвовать в балансировке нагрузки RDCB.</span><span class="sxs-lookup"><span data-stu-id="a7573-114">The server will not participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="a7573-115">1</span><span class="sxs-lookup"><span data-stu-id="a7573-115">1</span></span>
</dt> <dd>

<span data-ttu-id="a7573-116">Сервер будет участвовать в балансировке нагрузки RDCB.</span><span class="sxs-lookup"><span data-stu-id="a7573-116">The server will participate in RD Connection Broker load balancing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7573-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a7573-117">Remarks</span></span>

<span data-ttu-id="a7573-118">Сервер должен быть присоединен к ферме в RDCB.</span><span class="sxs-lookup"><span data-stu-id="a7573-118">The server must be joined to a farm in RD Connection Broker.</span></span>

<span data-ttu-id="a7573-119">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="a7573-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a7573-120">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="a7573-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a7573-121">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="a7573-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a7573-122">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a7573-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7573-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a7573-123">Requirements</span></span>



| <span data-ttu-id="a7573-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a7573-124">Requirement</span></span> | <span data-ttu-id="a7573-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a7573-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7573-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7573-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a7573-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a7573-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a7573-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7573-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a7573-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7573-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7573-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a7573-130">Namespace</span></span><br/>                | <span data-ttu-id="a7573-131">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a7573-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a7573-132">MOF</span><span class="sxs-lookup"><span data-stu-id="a7573-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7573-133"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7573-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7573-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a7573-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7573-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7573-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7573-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7573-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7573-137">**\_Тссессиондиректори Win32**</span><span class="sxs-lookup"><span data-stu-id="a7573-137">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

