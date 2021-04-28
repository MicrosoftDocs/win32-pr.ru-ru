---
description: Метод Ремовересаурцесеттингс класса CIM_VirtualSystemManagementService — удаляет параметры виртуального ресурса из конфигурации виртуальной системы.
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Метод Ремовересаурцесеттингс класса CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5c7daabcdcd732c3a5693664e1768ebf66668d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112262"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="0f3aa-103">Метод Ремовересаурцесеттингс \_ класса CIM виртуалсистемманажементсервице</span><span class="sxs-lookup"><span data-stu-id="0f3aa-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="0f3aa-104">Удаляет параметры виртуального ресурса из конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="0f3aa-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="0f3aa-105">При применении к частям "текущей" конфигурации виртуальной системы, так как ресурсы активной виртуальной системы могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="0f3aa-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3aa-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f3aa-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0f3aa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f3aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f3aa-108">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f3aa-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3aa-109">Массив ссылок на экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , где каждый экземпляр представляет параметры виртуального ресурса в конфигурации виртуальной системы, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="0f3aa-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="0f3aa-110">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0f3aa-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3aa-111">Если операция выполняется долго, может быть возвращена также [**\_ конкретежоб CIM**](cim-concretejob.md) , представляющая задание.</span><span class="sxs-lookup"><span data-stu-id="0f3aa-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f3aa-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f3aa-112">Return value</span></span>

<span data-ttu-id="0f3aa-113">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0f3aa-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0f3aa-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f3aa-115">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0f3aa-116">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0f3aa-117">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0f3aa-118">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0f3aa-119">**Недопустимое состояние** (5)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0f3aa-120">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0f3aa-121">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0f3aa-122">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0f3aa-123">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="0f3aa-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0f3aa-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0f3aa-124">Requirements</span></span>



| <span data-ttu-id="0f3aa-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0f3aa-125">Requirement</span></span> | <span data-ttu-id="0f3aa-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0f3aa-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3aa-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f3aa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3aa-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0f3aa-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0f3aa-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f3aa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3aa-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0f3aa-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0f3aa-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f3aa-131">Namespace</span></span><br/>                | <span data-ttu-id="0f3aa-132">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0f3aa-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0f3aa-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0f3aa-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f3aa-134"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f3aa-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f3aa-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0f3aa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f3aa-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f3aa-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f3aa-137">См. также</span><span class="sxs-lookup"><span data-stu-id="0f3aa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3aa-138">**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="0f3aa-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




