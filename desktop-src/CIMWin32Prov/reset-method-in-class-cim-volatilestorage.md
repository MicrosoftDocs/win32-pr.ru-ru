---
description: Метод Reset \_ класса CIM волатилестораже запрашивает сброс логического устройства.
ms.assetid: 3a0c4bf7-a2c3-4001-9658-8c3a94c2e7f1
ms.tgt_platform: multiple
title: Метод Reset класса CIM_VolatileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolatileStorage.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f09efbcf19ebf4bfccfb03a771058a102932ae2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423229"
---
# <a name="reset-method-of-the-cim_volatilestorage-class"></a><span data-ttu-id="4e07b-103">Метод Reset \_ класса CIM волатилестораже</span><span class="sxs-lookup"><span data-stu-id="4e07b-103">Reset method of the CIM\_VolatileStorage class</span></span>

<span data-ttu-id="4e07b-104">Метод **Reset** \_ класса CIM волатилестораже запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4e07b-104">The **Reset** method of the CIM\_VolatileStorage class requests a reset of the logical device.</span></span> <span data-ttu-id="4e07b-105">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="4e07b-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e07b-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4e07b-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e07b-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e07b-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4e07b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e07b-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="4e07b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e07b-109">Parameters</span></span>

<span data-ttu-id="4e07b-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4e07b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e07b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e07b-111">Return value</span></span>

<span data-ttu-id="4e07b-112">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="4e07b-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e07b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e07b-113">Remarks</span></span>

<span data-ttu-id="4e07b-114">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4e07b-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4e07b-115">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="4e07b-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4e07b-116">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4e07b-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e07b-117">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4e07b-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e07b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4e07b-118">Requirements</span></span>



| <span data-ttu-id="4e07b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4e07b-119">Requirement</span></span> | <span data-ttu-id="4e07b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4e07b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e07b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e07b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e07b-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e07b-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e07b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e07b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e07b-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e07b-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e07b-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4e07b-125">Namespace</span></span><br/>                | <span data-ttu-id="4e07b-126">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4e07b-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e07b-127">MOF</span><span class="sxs-lookup"><span data-stu-id="4e07b-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e07b-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e07b-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e07b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4e07b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e07b-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e07b-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e07b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e07b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e07b-132">\_ВОЛАТИЛЕСТОРАЖЕ CIM</span><span class="sxs-lookup"><span data-stu-id="4e07b-132">CIM\_VolatileStorage</span></span>](reset-method-in-class-cim-volatilestorage.md)
</dt> <dt>

[<span data-ttu-id="4e07b-133">**\_ВОЛАТИЛЕСТОРАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="4e07b-133">**CIM\_VolatileStorage**</span></span>](cim-volatilestorage.md)
</dt> </dl>

 

 




