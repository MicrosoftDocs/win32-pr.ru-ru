---
description: Метод StartService класса CIM_ClusteringService — метод StartService помещает службу в запущенное состояние.
ms.assetid: 2efd2a06-a03c-4f4c-b2fa-889f84faac0f
ms.tgt_platform: multiple
title: Метод StartService класса CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcd18af37da9302256776cfee844fd83f989c9b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086192"
---
# <a name="startservice-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="fa714-103">Метод StartService \_ класса CIM клустерингсервице</span><span class="sxs-lookup"><span data-stu-id="fa714-103">StartService method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="fa714-104">Метод **StartService** помещает службу в запущенное состояние.</span><span class="sxs-lookup"><span data-stu-id="fa714-104">The **StartService** method puts the service in a started state.</span></span> <span data-ttu-id="fa714-105">В подклассе набор возможных кодов возврата можно указать с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="fa714-105">In a subclass, the set of possible return codes can be specified using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="fa714-106">Строки, в которые транслируются содержимое **ValueMap** , также можно указать в подклассе как квалификатор массива **значений** .</span><span class="sxs-lookup"><span data-stu-id="fa714-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="fa714-107">Этот метод наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="fa714-107">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa714-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="fa714-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fa714-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fa714-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fa714-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="fa714-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fa714-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fa714-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fa714-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa714-112">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="fa714-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa714-113">Parameters</span></span>

<span data-ttu-id="fa714-114">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fa714-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa714-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa714-115">Return value</span></span>

<span data-ttu-id="fa714-116">Возвращает значение 0 (нуль), если служба была успешно запущена, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="fa714-116">Returns a value of 0 (zero) if the service was successfully started, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa714-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="fa714-117">Remarks</span></span>

<span data-ttu-id="fa714-118">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="fa714-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fa714-119">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="fa714-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fa714-120">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="fa714-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fa714-121">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="fa714-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa714-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fa714-122">Requirements</span></span>



| <span data-ttu-id="fa714-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fa714-123">Requirement</span></span> | <span data-ttu-id="fa714-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fa714-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa714-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa714-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa714-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa714-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa714-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa714-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa714-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa714-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa714-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fa714-129">Namespace</span></span><br/>                | <span data-ttu-id="fa714-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fa714-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa714-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fa714-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa714-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa714-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa714-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fa714-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa714-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa714-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa714-135">См. также</span><span class="sxs-lookup"><span data-stu-id="fa714-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa714-136">\_КЛУСТЕРИНГСЕРВИЦЕ CIM</span><span class="sxs-lookup"><span data-stu-id="fa714-136">CIM\_ClusteringService</span></span>](startservice-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="fa714-137">**\_КЛУСТЕРИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="fa714-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

