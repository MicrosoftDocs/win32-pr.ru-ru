---
description: Определяет виртуальную систему.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Метод Дефинесистем класса CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683246"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="366a0-103">Метод Дефинесистем \_ класса CIM виртуалсистемманажементсервице</span><span class="sxs-lookup"><span data-stu-id="366a0-103">DefineSystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="366a0-104">Определяет виртуальную систему.</span><span class="sxs-lookup"><span data-stu-id="366a0-104">Defines a virtual system.</span></span>

<span data-ttu-id="366a0-105">Входные данные, которые указаны не полностью, могут быть заполнены значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="366a0-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="366a0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="366a0-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="366a0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="366a0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="366a0-108">*SystemSettings* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="366a0-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="366a0-109">Строка, содержащая внедренный экземпляр класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , который используется для определения атрибутов создаваемой виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="366a0-109">String containing an embedded instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to define attributes of the virtual system to be created.</span></span>

</dd> <dt>

<span data-ttu-id="366a0-110">*Ресаурцесеттингс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="366a0-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="366a0-111">Массив строк, содержащий встроенный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , который описывает виртуальные аспекты виртуального ресурса, создаваемого в области новой виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="366a0-111">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be created in the scope of the new virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="366a0-112">*Референцеконфигуратион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="366a0-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="366a0-113">Ссылка на экземпляр объекта [**CIM \_ виртуалсистемсеттингдат**](cim-virtualsystemsettingdata.md) , который является объектом верхнего уровня эталонной конфигурации виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="366a0-113">Reference to a [**CIM\_VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) object instance that is the top level object of a reference virtual system configuration.</span></span> <span data-ttu-id="366a0-114">Конфигурация ссылки используется для дополнения конфигурации новой виртуальной системы, если параметры *SystemSettings* и *ресаурцесеттингс* не предпредоставил соответствующие сведения.</span><span class="sxs-lookup"><span data-stu-id="366a0-114">The reference configuration is used to complement the configuration of the new virtual system if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="366a0-115">*Ресултингсистем* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="366a0-115">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="366a0-116">Если система виртуальных компьютеров успешно определена, возвращается ссылка на экземпляр класса [**CIM \_ ComputerSystem**](cim-computersystem.md) , представляющий только что определенную систему виртуальных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="366a0-116">If a virtual computer system is successfully defined, a reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the newly defined virtual computer system is returned.</span></span>

</dd> <dt>

<span data-ttu-id="366a0-117">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="366a0-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="366a0-118">Если операция выполняется долго, при необходимости может быть возвращено задание.</span><span class="sxs-lookup"><span data-stu-id="366a0-118">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="366a0-119">В этом случае экземпляр класса [**CIM \_ ComputerSystem**](cim-computersystem.md) , представляющий новую виртуальную систему, представлен через ассоциацию [**CIM \_ аффектеджобелемент**](cim-affectedjobelement.md) со свойством **аффектеделемент** , ссылающимся на новый экземпляр класса **CIM \_ ComputerSystem** , а свойство **елементеффектс** установлено в значение 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="366a0-119">In this case, the instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the new virtual system is presented via association [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) with the property **AffectedElement** referring to the new instance of class **CIM\_ComputerSystem** and property **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="366a0-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="366a0-120">Return value</span></span>

<span data-ttu-id="366a0-121">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="366a0-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="366a0-122">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="366a0-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="366a0-123">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="366a0-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="366a0-124">**Сбой** (2)</span><span class="sxs-lookup"><span data-stu-id="366a0-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="366a0-125">**Время ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="366a0-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="366a0-126">**Недопустимый параметр** (4)</span><span class="sxs-lookup"><span data-stu-id="366a0-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="366a0-127">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="366a0-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="366a0-128">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="366a0-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="366a0-129">**Метод зарезервирован** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="366a0-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="366a0-130">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="366a0-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="366a0-131">Требования</span><span class="sxs-lookup"><span data-stu-id="366a0-131">Requirements</span></span>



| <span data-ttu-id="366a0-132">Требование</span><span class="sxs-lookup"><span data-stu-id="366a0-132">Requirement</span></span> | <span data-ttu-id="366a0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="366a0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="366a0-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="366a0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="366a0-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="366a0-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="366a0-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="366a0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="366a0-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="366a0-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="366a0-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="366a0-138">Namespace</span></span><br/>                | <span data-ttu-id="366a0-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="366a0-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="366a0-140">MOF</span><span class="sxs-lookup"><span data-stu-id="366a0-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="366a0-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="366a0-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="366a0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="366a0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="366a0-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="366a0-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="366a0-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="366a0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="366a0-145">**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="366a0-145">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




