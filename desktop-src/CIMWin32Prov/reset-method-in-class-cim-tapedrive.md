---
description: Метод Reset \_ класса CIM TapeDrive запрашивает сброс логического устройства.
ms.assetid: 48097e0d-7986-46b9-884d-7534f3848dd7
ms.tgt_platform: multiple
title: Метод Reset класса CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e5fd76d038e743ba5148f4c82555d50f0a5dde5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896390"
---
# <a name="reset-method-of-the-cim_tapedrive-class"></a><span data-ttu-id="0aae9-103">Метод Reset \_ класса CIM TapeDrive</span><span class="sxs-lookup"><span data-stu-id="0aae9-103">Reset method of the CIM\_TapeDrive class</span></span>

<span data-ttu-id="0aae9-104">Метод **Reset** \_ класса CIM TapeDrive запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0aae9-104">The **Reset** method of the CIM\_TapeDrive class requests a reset of the logical device.</span></span> <span data-ttu-id="0aae9-105">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="0aae9-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0aae9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0aae9-106">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="0aae9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0aae9-107">Parameters</span></span>

<span data-ttu-id="0aae9-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0aae9-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0aae9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0aae9-109">Return value</span></span>

<span data-ttu-id="0aae9-110">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="0aae9-110">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="0aae9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0aae9-111">Remarks</span></span>

<span data-ttu-id="0aae9-112">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0aae9-112">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0aae9-113">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="0aae9-113">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0aae9-114">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0aae9-114">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0aae9-115">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0aae9-115">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aae9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0aae9-116">Requirements</span></span>



| <span data-ttu-id="0aae9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0aae9-117">Requirement</span></span> | <span data-ttu-id="0aae9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0aae9-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0aae9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0aae9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0aae9-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0aae9-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0aae9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0aae9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0aae9-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0aae9-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0aae9-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0aae9-123">Namespace</span></span><br/>                | <span data-ttu-id="0aae9-124">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0aae9-124">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0aae9-125">MOF</span><span class="sxs-lookup"><span data-stu-id="0aae9-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0aae9-126"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0aae9-126"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0aae9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0aae9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aae9-128"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aae9-128"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aae9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0aae9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aae9-130">\_TAPEDRIVE CIM</span><span class="sxs-lookup"><span data-stu-id="0aae9-130">CIM\_TapeDrive</span></span>](reset-method-in-class-cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="0aae9-131">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="0aae9-131">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> </dl>

 

 




