---
description: Метод Reset \_ класса принтера CIM запрашивает сброс логического устройства.
ms.assetid: 7d5c9e57-0f48-4a31-855d-d06197a9b5df
ms.tgt_platform: multiple
title: Метод Reset класса CIM_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42e4f4ff44eb1de7b0834239cf0d8af0ea88b42c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655751"
---
# <a name="reset-method-of-the-cim_printer-class"></a><span data-ttu-id="18785-103">Метод Reset класса модели CIM \_</span><span class="sxs-lookup"><span data-stu-id="18785-103">Reset method of the CIM\_Printer class</span></span>

<span data-ttu-id="18785-104">Метод **Reset** \_ класса принтера CIM запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="18785-104">The **Reset** method of the CIM\_Printer class requests a reset of the logical device.</span></span> <span data-ttu-id="18785-105">Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.</span><span class="sxs-lookup"><span data-stu-id="18785-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18785-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="18785-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="18785-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="18785-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="18785-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18785-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="18785-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="18785-109">Parameters</span></span>

<span data-ttu-id="18785-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="18785-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18785-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="18785-111">Return value</span></span>

<span data-ttu-id="18785-112">Возвращает 0 (ноль), если запрос был успешно выполнен, 1 (один), если запрос не поддерживается, и другое значение, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="18785-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="18785-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18785-113">Remarks</span></span>

<span data-ttu-id="18785-114">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="18785-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="18785-115">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="18785-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="18785-116">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="18785-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="18785-117">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="18785-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="18785-118">Требования</span><span class="sxs-lookup"><span data-stu-id="18785-118">Requirements</span></span>



| <span data-ttu-id="18785-119">Требование</span><span class="sxs-lookup"><span data-stu-id="18785-119">Requirement</span></span> | <span data-ttu-id="18785-120">Значение</span><span class="sxs-lookup"><span data-stu-id="18785-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18785-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18785-121">Minimum supported client</span></span><br/> | <span data-ttu-id="18785-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18785-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="18785-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18785-123">Minimum supported server</span></span><br/> | <span data-ttu-id="18785-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18785-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="18785-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18785-125">Namespace</span></span><br/>                | <span data-ttu-id="18785-126">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="18785-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="18785-127">MOF</span><span class="sxs-lookup"><span data-stu-id="18785-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18785-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18785-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="18785-129">DLL</span><span class="sxs-lookup"><span data-stu-id="18785-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18785-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18785-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18785-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18785-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18785-132">\_Принтер CIM</span><span class="sxs-lookup"><span data-stu-id="18785-132">CIM\_Printer</span></span>](reset-method-in-class-cim-printer.md)
</dt> <dt>

[<span data-ttu-id="18785-133">**\_Принтер CIM**</span><span class="sxs-lookup"><span data-stu-id="18785-133">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> </dl>

 

 




