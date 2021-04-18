---
description: Переводит новую компьютерную систему в кластер.
ms.assetid: 26d9428e-99de-4dcb-96ed-d773f28e015a
ms.tgt_platform: multiple
title: Метод AddNode класса CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService.AddNode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1769ebb876fd2ae99c800a61b80d339a850ab232
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655846"
---
# <a name="addnode-method-of-the-cim_clusteringservice-class"></a><span data-ttu-id="4793a-103">Метод AddNode \_ класса CIM клустерингсервице</span><span class="sxs-lookup"><span data-stu-id="4793a-103">AddNode method of the CIM\_ClusteringService class</span></span>

<span data-ttu-id="4793a-104">Метод **AddNode** выводит новую компьютерную систему в кластер.</span><span class="sxs-lookup"><span data-stu-id="4793a-104">The **AddNode** method brings a new computer system into a cluster.</span></span> <span data-ttu-id="4793a-105">Добавляемый узел указывается в качестве параметра метода.</span><span class="sxs-lookup"><span data-stu-id="4793a-105">The node to be added is specified as a parameter to the method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4793a-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4793a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4793a-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4793a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4793a-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4793a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4793a-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4793a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4793a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4793a-110">Syntax</span></span>


```mof
uint32 AddNode(
  [in] CIM_ComputerSystem REF CS
);
```



## <a name="parameters"></a><span data-ttu-id="4793a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4793a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4793a-112">*CS* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4793a-112">*CS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4793a-113">Ссылка на компьютерную систему, добавляемую в кластер.</span><span class="sxs-lookup"><span data-stu-id="4793a-113">Reference to the computer system to add to the cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4793a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4793a-114">Return value</span></span>

<span data-ttu-id="4793a-115">Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если операция не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="4793a-115">Returns a value of 0 (zero) on success, 1 (one) if the operation is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4793a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4793a-116">Remarks</span></span>

<span data-ttu-id="4793a-117">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4793a-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4793a-118">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="4793a-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4793a-119">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4793a-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4793a-120">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4793a-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4793a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4793a-121">Requirements</span></span>



| <span data-ttu-id="4793a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4793a-122">Requirement</span></span> | <span data-ttu-id="4793a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4793a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4793a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4793a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4793a-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4793a-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4793a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4793a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4793a-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4793a-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4793a-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4793a-128">Namespace</span></span><br/>                | <span data-ttu-id="4793a-129">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4793a-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4793a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="4793a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4793a-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4793a-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4793a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4793a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4793a-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4793a-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4793a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4793a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4793a-135">**\_КЛУСТЕРИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="4793a-135">**CIM\_ClusteringService**</span></span>](addnode-method-in-class-cim-clusteringservice.md)
</dt> <dt>

[<span data-ttu-id="4793a-136">**\_КЛУСТЕРИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="4793a-136">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> </dl>

 

