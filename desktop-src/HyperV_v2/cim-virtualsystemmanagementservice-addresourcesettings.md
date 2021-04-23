---
description: Добавляет ресурсы в конфигурацию виртуальной системы.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Метод Аддресаурцесеттингс класса CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683247"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="d28c9-103">Метод Аддресаурцесеттингс \_ класса CIM виртуалсистемманажементсервице</span><span class="sxs-lookup"><span data-stu-id="d28c9-103">AddResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d28c9-104">Добавляет ресурсы в конфигурацию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="d28c9-104">Adds resources to a virtual system configuration.</span></span>

<span data-ttu-id="d28c9-105">При применении к конфигурации виртуальной системы "State" ресурсы побочных эффектов добавляются в активную виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="d28c9-105">When applied to a "state" virtual system configuration, as a side effect resources are added to the active virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d28c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d28c9-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d28c9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d28c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d28c9-108">*Аффектедконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d28c9-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d28c9-109">Ссылка [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) на затронутую конфигурацию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="d28c9-109">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="d28c9-110">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d28c9-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d28c9-111">Массив строк, каждый из которых содержит один внедренный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , описывающий виртуальные аспекты виртуального ресурса, добавляемого в виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="d28c9-111">Array of strings each containing one embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be added to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="d28c9-112">*Ресултингресаурцесеттингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d28c9-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d28c9-113">Массив ссылок на экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющие виртуальные аспекты добавленных виртуальных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d28c9-113">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="d28c9-114">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d28c9-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d28c9-115">Если операция выполняется долго, при необходимости может быть возвращено задание.</span><span class="sxs-lookup"><span data-stu-id="d28c9-115">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="d28c9-116">В этом случае экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющие добавленные параметры ресурсов, доступны через ассоциацию **CIM \_ конретекомпонент** от экземпляра класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющего затронутую конфигурацию виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="d28c9-116">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the added resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d28c9-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d28c9-117">Return value</span></span>

<span data-ttu-id="d28c9-118">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="d28c9-118">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d28c9-119">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="d28c9-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d28c9-120">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="d28c9-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d28c9-121">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="d28c9-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d28c9-122">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="d28c9-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d28c9-123">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="d28c9-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d28c9-124">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="d28c9-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d28c9-125">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="d28c9-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d28c9-126">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d28c9-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d28c9-127">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="d28c9-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d28c9-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d28c9-128">Requirements</span></span>



| <span data-ttu-id="d28c9-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d28c9-129">Requirement</span></span> | <span data-ttu-id="d28c9-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d28c9-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d28c9-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d28c9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d28c9-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d28c9-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d28c9-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d28c9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d28c9-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d28c9-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d28c9-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d28c9-135">Namespace</span></span><br/>                | <span data-ttu-id="d28c9-136">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d28c9-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d28c9-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d28c9-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d28c9-138"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d28c9-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d28c9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d28c9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d28c9-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d28c9-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d28c9-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d28c9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d28c9-142">**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="d28c9-142">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




