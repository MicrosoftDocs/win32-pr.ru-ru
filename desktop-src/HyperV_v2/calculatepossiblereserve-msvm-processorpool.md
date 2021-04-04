---
description: Этот метод используется для поиска фактического резервирования с входным параметром, равным количеству процессоров виртуальной машины, для которых вычисляется резерв.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Метод Калкулатепоссиблересерве класса Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813856"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a><span data-ttu-id="6276e-103">Метод Калкулатепоссиблересерве \_ класса Процессорпул мсвм</span><span class="sxs-lookup"><span data-stu-id="6276e-103">CalculatePossibleReserve method of the Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="6276e-104">Этот метод используется для поиска фактического резервирования с входным параметром, равным количеству процессоров виртуальной машины, для которых вычисляется резерв.</span><span class="sxs-lookup"><span data-stu-id="6276e-104">This method is used to find the actual reserve with the input parameter being the number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="6276e-105">Этот метод необходим, поскольку резервирование ресурсов процессора сильно зависит от числа процессоров, которые должны быть запланированы параллельно.</span><span class="sxs-lookup"><span data-stu-id="6276e-105">This method is necessary because the reservation of processor resources is highly dependent on the number of processors which must be scheduled in parallel.</span></span>

## <a name="syntax"></a><span data-ttu-id="6276e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6276e-106">Syntax</span></span>


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a><span data-ttu-id="6276e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6276e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6276e-108">*ProcessorCount* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6276e-108">*ProcessorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6276e-109">Тип: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6276e-109">Type: **uint16**</span></span>

<span data-ttu-id="6276e-110">Число процессоров виртуальной машины, для которых вычисляется резерв.</span><span class="sxs-lookup"><span data-stu-id="6276e-110">The number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="6276e-111">Максимальное значение этого свойства — число логических процессоров для главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="6276e-111">The maximum value for this property is the logical processor count for the host computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6276e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6276e-112">Return value</span></span>

<span data-ttu-id="6276e-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6276e-113">Type: **uint32**</span></span>

<span data-ttu-id="6276e-114">Объем ресурсов ЦП, которые могут быть зарезервированы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6276e-114">The amount of CPU resources that may be reserved for a virtual machine.</span></span>

## <a name="remarks"></a><span data-ttu-id="6276e-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6276e-115">Remarks</span></span>

<span data-ttu-id="6276e-116">Доступ к классу [**\_ процессорпул мсвм**](msvm-processorpool.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="6276e-116">Access to the [**Msvm\_ProcessorPool**](msvm-processorpool.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6276e-117">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6276e-117">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6276e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6276e-118">Requirements</span></span>



| <span data-ttu-id="6276e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6276e-119">Requirement</span></span> | <span data-ttu-id="6276e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6276e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6276e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6276e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6276e-122">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6276e-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6276e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6276e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6276e-124">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6276e-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6276e-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6276e-125">Namespace</span></span><br/>                | <span data-ttu-id="6276e-126">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="6276e-126">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6276e-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6276e-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6276e-128"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6276e-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6276e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6276e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6276e-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6276e-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6276e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6276e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6276e-132">**Мсвм \_ процессорпул**</span><span class="sxs-lookup"><span data-stu-id="6276e-132">**Msvm\_ProcessorPool**</span></span>](msvm-processorpool.md)
</dt> </dl>

 

