---
description: Метод Модифиресаурцесеттингс класса CIM_VirtualSystemManagementService изменяет параметры виртуального ресурса.
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Метод Модифиресаурцесеттингс класса CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26971c80ce6f7d0ffcdcef069d76aef5fdc15138
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112292"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="f5a40-103">Метод Модифиресаурцесеттингс \_ класса CIM виртуалсистемманажементсервице</span><span class="sxs-lookup"><span data-stu-id="f5a40-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f5a40-104">Изменяет параметры виртуального ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5a40-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="f5a40-105">При применении к частям "текущей" конфигурации виртуальной системы могут быть изменены ресурсы побочных эффектов активной виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f5a40-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a40-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5a40-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f5a40-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5a40-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a40-108">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5a40-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a40-109">Массив строк, содержащий встроенный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , который описывает изменения виртуальных аспектов существующего виртуального ресурса.</span><span class="sxs-lookup"><span data-stu-id="f5a40-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="f5a40-110">Для указания изменяемого параметра виртуального ресурса все экземпляры должны иметь допустимый идентификатор **InstanceId** .</span><span class="sxs-lookup"><span data-stu-id="f5a40-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="f5a40-111">*Ресултингресаурцесеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f5a40-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a40-112">Массив ссылок на экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющие виртуальные аспекты измененных виртуальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f5a40-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="f5a40-113">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f5a40-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a40-114">Если операция выполняется долго, при необходимости возвращается задание.</span><span class="sxs-lookup"><span data-stu-id="f5a40-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="f5a40-115">В этом случае экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющие измененные параметры ресурсов, доступны через ассоциацию **CIM \_ конретекомпонент** от экземпляра класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющего затронутую конфигурацию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f5a40-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a40-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5a40-116">Return value</span></span>

<span data-ttu-id="f5a40-117">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f5a40-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f5a40-118">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f5a40-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-119">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="f5a40-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-120">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="f5a40-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-121">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="f5a40-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-122">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="f5a40-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-123">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="f5a40-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-124">**Несовместимые параметры** (6)</span><span class="sxs-lookup"><span data-stu-id="f5a40-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-125">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="f5a40-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-126">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f5a40-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-127">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f5a40-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f5a40-128">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="f5a40-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f5a40-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f5a40-129">Requirements</span></span>



| <span data-ttu-id="f5a40-130">Требование</span><span class="sxs-lookup"><span data-stu-id="f5a40-130">Requirement</span></span> | <span data-ttu-id="f5a40-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f5a40-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a40-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5a40-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a40-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f5a40-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f5a40-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5a40-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a40-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f5a40-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f5a40-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f5a40-136">Namespace</span></span><br/>                | <span data-ttu-id="f5a40-137">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f5a40-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f5a40-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f5a40-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5a40-139"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5a40-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5a40-140">DLL</span><span class="sxs-lookup"><span data-stu-id="f5a40-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5a40-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f5a40-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f5a40-142">См. также</span><span class="sxs-lookup"><span data-stu-id="f5a40-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a40-143">**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="f5a40-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




