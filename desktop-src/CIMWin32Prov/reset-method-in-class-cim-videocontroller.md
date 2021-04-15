---
description: Метод Reset \_ класса CIM видеоконтроллер запрашивает сброс логического устройства.
ms.assetid: 4dab954d-ed0f-4620-b5a8-7e55185d0b7b
ms.tgt_platform: multiple
title: Метод Reset класса CIM_VideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03d5b8a64edf73cc7ef76847177a1e86b2efc20d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496686"
---
# <a name="reset-method-of-the-cim_videocontroller-class"></a><span data-ttu-id="cb0e0-103">Метод Reset \_ класса CIM видеоконтроллер</span><span class="sxs-lookup"><span data-stu-id="cb0e0-103">Reset method of the CIM\_VideoController class</span></span>

<span data-ttu-id="cb0e0-104">Метод **Reset** \_ класса CIM видеоконтроллер запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="cb0e0-104">The **Reset** method of the CIM\_VideoController class requests a reset of the logical device.</span></span> <span data-ttu-id="cb0e0-105">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="cb0e0-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb0e0-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cb0e0-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cb0e0-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cb0e0-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cb0e0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb0e0-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="cb0e0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb0e0-109">Parameters</span></span>

<span data-ttu-id="cb0e0-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cb0e0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb0e0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb0e0-111">Return value</span></span>

<span data-ttu-id="cb0e0-112">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="cb0e0-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb0e0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb0e0-113">Remarks</span></span>

<span data-ttu-id="cb0e0-114">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="cb0e0-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cb0e0-115">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="cb0e0-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cb0e0-116">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cb0e0-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cb0e0-117">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cb0e0-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb0e0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cb0e0-118">Requirements</span></span>



| <span data-ttu-id="cb0e0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cb0e0-119">Requirement</span></span> | <span data-ttu-id="cb0e0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cb0e0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb0e0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb0e0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cb0e0-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb0e0-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb0e0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb0e0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cb0e0-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb0e0-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb0e0-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cb0e0-125">Namespace</span></span><br/>                | <span data-ttu-id="cb0e0-126">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cb0e0-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb0e0-127">MOF</span><span class="sxs-lookup"><span data-stu-id="cb0e0-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb0e0-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb0e0-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb0e0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cb0e0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb0e0-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb0e0-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb0e0-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb0e0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb0e0-132">\_ВИДЕОКОНТРОЛЛЕР CIM</span><span class="sxs-lookup"><span data-stu-id="cb0e0-132">CIM\_VideoController</span></span>](reset-method-in-class-cim-videocontroller.md)
</dt> <dt>

[<span data-ttu-id="cb0e0-133">**\_ВИДЕОКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="cb0e0-133">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> </dl>

 

 




