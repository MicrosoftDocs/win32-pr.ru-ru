---
description: Метод Reset запрашивает сброс логического устройства. Этот метод наследуется от CIM-ого модели \_ .
ms.assetid: d764986b-b512-4f38-8284-d16b1f670871
ms.tgt_platform: multiple
title: Метод Reset класса CIM_Sensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Sensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7aaddafd0c2316bb2fb996ec5f9640e0135899c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142715"
---
# <a name="reset-method-of-the-cim_sensor-class"></a><span data-ttu-id="4b6dc-104">Метод Reset \_ класса датчика CIM</span><span class="sxs-lookup"><span data-stu-id="4b6dc-104">Reset method of the CIM\_Sensor class</span></span>

<span data-ttu-id="4b6dc-105">Метод **Reset** запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="4b6dc-106">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4b6dc-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4b6dc-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4b6dc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4b6dc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b6dc-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="4b6dc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b6dc-110">Parameters</span></span>

<span data-ttu-id="4b6dc-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b6dc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b6dc-112">Return value</span></span>

<span data-ttu-id="4b6dc-113">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b6dc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b6dc-114">Remarks</span></span>

<span data-ttu-id="4b6dc-115">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4b6dc-116">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4b6dc-117">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4b6dc-118">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4b6dc-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b6dc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4b6dc-119">Requirements</span></span>



| <span data-ttu-id="4b6dc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4b6dc-120">Requirement</span></span> | <span data-ttu-id="4b6dc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6dc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b6dc-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b6dc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4b6dc-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b6dc-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b6dc-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b6dc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4b6dc-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b6dc-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b6dc-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4b6dc-126">Namespace</span></span><br/>                | <span data-ttu-id="4b6dc-127">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4b6dc-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4b6dc-128">MOF</span><span class="sxs-lookup"><span data-stu-id="4b6dc-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b6dc-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b6dc-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b6dc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4b6dc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b6dc-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b6dc-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b6dc-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b6dc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b6dc-133">\_Датчик CIM</span><span class="sxs-lookup"><span data-stu-id="4b6dc-133">CIM\_Sensor</span></span>](reset-method-in-class-cim-sensor.md)
</dt> <dt>

[<span data-ttu-id="4b6dc-134">**\_Датчик CIM**</span><span class="sxs-lookup"><span data-stu-id="4b6dc-134">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

 




