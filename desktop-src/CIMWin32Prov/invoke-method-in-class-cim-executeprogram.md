---
description: Метод Invoke \_ класса CIM ексекутепрограм принимает определенное действие. Сведения о том, как метод выполняет действие, зависят от реализации. Этот метод наследуется от \_ действия CIM.
ms.assetid: 14a12fae-14a6-412a-a778-8dd34a5843d1
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_ExecuteProgram
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bdf9a4edb78bb47c0354991d161339099e4dc49f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423302"
---
# <a name="invoke-method-of-the-cim_executeprogram-class"></a><span data-ttu-id="7d42a-105">Метод Invoke \_ класса CIM ексекутепрограм</span><span class="sxs-lookup"><span data-stu-id="7d42a-105">Invoke method of the CIM\_ExecuteProgram class</span></span>

<span data-ttu-id="7d42a-106">Метод **Invoke** класса [**CIM \_ ексекутепрограм**](cim-executeprogram.md) принимает определенное действие.</span><span class="sxs-lookup"><span data-stu-id="7d42a-106">The **Invoke** method of the [**CIM\_ExecuteProgram**](cim-executeprogram.md) class takes a particular action.</span></span> <span data-ttu-id="7d42a-107">Сведения о том, как метод выполняет действие, зависят от реализации.</span><span class="sxs-lookup"><span data-stu-id="7d42a-107">The details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="7d42a-108">Этот метод наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="7d42a-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d42a-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7d42a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7d42a-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7d42a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7d42a-111">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="7d42a-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7d42a-112">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7d42a-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d42a-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d42a-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="7d42a-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d42a-114">Parameters</span></span>

<span data-ttu-id="7d42a-115">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7d42a-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d42a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d42a-116">Return value</span></span>

<span data-ttu-id="7d42a-117">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="7d42a-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d42a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d42a-118">Remarks</span></span>

<span data-ttu-id="7d42a-119">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7d42a-119">WMI does not implement this class.</span></span>

<span data-ttu-id="7d42a-120">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7d42a-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7d42a-121">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7d42a-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d42a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7d42a-122">Requirements</span></span>



| <span data-ttu-id="7d42a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7d42a-123">Requirement</span></span> | <span data-ttu-id="7d42a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7d42a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d42a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d42a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7d42a-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d42a-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d42a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d42a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7d42a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d42a-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d42a-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7d42a-129">Namespace</span></span><br/>                | <span data-ttu-id="7d42a-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7d42a-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7d42a-131">MOF</span><span class="sxs-lookup"><span data-stu-id="7d42a-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d42a-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d42a-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d42a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7d42a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d42a-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d42a-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d42a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d42a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d42a-136">\_ЕКСЕКУТЕПРОГРАМ CIM</span><span class="sxs-lookup"><span data-stu-id="7d42a-136">CIM\_ExecuteProgram</span></span>](invoke-method-in-class-cim-executeprogram.md)
</dt> <dt>

[<span data-ttu-id="7d42a-137">**\_ЕКСЕКУТЕПРОГРАМ CIM**</span><span class="sxs-lookup"><span data-stu-id="7d42a-137">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> </dl>

 

