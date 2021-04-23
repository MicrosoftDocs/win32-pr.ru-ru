---
description: Метод StartService помещает службу в &\# 0034; start&\# 0034; State.
ms.assetid: b2b38d64-b497-46f5-8638-a9a8ce50e888
ms.tgt_platform: multiple
title: Метод StartService класса CIM_BootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7f7f56633319f9e009f58f7c06dde7a3baee8e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990800"
---
# <a name="startservice-method-of-the-cim_bootservice-class"></a><span data-ttu-id="eb42f-103">Метод StartService \_ класса CIM бутсервице</span><span class="sxs-lookup"><span data-stu-id="eb42f-103">StartService method of the CIM\_BootService class</span></span>

<span data-ttu-id="eb42f-104">Метод **StartService** помещает службу в состояние "Start".</span><span class="sxs-lookup"><span data-stu-id="eb42f-104">The **StartService** method puts the service in a "start" state.</span></span> <span data-ttu-id="eb42f-105">В подклассе набор возможных кодов возврата можно указать с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="eb42f-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="eb42f-106">Строки, в которые транслируются содержимое **ValueMap** , могут также быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="eb42f-106">The strings to which the **ValueMap** contents are translated may also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="eb42f-107">Этот метод наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="eb42f-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb42f-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="eb42f-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eb42f-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eb42f-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eb42f-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="eb42f-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eb42f-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eb42f-111">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb42f-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb42f-112">Syntax</span></span>


```mof
Integer StartService();
```



## <a name="parameters"></a><span data-ttu-id="eb42f-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb42f-113">Parameters</span></span>

<span data-ttu-id="eb42f-114">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="eb42f-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb42f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb42f-115">Return value</span></span>

<span data-ttu-id="eb42f-116">Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="eb42f-116">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb42f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb42f-117">Remarks</span></span>

<span data-ttu-id="eb42f-118">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="eb42f-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="eb42f-119">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="eb42f-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="eb42f-120">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="eb42f-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eb42f-121">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb42f-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb42f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="eb42f-122">Requirements</span></span>



| <span data-ttu-id="eb42f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="eb42f-123">Requirement</span></span> | <span data-ttu-id="eb42f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="eb42f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb42f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb42f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="eb42f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb42f-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb42f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb42f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="eb42f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb42f-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb42f-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eb42f-129">Namespace</span></span><br/>                | <span data-ttu-id="eb42f-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eb42f-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb42f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="eb42f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb42f-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb42f-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb42f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eb42f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb42f-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb42f-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb42f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb42f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb42f-136">\_БУТСЕРВИЦЕ CIM</span><span class="sxs-lookup"><span data-stu-id="eb42f-136">CIM\_BootService</span></span>](startservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[<span data-ttu-id="eb42f-137">**\_БУТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="eb42f-137">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> </dl>

 

