---
description: Проверяет, может ли физический корпус, на который указывает ссылка, находиться в физическом пакете или вставляться в него.
ms.assetid: 9a1aa1b7-2b95-4887-9d14-e416ff69f9df
ms.tgt_platform: multiple
title: Метод, совместимый с классом CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8796582b153a7283429715569eeed91e4dd38fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655773"
---
# <a name="iscompatible-method-of-the-cim_chassis-class"></a><span data-ttu-id="0abac-103">Метод, совместимый с \_ классом CIM Chassis</span><span class="sxs-lookup"><span data-stu-id="0abac-103">IsCompatible method of the CIM\_Chassis class</span></span>

<span data-ttu-id="0abac-104">Метод, **совместимый** с, позволяет проверить, может ли связанный физический корпус быть включен в физический пакет или вставляться в него.</span><span class="sxs-lookup"><span data-stu-id="0abac-104">The **IsCompatible** method verifies whether the referenced physical chassis can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="0abac-105">В подклассе набор возможных кодов возврата можно указать с помощью квалификатора [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) в методе.</span><span class="sxs-lookup"><span data-stu-id="0abac-105">In a subclass, the set of possible return codes can be specified by using a [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) qualifier on the method.</span></span> <span data-ttu-id="0abac-106">Строки, в которые транслируются содержимое **ValueMap** , также можно указать в подклассе как квалификатор массива **значений** .</span><span class="sxs-lookup"><span data-stu-id="0abac-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="0abac-107">Этот метод наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="0abac-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0abac-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0abac-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0abac-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0abac-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0abac-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="0abac-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0abac-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0abac-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0abac-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0abac-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="0abac-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="0abac-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0abac-114">*Елементточекк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0abac-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0abac-115">Ссылка на физический элемент, для которого проверяется совместимость.</span><span class="sxs-lookup"><span data-stu-id="0abac-115">Reference to the physical element for which to check compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0abac-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0abac-116">Return value</span></span>

<span data-ttu-id="0abac-117">Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="0abac-117">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0abac-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0abac-118">Remarks</span></span>

<span data-ttu-id="0abac-119">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0abac-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0abac-120">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="0abac-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0abac-121">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0abac-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0abac-122">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0abac-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0abac-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0abac-123">Requirements</span></span>



| <span data-ttu-id="0abac-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0abac-124">Requirement</span></span> | <span data-ttu-id="0abac-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0abac-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0abac-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0abac-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0abac-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0abac-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0abac-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0abac-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0abac-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0abac-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0abac-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0abac-130">Namespace</span></span><br/>                | <span data-ttu-id="0abac-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0abac-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0abac-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0abac-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0abac-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0abac-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0abac-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0abac-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0abac-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0abac-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0abac-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0abac-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abac-137">**\_Корпус CIM**</span><span class="sxs-lookup"><span data-stu-id="0abac-137">**CIM\_Chassis**</span></span>](iscompatible-method-in-class-cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="0abac-138">**\_Корпус CIM**</span><span class="sxs-lookup"><span data-stu-id="0abac-138">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> </dl>

 

