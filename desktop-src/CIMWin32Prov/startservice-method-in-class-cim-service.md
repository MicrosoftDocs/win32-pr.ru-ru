---
description: Метод StartService помещает службу в запущенное состояние.
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: Метод StartService класса CIM_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1592552595c06ec7111041cbb1c1b1d2628f8b6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807463"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="25e1b-103">Метод StartService класса CIM_Service (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="25e1b-103">StartService method of the CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="25e1b-104">Метод **StartService** помещает службу в запущенное состояние.</span><span class="sxs-lookup"><span data-stu-id="25e1b-104">The **StartService** method puts the service in a started state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25e1b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="25e1b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="25e1b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="25e1b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="25e1b-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="25e1b-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="25e1b-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="25e1b-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="25e1b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25e1b-109">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="25e1b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="25e1b-110">Parameters</span></span>

<span data-ttu-id="25e1b-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="25e1b-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25e1b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25e1b-112">Return value</span></span>

<span data-ttu-id="25e1b-113">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="25e1b-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="25e1b-114">В подклассе набор возможных кодов возврата можно указать с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="25e1b-114">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="25e1b-115">Строки, в которые транслируются содержимое **ValueMap** , также можно указать в подклассе как квалификатор массива **значений** .</span><span class="sxs-lookup"><span data-stu-id="25e1b-115">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="25e1b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25e1b-116">Remarks</span></span>

<span data-ttu-id="25e1b-117">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="25e1b-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="25e1b-118">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="25e1b-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="25e1b-119">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="25e1b-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="25e1b-120">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="25e1b-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="25e1b-121">Требования</span><span class="sxs-lookup"><span data-stu-id="25e1b-121">Requirements</span></span>



| <span data-ttu-id="25e1b-122">Требование</span><span class="sxs-lookup"><span data-stu-id="25e1b-122">Requirement</span></span> | <span data-ttu-id="25e1b-123">Значение</span><span class="sxs-lookup"><span data-stu-id="25e1b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25e1b-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25e1b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="25e1b-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25e1b-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25e1b-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25e1b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="25e1b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25e1b-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25e1b-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="25e1b-128">Namespace</span></span><br/>                | <span data-ttu-id="25e1b-129">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="25e1b-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25e1b-130">MOF</span><span class="sxs-lookup"><span data-stu-id="25e1b-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25e1b-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25e1b-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25e1b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="25e1b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25e1b-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25e1b-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e1b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25e1b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e1b-135">\_Служба CIM</span><span class="sxs-lookup"><span data-stu-id="25e1b-135">CIM\_Service</span></span>](startservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="25e1b-136">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="25e1b-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

