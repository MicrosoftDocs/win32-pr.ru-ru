---
description: Метод Invoke \_ класса CIM директоряктион принимает определенное действие. Сведения о том, как метод выполняет действие, зависит от реализации. Этот метод наследуется от \_ действия CIM.
ms.assetid: e919dfdb-a52d-4bcb-abff-e1273c406226
ms.tgt_platform: multiple
title: Метод Invoke класса CIM_DirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f30184fe46cd8e8b9a595545ccba9a7d738af18e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895702"
---
# <a name="invoke-method-of-the-cim_directoryaction-class"></a><span data-ttu-id="81687-105">Метод Invoke \_ класса CIM директоряктион</span><span class="sxs-lookup"><span data-stu-id="81687-105">Invoke method of the CIM\_DirectoryAction class</span></span>

<span data-ttu-id="81687-106">Метод **Invoke** класса [**CIM \_ директоряктион**](cim-directoryaction.md) принимает определенное действие.</span><span class="sxs-lookup"><span data-stu-id="81687-106">The **Invoke** method of the [**CIM\_DirectoryAction**](cim-directoryaction.md) class takes a particular action.</span></span> <span data-ttu-id="81687-107">Сведения о том, как метод выполняет действие, зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="81687-107">Details of how the method performs the action are implementation-specific.</span></span> <span data-ttu-id="81687-108">Этот метод наследуется [**от \_ действия CIM**](cim-action.md).</span><span class="sxs-lookup"><span data-stu-id="81687-108">This method is inherited from [**CIM\_Action**](cim-action.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81687-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="81687-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="81687-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="81687-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="81687-111">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="81687-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="81687-112">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="81687-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="81687-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81687-113">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="81687-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="81687-114">Parameters</span></span>

<span data-ttu-id="81687-115">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="81687-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81687-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81687-116">Return value</span></span>

<span data-ttu-id="81687-117">Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если метод не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="81687-117">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="81687-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81687-118">Remarks</span></span>

<span data-ttu-id="81687-119">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="81687-119">WMI does not implement this class.</span></span>

<span data-ttu-id="81687-120">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="81687-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="81687-121">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="81687-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="81687-122">Требования</span><span class="sxs-lookup"><span data-stu-id="81687-122">Requirements</span></span>



| <span data-ttu-id="81687-123">Требование</span><span class="sxs-lookup"><span data-stu-id="81687-123">Requirement</span></span> | <span data-ttu-id="81687-124">Значение</span><span class="sxs-lookup"><span data-stu-id="81687-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81687-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81687-125">Minimum supported client</span></span><br/> | <span data-ttu-id="81687-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81687-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81687-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81687-127">Minimum supported server</span></span><br/> | <span data-ttu-id="81687-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81687-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81687-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="81687-129">Namespace</span></span><br/>                | <span data-ttu-id="81687-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="81687-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81687-131">MOF</span><span class="sxs-lookup"><span data-stu-id="81687-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81687-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81687-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81687-133">DLL</span><span class="sxs-lookup"><span data-stu-id="81687-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81687-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81687-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81687-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81687-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81687-136">\_ДИРЕКТОРЯКТИОН CIM</span><span class="sxs-lookup"><span data-stu-id="81687-136">CIM\_DirectoryAction</span></span>](invoke-method-in-class-cim-directoryaction.md)
</dt> <dt>

[<span data-ttu-id="81687-137">**\_ДИРЕКТОРЯКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="81687-137">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> </dl>

 

