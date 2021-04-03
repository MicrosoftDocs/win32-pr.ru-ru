---
description: Метод Евиктноде удаляет компьютерную систему из кластера. Удаляемый узел указывается в качестве параметра метода.
ms.assetid: 4691d536-ade3-4a02-bc28-e31ebaf5d9e4
ms.tgt_platform: multiple
title: Метод Евиктноде класса CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.EvictNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d68ddc1adc0af335dcf2d4139cf7c1f0a381d986
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807253"
---
# <a name="evictnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="c33be-104">Метод Евиктноде \_ класса CIM клустерингсервице</span><span class="sxs-lookup"><span data-stu-id="c33be-104">EvictNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="c33be-105">Метод **евиктноде** удаляет компьютерную систему из кластера.</span><span class="sxs-lookup"><span data-stu-id="c33be-105">The **EvictNode** method removes a computer system from a cluster.</span></span> <span data-ttu-id="c33be-106">Удаляемый узел указывается в качестве параметра метода.</span><span class="sxs-lookup"><span data-stu-id="c33be-106">The node to be evicted is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c33be-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c33be-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c33be-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c33be-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c33be-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="c33be-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c33be-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c33be-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c33be-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c33be-111">Syntax</span></span>


```mof
uint32 EvictNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="c33be-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c33be-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c33be-113">*CS* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c33be-113">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c33be-114">Ссылка на компьютерную систему, которую необходимо удалить из кластера.</span><span class="sxs-lookup"><span data-stu-id="c33be-114">Reference to the computer system to remove from the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c33be-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c33be-115">Return value</span></span>

<span data-ttu-id="c33be-116">Возвращает 0 (нуль), если компьютерная система успешно удалена, 1 (один), если метод не поддерживается, и любое другое число, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="c33be-116">Returns 0 (zero) if the computer system is successfully evicted, 1 (one) if the method is not supported, and any other number if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="c33be-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c33be-117">Remarks</span></span>

<span data-ttu-id="c33be-118">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c33be-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c33be-119">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="c33be-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c33be-120">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c33be-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c33be-121">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c33be-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33be-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c33be-122">Requirements</span></span>



| <span data-ttu-id="c33be-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c33be-123">Requirement</span></span> | <span data-ttu-id="c33be-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c33be-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c33be-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c33be-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c33be-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c33be-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c33be-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c33be-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c33be-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c33be-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c33be-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c33be-129">Namespace</span></span><br/>                | <span data-ttu-id="c33be-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c33be-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c33be-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c33be-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c33be-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c33be-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c33be-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c33be-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c33be-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c33be-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c33be-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c33be-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33be-136">**\_КЛУСТЕРИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="c33be-136">**CIM\_ClusteringService**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="c33be-137">**\_КЛУСТЕРИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="c33be-137">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

