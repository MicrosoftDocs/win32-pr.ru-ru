---
description: Запускает задание по добавлению ресурсов в пул ресурсов.
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: Метод Аддресаурцесторесаурцепул класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.AddResourcesToResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d3aed59267bd064e95b62431064fbd54bb9168aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682815"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="51382-103">Метод Аддресаурцесторесаурцепул \_ класса CIM ресаурцепулконфигуратионсервице</span><span class="sxs-lookup"><span data-stu-id="51382-103">AddResourcesToResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="51382-104">Запускает задание по добавлению ресурсов в пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51382-104">Starts a job to add resources to a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="51382-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51382-105">Syntax</span></span>


```mof
uint32 AddResourcesToResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="51382-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51382-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51382-107">*Хостресаурцес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51382-107">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51382-108">Массив экземпляров [**CIM \_**](cim-logicaldevice.md) , добавляемых в пул.</span><span class="sxs-lookup"><span data-stu-id="51382-108">Array of [**CIM\_LogicalDevice**](cim-logicaldevice.md) instances to add to the pool.</span></span>

</dd> <dt>

<span data-ttu-id="51382-109">*Пул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51382-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51382-110">[**\_ ResourcePool CIM**](cim-resourcepool.md) , представляющий пул, в который добавляются ресурсы.</span><span class="sxs-lookup"><span data-stu-id="51382-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that represents the pool to add the resources to.</span></span>

</dd> <dt>

<span data-ttu-id="51382-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="51382-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51382-112">[**\_ Конкретежоб CIM**](cim-concretejob.md) , который ссылается на задание (может иметь **значение NULL** , если задание завершено).</span><span class="sxs-lookup"><span data-stu-id="51382-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51382-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51382-113">Return value</span></span>

<span data-ttu-id="51382-114">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="51382-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="51382-115">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="51382-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="51382-116">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="51382-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="51382-117">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="51382-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="51382-118">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="51382-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="51382-119">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="51382-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="51382-120">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="51382-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="51382-121">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="51382-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="51382-122">**Неверный ResourceType для пула** (7)</span><span class="sxs-lookup"><span data-stu-id="51382-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="51382-123">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="51382-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="51382-124">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="51382-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="51382-125">**Размер не поддерживается** (4097)</span><span class="sxs-lookup"><span data-stu-id="51382-125">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="51382-126">**Метод зарезервирован** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="51382-126">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="51382-127">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="51382-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="51382-128">Требования</span><span class="sxs-lookup"><span data-stu-id="51382-128">Requirements</span></span>



| <span data-ttu-id="51382-129">Требование</span><span class="sxs-lookup"><span data-stu-id="51382-129">Requirement</span></span> | <span data-ttu-id="51382-130">Значение</span><span class="sxs-lookup"><span data-stu-id="51382-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51382-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51382-131">Minimum supported client</span></span><br/> | <span data-ttu-id="51382-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="51382-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="51382-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51382-133">Minimum supported server</span></span><br/> | <span data-ttu-id="51382-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="51382-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="51382-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="51382-135">Namespace</span></span><br/>                | <span data-ttu-id="51382-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="51382-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="51382-137">MOF</span><span class="sxs-lookup"><span data-stu-id="51382-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51382-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51382-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51382-139">DLL</span><span class="sxs-lookup"><span data-stu-id="51382-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51382-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51382-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="51382-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51382-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51382-142">**\_РЕСАУРЦЕПУЛКОНФИГУРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="51382-142">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




