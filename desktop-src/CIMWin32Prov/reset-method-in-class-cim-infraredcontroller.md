---
description: Метод Reset запрашивает сброс логического устройства. Этот метод наследуется от CIM-ого модели \_ .
ms.assetid: 16e77637-f063-4206-a9b3-2c7d08c652a6
ms.tgt_platform: multiple
title: Метод Reset класса CIM_InfraredController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InfraredController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8037088e68d91769cc34c4f2665902ad70019b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990709"
---
# <a name="reset-method-of-the-cim_infraredcontroller-class"></a><span data-ttu-id="fe6d7-104">Метод Reset \_ класса CIM инфраредконтроллер</span><span class="sxs-lookup"><span data-stu-id="fe6d7-104">Reset method of the CIM\_InfraredController class</span></span>

<span data-ttu-id="fe6d7-105">Метод **Reset** запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="fe6d7-105">The **Reset** method requests a reset of the logical device.</span></span> <span data-ttu-id="fe6d7-106">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="fe6d7-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe6d7-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="fe6d7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fe6d7-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fe6d7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fe6d7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe6d7-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="fe6d7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe6d7-110">Parameters</span></span>

<span data-ttu-id="fe6d7-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="fe6d7-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe6d7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe6d7-112">Return value</span></span>

<span data-ttu-id="fe6d7-113">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="fe6d7-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6d7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe6d7-114">Remarks</span></span>

<span data-ttu-id="fe6d7-115">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="fe6d7-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fe6d7-116">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="fe6d7-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fe6d7-117">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="fe6d7-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fe6d7-118">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="fe6d7-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6d7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fe6d7-119">Requirements</span></span>



| <span data-ttu-id="fe6d7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fe6d7-120">Requirement</span></span> | <span data-ttu-id="fe6d7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fe6d7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6d7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe6d7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fe6d7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe6d7-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe6d7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe6d7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fe6d7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe6d7-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe6d7-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fe6d7-126">Namespace</span></span><br/>                | <span data-ttu-id="fe6d7-127">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fe6d7-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fe6d7-128">MOF</span><span class="sxs-lookup"><span data-stu-id="fe6d7-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe6d7-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe6d7-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe6d7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fe6d7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe6d7-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe6d7-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe6d7-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe6d7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6d7-133">\_ИНФРАРЕДКОНТРОЛЛЕР CIM</span><span class="sxs-lookup"><span data-stu-id="fe6d7-133">CIM\_InfraredController</span></span>](reset-method-in-class-cim-infraredcontroller.md)
</dt> <dt>

[<span data-ttu-id="fe6d7-134">**\_ИНФРАРЕДКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="fe6d7-134">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> </dl>

 

 




