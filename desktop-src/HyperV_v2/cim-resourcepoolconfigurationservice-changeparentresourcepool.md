---
description: Запуск задания для изменения родительского пула с указанными параметрами выделения.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Метод Чанжепарентресаурцепул класса CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682814"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="3fe7d-103">Метод Чанжепарентресаурцепул \_ класса CIM ресаурцепулконфигуратионсервице</span><span class="sxs-lookup"><span data-stu-id="3fe7d-103">ChangeParentResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="3fe7d-104">Запуск задания для изменения родительского пула с указанными параметрами выделения.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-104">Start a job to change a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fe7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fe7d-105">Syntax</span></span>


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="3fe7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fe7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fe7d-107">*Чилдпул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3fe7d-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe7d-108">[**\_ ResourcePool CIM**](cim-resourcepool.md) , который ссылается на дочерний пул.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-108">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="3fe7d-109">*Парентпул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3fe7d-109">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe7d-110">Массив [**CIM \_ ResourcePool**](cim-resourcepool.md) , который ссылается на родительские пулы.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) array that references the parent pool(s).</span></span>

</dd> <dt>

<span data-ttu-id="3fe7d-111">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3fe7d-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe7d-112">Необязательная строка, содержащая представление [**экземпляра \_ CIM**](cim-settingdata.md) типа "Категория", которое используется для указания параметров родительского пула.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-112">Optional string containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the parent pool.</span></span>

</dd> <dt>

<span data-ttu-id="3fe7d-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3fe7d-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fe7d-114">[**\_ Конкретежоб CIM**](cim-concretejob.md) , который ссылается на задание (может иметь **значение NULL** , если задание завершено).</span><span class="sxs-lookup"><span data-stu-id="3fe7d-114">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fe7d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3fe7d-115">Return value</span></span>

<span data-ttu-id="3fe7d-116">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3fe7d-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="3fe7d-117">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-118">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-119">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-119">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-120">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-121">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-121">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-122">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-122">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-123">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-123">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-124">**Неверный ResourceType для пула** (7)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-124">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-125">**Недостаточно ресурсов** (8)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-125">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-126">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-127">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-128">**Размер не поддерживается** (4097)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-128">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-129">**Метод зарезервирован** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-129">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3fe7d-130">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="3fe7d-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3fe7d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="3fe7d-131">Requirements</span></span>



| <span data-ttu-id="3fe7d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="3fe7d-132">Requirement</span></span> | <span data-ttu-id="3fe7d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="3fe7d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe7d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fe7d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3fe7d-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3fe7d-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="3fe7d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fe7d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3fe7d-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3fe7d-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="3fe7d-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3fe7d-138">Namespace</span></span><br/>                | <span data-ttu-id="3fe7d-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3fe7d-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3fe7d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3fe7d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fe7d-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fe7d-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fe7d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3fe7d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fe7d-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fe7d-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fe7d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fe7d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fe7d-145">**\_РЕСАУРЦЕПУЛКОНФИГУРАТИОНСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe7d-145">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




