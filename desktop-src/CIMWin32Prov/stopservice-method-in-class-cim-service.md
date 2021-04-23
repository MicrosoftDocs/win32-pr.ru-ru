---
description: Останавливает службу, представленную объектом, производным от \_ службы CIM.
ms.assetid: f9eedde7-8d71-40a2-b1e9-7ba97e634f64
ms.tgt_platform: multiple
title: Метод «начало» класса CIM_Service (Сдоиас. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14a7d378b514a93906c3be4f711bd6ab5b88bf17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141551"
---
# <a name="stopservice-method-of-the-cim_service-class-sdoiash"></a><span data-ttu-id="93db9-103">Метод «начало» класса CIM_Service (Сдоиас. h)</span><span class="sxs-lookup"><span data-stu-id="93db9-103">StopService method of the CIM_Service class (Sdoias.h)</span></span>

<span data-ttu-id="93db9-104">Метод **«** незавершенный» останавливает службу, представленную объектом, производным от [**\_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="93db9-104">The **StopService** method stops the service represented by the object derived from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="93db9-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="93db9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="93db9-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="93db9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="93db9-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="93db9-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="93db9-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="93db9-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="93db9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93db9-109">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="93db9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="93db9-110">Parameters</span></span>

<span data-ttu-id="93db9-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="93db9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93db9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="93db9-112">Return value</span></span>

<span data-ttu-id="93db9-113">Возвращает значение 0 (нуль), если служба была успешно остановлена, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="93db9-113">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="93db9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93db9-114">Remarks</span></span>

<span data-ttu-id="93db9-115">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="93db9-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="93db9-116">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="93db9-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="93db9-117">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="93db9-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="93db9-118">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="93db9-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="93db9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="93db9-119">Requirements</span></span>



| <span data-ttu-id="93db9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="93db9-120">Requirement</span></span> | <span data-ttu-id="93db9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="93db9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93db9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93db9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="93db9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93db9-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93db9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93db9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="93db9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93db9-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93db9-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93db9-126">Namespace</span></span><br/>                | <span data-ttu-id="93db9-127">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="93db9-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93db9-128">Header</span><span class="sxs-lookup"><span data-stu-id="93db9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="93db9-129"><dt>Сдоиас. h</dt></span><span class="sxs-lookup"><span data-stu-id="93db9-129"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="93db9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="93db9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93db9-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93db9-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93db9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="93db9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93db9-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93db9-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93db9-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93db9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93db9-135">\_Служба CIM</span><span class="sxs-lookup"><span data-stu-id="93db9-135">CIM\_Service</span></span>](stopservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="93db9-136">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="93db9-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

