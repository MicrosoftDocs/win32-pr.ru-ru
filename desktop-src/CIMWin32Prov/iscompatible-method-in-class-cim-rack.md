---
description: Проверяет, может ли упоминаемая в данный стеллаже стойка находиться в физическом пакете или вставляться в нее.
ms.assetid: 03276c6a-ca48-48bc-adbe-e53e02107abb
ms.tgt_platform: multiple
title: Метод, совместимый с классом CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6855b797e8941882aac1dc25d77b2ef7e3bc11c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655815"
---
# <a name="iscompatible-method-of-the-cim_rack-class"></a><span data-ttu-id="89bd9-103">Метод, совместимый с \_ классом стойки CIM</span><span class="sxs-lookup"><span data-stu-id="89bd9-103">IsCompatible method of the CIM\_Rack class</span></span>

<span data-ttu-id="89bd9-104">Метод, **совместимый** с, позволяет проверить, может ли задержаться ссылка на стойку в физическом пакете или вставляться в нее.</span><span class="sxs-lookup"><span data-stu-id="89bd9-104">The **IsCompatible** method verifies whether the referenced rack can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="89bd9-105">В подклассе набор возможных кодов возврата можно указать с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="89bd9-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="89bd9-106">Строки, в которые транслируются содержимое **ValueMap** , также можно указать в подклассе как квалификатор массива **значений** .</span><span class="sxs-lookup"><span data-stu-id="89bd9-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="89bd9-107">Этот метод наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="89bd9-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89bd9-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="89bd9-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89bd9-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="89bd9-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89bd9-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="89bd9-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="89bd9-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="89bd9-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="89bd9-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89bd9-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="89bd9-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="89bd9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89bd9-114">*Елементточекк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89bd9-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89bd9-115">Ссылка на физический элемент, к которому выполняется этот метод.</span><span class="sxs-lookup"><span data-stu-id="89bd9-115">Reference to the physical element that this method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89bd9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89bd9-116">Return value</span></span>

<span data-ttu-id="89bd9-117">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="89bd9-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="89bd9-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89bd9-118">Remarks</span></span>

<span data-ttu-id="89bd9-119">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="89bd9-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="89bd9-120">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="89bd9-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="89bd9-121">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="89bd9-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89bd9-122">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="89bd9-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89bd9-123">Требования</span><span class="sxs-lookup"><span data-stu-id="89bd9-123">Requirements</span></span>



| <span data-ttu-id="89bd9-124">Требование</span><span class="sxs-lookup"><span data-stu-id="89bd9-124">Requirement</span></span> | <span data-ttu-id="89bd9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="89bd9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89bd9-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89bd9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="89bd9-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89bd9-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89bd9-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89bd9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="89bd9-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89bd9-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89bd9-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="89bd9-130">Namespace</span></span><br/>                | <span data-ttu-id="89bd9-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="89bd9-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89bd9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="89bd9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89bd9-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89bd9-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89bd9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="89bd9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89bd9-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89bd9-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89bd9-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89bd9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89bd9-137">**\_Стойка CIM**</span><span class="sxs-lookup"><span data-stu-id="89bd9-137">**CIM\_Rack**</span></span>](iscompatible-method-in-class-cim-rack.md)
</dt> <dt>

[<span data-ttu-id="89bd9-138">**\_Стойка CIM**</span><span class="sxs-lookup"><span data-stu-id="89bd9-138">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> </dl>

 

