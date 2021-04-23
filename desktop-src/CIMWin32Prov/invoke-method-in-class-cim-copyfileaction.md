---
description: Метод Invoke \_ класса CIM копифилеактион принимает определенное действие. Сведения о том, как метод выполняет действие, зависит от реализации. Этот метод наследуется от \_ действия CIM.
ms.assetid: b948e9ed-332d-4ac5-be7f-88b7f46f5f1d
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_CopyFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CopyFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b88ddafd0420a40af8b815aab26849572cb7c019
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895706"
---
# <a name="invoke-method-of-the-cim_copyfileaction-class"></a><span data-ttu-id="4e408-105">Метод Invoke \_ класса CIM копифилеактион</span><span class="sxs-lookup"><span data-stu-id="4e408-105">Invoke method of the CIM\_CopyFileAction class</span></span>

<span data-ttu-id="4e408-106">Метод **Invoke** класса [**CIM \_ копифилеактион**](cim-copyfileaction.md) принимает определенное действие.</span><span class="sxs-lookup"><span data-stu-id="4e408-106">The **Invoke** method of the [**CIM\_CopyFileAction**](cim-copyfileaction.md) class takes a particular action.</span></span> <span data-ttu-id="4e408-107">Сведения о том, как метод выполняет действие, зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="4e408-107">Details about how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="4e408-108">Этот метод наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="4e408-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e408-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4e408-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e408-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e408-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e408-111">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4e408-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4e408-112">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4e408-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e408-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e408-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="4e408-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e408-114">Parameters</span></span>

<span data-ttu-id="4e408-115">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4e408-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e408-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e408-116">Return value</span></span>

<span data-ttu-id="4e408-117">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="4e408-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e408-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e408-118">Remarks</span></span>

<span data-ttu-id="4e408-119">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4e408-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4e408-120">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="4e408-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4e408-121">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4e408-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e408-122">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4e408-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e408-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4e408-123">Requirements</span></span>



| <span data-ttu-id="4e408-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4e408-124">Requirement</span></span> | <span data-ttu-id="4e408-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4e408-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e408-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e408-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4e408-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e408-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e408-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e408-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4e408-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e408-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e408-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4e408-130">Namespace</span></span><br/>                | <span data-ttu-id="4e408-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4e408-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e408-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4e408-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e408-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e408-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e408-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4e408-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e408-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e408-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e408-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e408-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e408-137">**\_КОПИФИЛЕАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="4e408-137">**CIM\_CopyFileAction**</span></span>](invoke-method-in-class-cim-copyfileaction.md)
</dt> <dt>

[<span data-ttu-id="4e408-138">**\_КОПИФИЛЕАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="4e408-138">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> </dl>

 

