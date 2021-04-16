---
description: Проверяет, может ли связанный физический элемент быть включен в физический пакет или вставлен в него.
ms.assetid: 406aaa75-b48c-4377-adb5-e900676b6e36
ms.tgt_platform: multiple
title: Метод, совместимый с классом CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1957b8d0c1929ff6f7b4ef8c69fa55ea4ccc83b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655816"
---
# <a name="iscompatible-method-of-the-cim_physicalpackage-class"></a><span data-ttu-id="ecbfd-103">Метод, совместимый с \_ классом CIM фисикалпаккаже</span><span class="sxs-lookup"><span data-stu-id="ecbfd-103">IsCompatible method of the CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="ecbfd-104">Метод, **совместимый** с, проверяет, может ли связанный физический элемент содержать или вставляться в физический пакет.</span><span class="sxs-lookup"><span data-stu-id="ecbfd-104">The **IsCompatible** method verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="ecbfd-105">В подклассе набор возможных кодов возврата можно указать с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="ecbfd-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="ecbfd-106">Строки, в которые транслируются содержимое **ValueMap** , также можно указать в подклассе как квалификатор массива **значений** .</span><span class="sxs-lookup"><span data-stu-id="ecbfd-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ecbfd-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ecbfd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ecbfd-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ecbfd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ecbfd-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="ecbfd-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ecbfd-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ecbfd-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecbfd-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecbfd-111">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="ecbfd-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecbfd-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecbfd-113">*Елементточекк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ecbfd-113">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecbfd-114">Ссылка на физический элемент, к которому выполняется метод, **совместимый** с.</span><span class="sxs-lookup"><span data-stu-id="ecbfd-114">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecbfd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecbfd-115">Return value</span></span>

<span data-ttu-id="ecbfd-116">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="ecbfd-116">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecbfd-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ecbfd-117">Remarks</span></span>

<span data-ttu-id="ecbfd-118">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="ecbfd-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ecbfd-119">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="ecbfd-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ecbfd-120">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ecbfd-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ecbfd-121">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ecbfd-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbfd-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ecbfd-122">Requirements</span></span>



| <span data-ttu-id="ecbfd-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ecbfd-123">Requirement</span></span> | <span data-ttu-id="ecbfd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ecbfd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbfd-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecbfd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ecbfd-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecbfd-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ecbfd-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecbfd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ecbfd-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecbfd-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ecbfd-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ecbfd-129">Namespace</span></span><br/>                | <span data-ttu-id="ecbfd-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ecbfd-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ecbfd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ecbfd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecbfd-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecbfd-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecbfd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ecbfd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecbfd-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecbfd-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecbfd-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecbfd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecbfd-136">**\_ФИСИКАЛПАККАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ecbfd-136">**CIM\_PhysicalPackage**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="ecbfd-137">**\_ФИСИКАЛПАККАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="ecbfd-137">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

