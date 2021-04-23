---
description: Метод Shutdown запрашивает завершение работы операционной системы.
ms.assetid: f2a2a98b-2f4f-4aa1-9f54-515660273c8d
ms.tgt_platform: multiple
title: Метод Shutdown класса CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78a11f325b8682b0024ff281a48989b837d3073a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895405"
---
# <a name="shutdown-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="cee52-103">Метод Shutdown класса системы CIM \_</span><span class="sxs-lookup"><span data-stu-id="cee52-103">Shutdown method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="cee52-104">Метод **Shutdown** запрашивает завершение работы операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cee52-104">The **Shutdown** method requests a shutdown of the operating system.</span></span> <span data-ttu-id="cee52-105">Реализация или подкласс операционной системы может устанавливать зависимости между методами **завершения работы** и [**перезагрузки**](reboot-method-in-class-cim-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="cee52-105">The implementation or subclass of the operating system can establish dependencies between the **Shutdown** and [**Reboot**](reboot-method-in-class-cim-operatingsystem.md) methods.</span></span> <span data-ttu-id="cee52-106">Например, можно предоставить более сложные возможности, такие как запланированное выключение и перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="cee52-106">For example, more sophisticated capabilities can be provided, such as a scheduled shutdown and reboot.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cee52-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cee52-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cee52-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cee52-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cee52-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="cee52-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cee52-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cee52-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cee52-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cee52-111">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="cee52-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="cee52-112">Parameters</span></span>

<span data-ttu-id="cee52-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cee52-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cee52-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cee52-114">Return value</span></span>

<span data-ttu-id="cee52-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="cee52-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cee52-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cee52-116">Remarks</span></span>

<span data-ttu-id="cee52-117">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="cee52-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cee52-118">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="cee52-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cee52-119">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cee52-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cee52-120">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cee52-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cee52-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cee52-121">Requirements</span></span>



| <span data-ttu-id="cee52-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cee52-122">Requirement</span></span> | <span data-ttu-id="cee52-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cee52-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cee52-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cee52-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cee52-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cee52-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cee52-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cee52-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cee52-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cee52-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cee52-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cee52-128">Namespace</span></span><br/>                | <span data-ttu-id="cee52-129">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cee52-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cee52-130">MOF</span><span class="sxs-lookup"><span data-stu-id="cee52-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cee52-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cee52-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cee52-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cee52-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cee52-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cee52-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cee52-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cee52-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cee52-135">Операционная система CIM \_</span><span class="sxs-lookup"><span data-stu-id="cee52-135">CIM\_OperatingSystem</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="cee52-136">**Операционная система CIM \_**</span><span class="sxs-lookup"><span data-stu-id="cee52-136">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

