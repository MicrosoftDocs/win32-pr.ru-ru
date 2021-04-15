---
description: Метод Reset \_ класса контроллера CIM запрашивает сброс логического устройства.
ms.assetid: 98ec2010-4ce1-4aa8-941f-947714de8e7b
ms.tgt_platform: multiple
title: Метод Reset класса CIM_Controller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1585f153e16e7ffa7133871064f4ff7e1277243
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655891"
---
# <a name="reset-method-of-the-cim_controller-class"></a><span data-ttu-id="87811-103">Метод Reset \_ класса контроллера CIM</span><span class="sxs-lookup"><span data-stu-id="87811-103">Reset method of the CIM\_Controller class</span></span>

<span data-ttu-id="87811-104">Метод **Reset** \_ класса контроллера CIM запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="87811-104">The **Reset** method of the CIM\_Controller class requests a reset of the logical device.</span></span> <span data-ttu-id="87811-105">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="87811-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87811-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="87811-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="87811-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="87811-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="87811-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87811-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="87811-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="87811-109">Parameters</span></span>

<span data-ttu-id="87811-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="87811-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87811-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87811-111">Return value</span></span>

<span data-ttu-id="87811-112">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="87811-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="87811-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87811-113">Remarks</span></span>

<span data-ttu-id="87811-114">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="87811-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="87811-115">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="87811-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="87811-116">Дополнительные сведения см. в разделе [Создание поставщиков WMI](/windows/desktop/WmiSdk/creating-wmi-providers).</span><span class="sxs-lookup"><span data-stu-id="87811-116">For more information, see [Creating WMI Providers](/windows/desktop/WmiSdk/creating-wmi-providers).</span></span>

<span data-ttu-id="87811-117">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="87811-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="87811-118">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="87811-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="87811-119">Требования</span><span class="sxs-lookup"><span data-stu-id="87811-119">Requirements</span></span>



| <span data-ttu-id="87811-120">Требование</span><span class="sxs-lookup"><span data-stu-id="87811-120">Requirement</span></span> | <span data-ttu-id="87811-121">Значение</span><span class="sxs-lookup"><span data-stu-id="87811-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87811-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87811-122">Minimum supported client</span></span><br/> | <span data-ttu-id="87811-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87811-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87811-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87811-124">Minimum supported server</span></span><br/> | <span data-ttu-id="87811-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87811-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87811-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="87811-126">Namespace</span></span><br/>                | <span data-ttu-id="87811-127">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="87811-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87811-128">MOF</span><span class="sxs-lookup"><span data-stu-id="87811-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87811-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87811-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87811-130">DLL</span><span class="sxs-lookup"><span data-stu-id="87811-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87811-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87811-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87811-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87811-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87811-133">\_Контроллер CIM</span><span class="sxs-lookup"><span data-stu-id="87811-133">CIM\_Controller</span></span>](reset-method-in-class-cim-controller.md)
</dt> <dt>

[<span data-ttu-id="87811-134">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="87811-134">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

