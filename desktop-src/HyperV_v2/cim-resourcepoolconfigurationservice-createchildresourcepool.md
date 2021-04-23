---
description: Запуск задания для создания подпула из родительского пула с указанными параметрами выделения.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Метод Креатечилдресаурцепул класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662476"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="d7b73-103">Метод Креатечилдресаурцепул \_ класса CIM ресаурцепулконфигуратионсервице</span><span class="sxs-lookup"><span data-stu-id="d7b73-103">CreateChildResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="d7b73-104">Запуск задания для создания подпула из родительского пула с указанными параметрами выделения.</span><span class="sxs-lookup"><span data-stu-id="d7b73-104">Start a job to create a sub-pool from a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7b73-105">Syntax</span></span>


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d7b73-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7b73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b73-107">*ElementName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7b73-107">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7b73-108">Имя, соответствующее конечному пользователю для создаваемого пула.</span><span class="sxs-lookup"><span data-stu-id="d7b73-108">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="d7b73-109">Если **значение равно NULL**, можно использовать имя по умолчанию, предоставляемое системой.</span><span class="sxs-lookup"><span data-stu-id="d7b73-109">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="d7b73-110">Значение будет храниться в свойстве **ElementName** для созданного элемента.</span><span class="sxs-lookup"><span data-stu-id="d7b73-110">The value will be stored in the **ElementName** property for the created element.</span></span>

</dd> <dt>

<span data-ttu-id="d7b73-111">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7b73-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7b73-112">Строка, содержащая представление экземпляра [**CIM типа \_**](cim-settingdata.md) "Категория", который используется для указания параметров дочернего пула.</span><span class="sxs-lookup"><span data-stu-id="d7b73-112">String containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the child Pool.</span></span>

</dd> <dt>

<span data-ttu-id="d7b73-113">*Парентпул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d7b73-113">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7b73-114">[**\_ ResourcePool CIM**](cim-resourcepool.md) , из которого создается новый пул.</span><span class="sxs-lookup"><span data-stu-id="d7b73-114">A [**CIM\_ResourcePool**](cim-resourcepool.md) from which to create the new Pool.</span></span>

</dd> <dt>

<span data-ttu-id="d7b73-115">*Пул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7b73-115">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7b73-116">[**\_ ResourcePool CIM**](cim-resourcepool.md) , который ссылается на полученный пул.</span><span class="sxs-lookup"><span data-stu-id="d7b73-116">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="d7b73-117">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d7b73-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7b73-118">Ссылка на задание (может иметь значение null, если задание завершено).</span><span class="sxs-lookup"><span data-stu-id="d7b73-118">Reference to the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7b73-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7b73-119">Return value</span></span>

<span data-ttu-id="d7b73-120">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d7b73-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d7b73-121">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d7b73-121">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-122">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="d7b73-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-123">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d7b73-123">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-124">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="d7b73-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-125">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="d7b73-125">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-126">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="d7b73-126">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-127">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="d7b73-127">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-128">**Неверный ResourceType для пула** (7)</span><span class="sxs-lookup"><span data-stu-id="d7b73-128">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-129">**Недостаточно ресурсов** (8)</span><span class="sxs-lookup"><span data-stu-id="d7b73-129">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-130">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d7b73-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-131">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d7b73-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-132">**Размер не поддерживается** (4097)</span><span class="sxs-lookup"><span data-stu-id="d7b73-132">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-133">**Метод зарезервирован** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d7b73-133">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d7b73-134">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="d7b73-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d7b73-135">Требования</span><span class="sxs-lookup"><span data-stu-id="d7b73-135">Requirements</span></span>



| <span data-ttu-id="d7b73-136">Требование</span><span class="sxs-lookup"><span data-stu-id="d7b73-136">Requirement</span></span> | <span data-ttu-id="d7b73-137">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b73-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b73-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7b73-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b73-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d7b73-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d7b73-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7b73-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b73-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d7b73-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d7b73-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d7b73-142">Namespace</span></span><br/>                | <span data-ttu-id="d7b73-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d7b73-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d7b73-144">MOF</span><span class="sxs-lookup"><span data-stu-id="d7b73-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7b73-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7b73-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7b73-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d7b73-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7b73-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d7b73-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d7b73-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7b73-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b73-149">**\_РЕСАУРЦЕПУЛКОНФИГУРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="d7b73-149">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




