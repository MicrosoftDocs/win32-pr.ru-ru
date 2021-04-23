---
description: Метод Invoke \_ класса CIM филеактион принимает определенное действие. Сведения о том, как метод выполняет действие, зависят от реализации. Этот метод наследуется от \_ действия CIM.
ms.assetid: f7514d67-4141-4d1a-bdfd-83aa062291aa
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_FileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1d0a877936a27a681a20e5ffd73da9dda77dcf4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262590"
---
# <a name="invoke-method-of-the-cim_fileaction-class"></a><span data-ttu-id="0bf1c-105">Метод Invoke \_ класса CIM филеактион</span><span class="sxs-lookup"><span data-stu-id="0bf1c-105">Invoke method of the CIM\_FileAction class</span></span>

<span data-ttu-id="0bf1c-106">Метод **Invoke** класса [**CIM \_ филеактион**](cim-fileaction.md) принимает определенное действие.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-106">The **Invoke** method of the [**CIM\_FileAction**](cim-fileaction.md) class takes a particular action.</span></span> <span data-ttu-id="0bf1c-107">Сведения о том, как метод выполняет действие, зависят от реализации.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-107">Details of how the method performs the action are implementation specific.</span></span> <span data-ttu-id="0bf1c-108">Этот метод наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="0bf1c-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bf1c-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0bf1c-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0bf1c-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0bf1c-111">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="0bf1c-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0bf1c-112">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0bf1c-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0bf1c-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bf1c-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="0bf1c-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf1c-114">Parameters</span></span>

<span data-ttu-id="0bf1c-115">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bf1c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bf1c-116">Return value</span></span>

<span data-ttu-id="0bf1c-117">Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если метод не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bf1c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bf1c-118">Remarks</span></span>

<span data-ttu-id="0bf1c-119">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0bf1c-120">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0bf1c-121">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0bf1c-122">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0bf1c-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bf1c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0bf1c-123">Requirements</span></span>



| <span data-ttu-id="0bf1c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0bf1c-124">Requirement</span></span> | <span data-ttu-id="0bf1c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0bf1c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf1c-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0bf1c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf1c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0bf1c-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0bf1c-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0bf1c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf1c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bf1c-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0bf1c-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0bf1c-130">Namespace</span></span><br/>                | <span data-ttu-id="0bf1c-131">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0bf1c-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0bf1c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0bf1c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bf1c-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bf1c-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bf1c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0bf1c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bf1c-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bf1c-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bf1c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bf1c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf1c-137">\_ФИЛЕАКТИОН CIM</span><span class="sxs-lookup"><span data-stu-id="0bf1c-137">CIM\_FileAction</span></span>](invoke-method-in-class-cim-fileaction.md)
</dt> <dt>

[<span data-ttu-id="0bf1c-138">**\_ФИЛЕАКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="0bf1c-138">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> </dl>

 

