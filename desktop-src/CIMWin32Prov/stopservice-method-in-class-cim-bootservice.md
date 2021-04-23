---
description: Останавливает службу, представленную объектом, производным от CIM \_ бутсервице.
ms.assetid: 443a2afa-ed46-4378-a06f-5f9f94af51c9
ms.tgt_platform: multiple
title: Метод «начало» класса CIM_BootService (Сдоиас. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c054a9d05410ddbe7ee7d11c5bd4adba9e0ce83b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538921"
---
# <a name="stopservice-method-of-the-cim_bootservice-class"></a><span data-ttu-id="a8b4a-103">Метод «начало» \_ класса CIM бутсервице</span><span class="sxs-lookup"><span data-stu-id="a8b4a-103">StopService method of the CIM\_BootService class</span></span>

<span data-ttu-id="a8b4a-104">Метод **«** незавершенный» останавливает службу, представленную объектом, производным от [**CIM \_ бутсервице**](cim-bootservice.md).</span><span class="sxs-lookup"><span data-stu-id="a8b4a-104">The **StopService** method stops the service represented by the object derived from [**CIM\_BootService**](cim-bootservice.md).</span></span> <span data-ttu-id="a8b4a-105">Этот метод наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="a8b4a-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8b4a-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="a8b4a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a8b4a-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a8b4a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a8b4a-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="a8b4a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a8b4a-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a8b4a-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b4a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8b4a-110">Syntax</span></span>


```mof
Integer StopService();
```



## <a name="parameters"></a><span data-ttu-id="a8b4a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8b4a-111">Parameters</span></span>

<span data-ttu-id="a8b4a-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a8b4a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8b4a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8b4a-113">Return value</span></span>

<span data-ttu-id="a8b4a-114">Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="a8b4a-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8b4a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8b4a-115">Remarks</span></span>

<span data-ttu-id="a8b4a-116">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="a8b4a-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a8b4a-117">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="a8b4a-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a8b4a-118">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="a8b4a-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a8b4a-119">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a8b4a-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b4a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a8b4a-120">Requirements</span></span>



| <span data-ttu-id="a8b4a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a8b4a-121">Requirement</span></span> | <span data-ttu-id="a8b4a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a8b4a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b4a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8b4a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b4a-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8b4a-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8b4a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8b4a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b4a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8b4a-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8b4a-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a8b4a-127">Namespace</span></span><br/>                | <span data-ttu-id="a8b4a-128">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a8b4a-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8b4a-129">Header</span><span class="sxs-lookup"><span data-stu-id="a8b4a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8b4a-130"><dt>Сдоиас. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b4a-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="a8b4a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a8b4a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8b4a-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8b4a-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8b4a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a8b4a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8b4a-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8b4a-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b4a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8b4a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b4a-136">\_БУТСЕРВИЦЕ CIM</span><span class="sxs-lookup"><span data-stu-id="a8b4a-136">CIM\_BootService</span></span>](stopservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[<span data-ttu-id="a8b4a-137">**\_БУТСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="a8b4a-137">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> </dl>

 

