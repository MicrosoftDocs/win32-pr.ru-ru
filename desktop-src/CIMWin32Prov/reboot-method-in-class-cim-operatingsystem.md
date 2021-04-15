---
description: Метод reboot запрашивает перезагрузку операционной системы.
ms.assetid: 2ce766dd-51a4-4ffb-a45a-40399f1110f6
ms.tgt_platform: multiple
title: Метод reboot класса CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e498dd16372503b23aa56471224faf4d5d0ff012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655642"
---
# <a name="reboot-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="257b6-103">Метод rereboot класса системы CIM \_</span><span class="sxs-lookup"><span data-stu-id="257b6-103">Reboot method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="257b6-104">Метод **reboot** запрашивает перезагрузку операционной системы.</span><span class="sxs-lookup"><span data-stu-id="257b6-104">The **Reboot** method requests a reboot of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="257b6-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="257b6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="257b6-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="257b6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="257b6-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="257b6-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="257b6-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="257b6-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="257b6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="257b6-109">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="257b6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="257b6-110">Parameters</span></span>

<span data-ttu-id="257b6-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="257b6-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="257b6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="257b6-112">Return value</span></span>

<span data-ttu-id="257b6-113">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="257b6-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="257b6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="257b6-114">Remarks</span></span>

<span data-ttu-id="257b6-115">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="257b6-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="257b6-116">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="257b6-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="257b6-117">Сведения о классах WMI, которые являются производными от CIM, см. в разделе [Классы Win32](win32-provider.md). [**\_**](cim-operatingsystem.md)</span><span class="sxs-lookup"><span data-stu-id="257b6-117">For WMI classes that are derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="257b6-118">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="257b6-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="257b6-119">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="257b6-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="257b6-120">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="257b6-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="257b6-121">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="257b6-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="257b6-122">Требования</span><span class="sxs-lookup"><span data-stu-id="257b6-122">Requirements</span></span>



| <span data-ttu-id="257b6-123">Требование</span><span class="sxs-lookup"><span data-stu-id="257b6-123">Requirement</span></span> | <span data-ttu-id="257b6-124">Значение</span><span class="sxs-lookup"><span data-stu-id="257b6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="257b6-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="257b6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="257b6-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="257b6-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="257b6-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="257b6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="257b6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="257b6-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="257b6-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="257b6-129">Namespace</span></span><br/>                | <span data-ttu-id="257b6-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="257b6-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="257b6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="257b6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="257b6-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="257b6-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="257b6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="257b6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="257b6-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="257b6-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="257b6-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="257b6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="257b6-136">Операционная система CIM \_</span><span class="sxs-lookup"><span data-stu-id="257b6-136">CIM\_OperatingSystem</span></span>](reboot-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="257b6-137">**Операционная система CIM \_**</span><span class="sxs-lookup"><span data-stu-id="257b6-137">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

