---
description: Метод Reset запрашивает сброс логического устройства. Этот метод наследуется от CIM-ого модели \_ .
ms.assetid: 4ddbad2a-e586-434a-a33e-7d60dcb67b3a
ms.tgt_platform: multiple
title: Метод Reset класса CIM_DiscreteSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d45544e62144c2d3aa14d898b5d595d3ea5b34f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806976"
---
# <a name="reset-method-of-the-cim_discretesensor-class"></a><span data-ttu-id="acd31-104">Метод Reset \_ класса CIM дискретесенсор</span><span class="sxs-lookup"><span data-stu-id="acd31-104">Reset method of the CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="acd31-105">Метод **Reset** запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="acd31-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="acd31-106">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="acd31-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="acd31-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="acd31-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="acd31-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="acd31-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="acd31-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acd31-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="acd31-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="acd31-110">Parameters</span></span>

<span data-ttu-id="acd31-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="acd31-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="acd31-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acd31-112">Return value</span></span>

<span data-ttu-id="acd31-113">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="acd31-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="acd31-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="acd31-114">Remarks</span></span>

<span data-ttu-id="acd31-115">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="acd31-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="acd31-116">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="acd31-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="acd31-117">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="acd31-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="acd31-118">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="acd31-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="acd31-119">Требования</span><span class="sxs-lookup"><span data-stu-id="acd31-119">Requirements</span></span>



| <span data-ttu-id="acd31-120">Требование</span><span class="sxs-lookup"><span data-stu-id="acd31-120">Requirement</span></span> | <span data-ttu-id="acd31-121">Значение</span><span class="sxs-lookup"><span data-stu-id="acd31-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acd31-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acd31-122">Minimum supported client</span></span><br/> | <span data-ttu-id="acd31-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acd31-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="acd31-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acd31-124">Minimum supported server</span></span><br/> | <span data-ttu-id="acd31-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acd31-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="acd31-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="acd31-126">Namespace</span></span><br/>                | <span data-ttu-id="acd31-127">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="acd31-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="acd31-128">MOF</span><span class="sxs-lookup"><span data-stu-id="acd31-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acd31-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acd31-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="acd31-130">DLL</span><span class="sxs-lookup"><span data-stu-id="acd31-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acd31-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acd31-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acd31-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acd31-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acd31-133">\_ДИСКРЕТЕСЕНСОР CIM</span><span class="sxs-lookup"><span data-stu-id="acd31-133">CIM\_DiscreteSensor</span></span>](reset-method-in-class-cim-discretesensor.md)
</dt> <dt>

[<span data-ttu-id="acd31-134">**\_ДИСКРЕТЕСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="acd31-134">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> </dl>

 

 




