---
description: Изменяет параметры дочернего пула, не связанные с распределением.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Метод Модифипулсеттингс класса Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265664"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="9cc3f-103">Метод Модифипулсеттингс \_ класса Ресаурцепулконфигуратионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="9cc3f-103">ModifyPoolSettings method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="9cc3f-104">Изменяет параметры дочернего пула, не связанные с распределением.</span><span class="sxs-lookup"><span data-stu-id="9cc3f-104">Changes the settings of a child pool that are not allocation related.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc3f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cc3f-105">Syntax</span></span>


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9cc3f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cc3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc3f-107">*Чилдпул* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9cc3f-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc3f-108">Ссылка на экземпляр класса [**CIM \_ ResourcePool**](cim-resourcepool.md) , представляющий дочерний пул, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="9cc3f-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="9cc3f-109">*Пулсеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9cc3f-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc3f-110">Встроенный экземпляр класса [**мсвм \_ ресаурцепулсеттингдата**](msvm-resourcepoolsettingdata.md) , который используется для указания новых параметров пула.</span><span class="sxs-lookup"><span data-stu-id="9cc3f-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the new settings for the pool.</span></span>

</dd> <dt>

<span data-ttu-id="9cc3f-111">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9cc3f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc3f-112">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9cc3f-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc3f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9cc3f-113">Return value</span></span>

<span data-ttu-id="9cc3f-114">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9cc3f-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9cc3f-115">**Задание завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-116">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-117">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-118">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-119">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-120">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-121">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-122">**Неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-123">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-124">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-125">**Используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-126">**Недопустимое состояние** (32775)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-127">**Неверный тип ресурса для пула** (32776)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-128">**Недоступно** (32777)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-129">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-130">**Поставщик зарезервирован** (32779)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-131">**Недостаточно ресурсов** (32780)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-132">**Объект не найден** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-133">**Объект существует** (32788)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="9cc3f-134">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="9cc3f-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9cc3f-135">Требования</span><span class="sxs-lookup"><span data-stu-id="9cc3f-135">Requirements</span></span>



| <span data-ttu-id="9cc3f-136">Требование</span><span class="sxs-lookup"><span data-stu-id="9cc3f-136">Requirement</span></span> | <span data-ttu-id="9cc3f-137">Значение</span><span class="sxs-lookup"><span data-stu-id="9cc3f-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc3f-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cc3f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc3f-139">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9cc3f-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9cc3f-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cc3f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc3f-141">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9cc3f-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9cc3f-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9cc3f-142">Namespace</span></span><br/>                | <span data-ttu-id="9cc3f-143">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="9cc3f-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9cc3f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="9cc3f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cc3f-145"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cc3f-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cc3f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="9cc3f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cc3f-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9cc3f-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9cc3f-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cc3f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc3f-149">**Мсвм \_ ресаурцепулконфигуратионсервице**</span><span class="sxs-lookup"><span data-stu-id="9cc3f-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

