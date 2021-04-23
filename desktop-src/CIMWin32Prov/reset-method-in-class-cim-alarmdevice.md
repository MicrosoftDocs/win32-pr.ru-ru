---
description: Метод Reset \_ класса CIM алармдевице запрашивает сброс логического устройства. Этот метод наследуется от CIM-ого модели \_ .
ms.assetid: e70718c5-2c80-4084-b233-b3e4d083e7b4
ms.tgt_platform: multiple
title: Метод Reset класса CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 442cac28c094e60c978099c2337076fd8f2df980
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496545"
---
# <a name="reset-method-of-the-cim_alarmdevice-class"></a><span data-ttu-id="0b3f2-104">Метод Reset \_ класса CIM алармдевице</span><span class="sxs-lookup"><span data-stu-id="0b3f2-104">Reset method of the CIM\_AlarmDevice class</span></span>

<span data-ttu-id="0b3f2-105">Метод **Reset** класса [**CIM \_ алармдевице**](cim-alarmdevice.md) запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0b3f2-105">The **Reset** method of the [**CIM\_AlarmDevice**](cim-alarmdevice.md) class requests a logical device reset.</span></span> <span data-ttu-id="0b3f2-106">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="0b3f2-106">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b3f2-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0b3f2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b3f2-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b3f2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0b3f2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b3f2-109">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="0b3f2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b3f2-110">Parameters</span></span>

<span data-ttu-id="0b3f2-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0b3f2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b3f2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b3f2-112">Return value</span></span>

<span data-ttu-id="0b3f2-113">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="0b3f2-113">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b3f2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b3f2-114">Remarks</span></span>

<span data-ttu-id="0b3f2-115">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0b3f2-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0b3f2-116">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="0b3f2-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0b3f2-117">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0b3f2-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0b3f2-118">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0b3f2-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b3f2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0b3f2-119">Requirements</span></span>



| <span data-ttu-id="0b3f2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0b3f2-120">Requirement</span></span> | <span data-ttu-id="0b3f2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0b3f2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3f2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b3f2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0b3f2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b3f2-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b3f2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b3f2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0b3f2-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b3f2-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b3f2-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0b3f2-126">Namespace</span></span><br/>                | <span data-ttu-id="0b3f2-127">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0b3f2-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b3f2-128">MOF</span><span class="sxs-lookup"><span data-stu-id="0b3f2-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b3f2-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b3f2-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b3f2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0b3f2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b3f2-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b3f2-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b3f2-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b3f2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3f2-133">\_АЛАРМДЕВИЦЕ CIM</span><span class="sxs-lookup"><span data-stu-id="0b3f2-133">CIM\_AlarmDevice</span></span>](reset-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[<span data-ttu-id="0b3f2-134">**\_АЛАРМДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="0b3f2-134">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> </dl>

 

 




