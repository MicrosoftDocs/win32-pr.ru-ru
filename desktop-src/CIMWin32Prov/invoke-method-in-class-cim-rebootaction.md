---
description: Метод Invoke \_ класса CIM ребутактион принимает определенное действие. Сведения о том, как метод выполняет действие, зависят от реализации. Этот метод наследуется от \_ действия CIM.
ms.assetid: 27b6571e-94fe-423e-89ab-5ba2bc632882
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_RebootAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RebootAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e68849a486cc6a5b61dc55cf86e259e2f58435e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655778"
---
# <a name="invoke-method-of-the-cim_rebootaction-class"></a><span data-ttu-id="cb950-105">Метод Invoke \_ класса CIM ребутактион</span><span class="sxs-lookup"><span data-stu-id="cb950-105">Invoke method of the CIM\_RebootAction class</span></span>

<span data-ttu-id="cb950-106">Метод **Invoke** класса [**CIM \_ ребутактион**](cim-rebootaction.md) принимает определенное действие.</span><span class="sxs-lookup"><span data-stu-id="cb950-106">The **Invoke** method of the [**CIM\_RebootAction**](cim-rebootaction.md) class takes a particular action.</span></span> <span data-ttu-id="cb950-107">Сведения о том, как метод выполняет действие, зависят от реализации.</span><span class="sxs-lookup"><span data-stu-id="cb950-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="cb950-108">Этот метод наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="cb950-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb950-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cb950-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cb950-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cb950-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cb950-111">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="cb950-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cb950-112">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cb950-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb950-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb950-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="cb950-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb950-114">Parameters</span></span>

<span data-ttu-id="cb950-115">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cb950-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb950-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb950-116">Return value</span></span>

<span data-ttu-id="cb950-117">Возвращает целочисленное значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="cb950-117">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb950-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb950-118">Remarks</span></span>

<span data-ttu-id="cb950-119">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="cb950-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cb950-120">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="cb950-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cb950-121">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cb950-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cb950-122">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cb950-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb950-123">Требования</span><span class="sxs-lookup"><span data-stu-id="cb950-123">Requirements</span></span>



| <span data-ttu-id="cb950-124">Требование</span><span class="sxs-lookup"><span data-stu-id="cb950-124">Requirement</span></span> | <span data-ttu-id="cb950-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cb950-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb950-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb950-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cb950-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb950-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb950-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb950-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cb950-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb950-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb950-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cb950-130">Namespace</span></span><br/>                | <span data-ttu-id="cb950-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cb950-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb950-132">MOF</span><span class="sxs-lookup"><span data-stu-id="cb950-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb950-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb950-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb950-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cb950-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb950-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb950-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb950-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb950-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb950-137">\_РЕБУТАКТИОН CIM</span><span class="sxs-lookup"><span data-stu-id="cb950-137">CIM\_RebootAction</span></span>](invoke-method-in-class-cim-rebootaction.md)
</dt> <dt>

[<span data-ttu-id="cb950-138">**\_РЕБУТАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="cb950-138">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> </dl>

 

