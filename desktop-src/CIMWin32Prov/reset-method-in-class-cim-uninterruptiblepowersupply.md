---
description: Метод Reset \_ класса CIM унинтерруптиблеповерсуппли запрашивает сброс логического устройства.
ms.assetid: be04a10d-267c-4001-93ac-408a133ca923
ms.tgt_platform: multiple
title: Метод Reset класса CIM_UninterruptiblePowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UninterruptiblePowerSupply.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54068e460ef2a1c6e6eee7500c018c485b81bd6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896389"
---
# <a name="reset-method-of-the-cim_uninterruptiblepowersupply-class"></a><span data-ttu-id="6e303-103">Метод Reset \_ класса CIM унинтерруптиблеповерсуппли</span><span class="sxs-lookup"><span data-stu-id="6e303-103">Reset method of the CIM\_UninterruptiblePowerSupply class</span></span>

<span data-ttu-id="6e303-104">Метод **Reset** \_ класса CIM унинтерруптиблеповерсуппли запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="6e303-104">The **Reset** method of the CIM\_UninterruptiblePowerSupply class requests a reset of the logical device.</span></span> <span data-ttu-id="6e303-105">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="6e303-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e303-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6e303-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6e303-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6e303-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6e303-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e303-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="6e303-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e303-109">Parameters</span></span>

<span data-ttu-id="6e303-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6e303-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e303-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e303-111">Return value</span></span>

<span data-ttu-id="6e303-112">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="6e303-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e303-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e303-113">Remarks</span></span>

<span data-ttu-id="6e303-114">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6e303-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6e303-115">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="6e303-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6e303-116">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6e303-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6e303-117">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6e303-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e303-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6e303-118">Requirements</span></span>



| <span data-ttu-id="6e303-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6e303-119">Requirement</span></span> | <span data-ttu-id="6e303-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6e303-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e303-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e303-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e303-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e303-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6e303-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e303-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e303-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e303-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6e303-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e303-125">Namespace</span></span><br/>                | <span data-ttu-id="6e303-126">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6e303-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6e303-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6e303-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e303-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e303-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e303-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6e303-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e303-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e303-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e303-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e303-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e303-132">\_УНИНТЕРРУПТИБЛЕПОВЕРСУППЛИ CIM</span><span class="sxs-lookup"><span data-stu-id="6e303-132">CIM\_UninterruptiblePowerSupply</span></span>](reset-method-in-class-cim-uninterruptiblepowersupply.md)
</dt> <dt>

[<span data-ttu-id="6e303-133">**\_УНИНТЕРРУПТИБЛЕПОВЕРСУППЛИ CIM**</span><span class="sxs-lookup"><span data-stu-id="6e303-133">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> </dl>

 

 




