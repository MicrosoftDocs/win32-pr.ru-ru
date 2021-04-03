---
description: Метод Invoke \_ класса действия CIM принимает определенное действие. Сведения о том, как метод выполняет действие, зависит от реализации.
ms.assetid: 4f0be560-bd78-4c7f-b6e3-ca86837a84f9
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_Action
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e02e414fb05e0dd4ea97c3e3a4d87659fed4c963
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895709"
---
# <a name="invoke-method-of-the-cim_action-class"></a><span data-ttu-id="69831-104">Метод Invoke \_ класса действия CIM</span><span class="sxs-lookup"><span data-stu-id="69831-104">Invoke method of the CIM\_Action class</span></span>

<span data-ttu-id="69831-105">Метод **Invoke** класса [**\_ действия CIM**](cim-action.md) принимает определенное действие.</span><span class="sxs-lookup"><span data-stu-id="69831-105">The **Invoke** method of the [**CIM\_Action**](cim-action.md) class takes a particular action.</span></span> <span data-ttu-id="69831-106">Сведения о том, как метод выполняет действие, зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="69831-106">The details of how the method performs the action is implementation-specific.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="69831-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="69831-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="69831-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="69831-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="69831-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="69831-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="69831-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="69831-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="69831-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69831-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="69831-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="69831-112">Parameters</span></span>

<span data-ttu-id="69831-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="69831-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69831-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69831-114">Return value</span></span>

<span data-ttu-id="69831-115">Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если метод не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="69831-115">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="69831-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69831-116">Remarks</span></span>

<span data-ttu-id="69831-117">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="69831-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="69831-118">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="69831-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="69831-119">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="69831-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="69831-120">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="69831-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="69831-121">Требования</span><span class="sxs-lookup"><span data-stu-id="69831-121">Requirements</span></span>



| <span data-ttu-id="69831-122">Требование</span><span class="sxs-lookup"><span data-stu-id="69831-122">Requirement</span></span> | <span data-ttu-id="69831-123">Значение</span><span class="sxs-lookup"><span data-stu-id="69831-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69831-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69831-124">Minimum supported client</span></span><br/> | <span data-ttu-id="69831-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69831-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69831-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69831-126">Minimum supported server</span></span><br/> | <span data-ttu-id="69831-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69831-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69831-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="69831-128">Namespace</span></span><br/>                | <span data-ttu-id="69831-129">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="69831-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="69831-130">MOF</span><span class="sxs-lookup"><span data-stu-id="69831-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69831-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69831-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="69831-132">DLL</span><span class="sxs-lookup"><span data-stu-id="69831-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69831-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69831-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69831-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69831-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69831-135">\_Действие CIM</span><span class="sxs-lookup"><span data-stu-id="69831-135">CIM\_Action</span></span>](invoke-method-in-class-cim-action.md)
</dt> <dt>

[<span data-ttu-id="69831-136">**\_Действие CIM**</span><span class="sxs-lookup"><span data-stu-id="69831-136">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dt>

[<span data-ttu-id="69831-137">Классы CIM</span><span class="sxs-lookup"><span data-stu-id="69831-137">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

