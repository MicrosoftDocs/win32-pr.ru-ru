---
description: Метод Сетспид требует, чтобы скорость вентилятора была установлена в значение, указанное в входном параметре метода.
ms.assetid: 7dd1cd57-66c5-4b50-9a73-31caf0b824e6
ms.tgt_platform: multiple
title: Метод Сетспид класса CIM_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan.SetSpeed
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16d90dbef3a9318ad144303e5720cea0abbde03e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896497"
---
# <a name="setspeed-method-of-the-cim_fan-class"></a><span data-ttu-id="cf87c-103">Метод Сетспид класса "вентилятор CIM" \_</span><span class="sxs-lookup"><span data-stu-id="cf87c-103">SetSpeed method of the CIM\_Fan class</span></span>

<span data-ttu-id="cf87c-104">Метод **сетспид** требует, чтобы скорость вентилятора была установлена в значение, указанное в входном параметре метода.</span><span class="sxs-lookup"><span data-stu-id="cf87c-104">The **SetSpeed** method requests that the fan speed be set to the value specified in the method's input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf87c-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cf87c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cf87c-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cf87c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cf87c-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="cf87c-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="cf87c-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="cf87c-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="cf87c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf87c-109">Syntax</span></span>


```mof
uint32 SetSpeed(
  [in] uint64 DesiredSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="cf87c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf87c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf87c-111">*Десиредспид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf87c-111">*DesiredSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf87c-112">Запрошенная скорость вентилятора, в революции в минуту.</span><span class="sxs-lookup"><span data-stu-id="cf87c-112">Requested fan speed, in revolutions per minute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf87c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf87c-113">Return value</span></span>

<span data-ttu-id="cf87c-114">Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="cf87c-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf87c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf87c-115">Remarks</span></span>

<span data-ttu-id="cf87c-116">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="cf87c-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="cf87c-117">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="cf87c-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="cf87c-118">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cf87c-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cf87c-119">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cf87c-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf87c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="cf87c-120">Requirements</span></span>



| <span data-ttu-id="cf87c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="cf87c-121">Requirement</span></span> | <span data-ttu-id="cf87c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="cf87c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf87c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf87c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cf87c-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf87c-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf87c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf87c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cf87c-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf87c-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf87c-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cf87c-127">Namespace</span></span><br/>                | <span data-ttu-id="cf87c-128">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cf87c-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf87c-129">MOF</span><span class="sxs-lookup"><span data-stu-id="cf87c-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf87c-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf87c-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf87c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="cf87c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf87c-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf87c-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf87c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf87c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf87c-134">\_Вентилятор CIM</span><span class="sxs-lookup"><span data-stu-id="cf87c-134">CIM\_Fan</span></span>](setspeed-method-in-class-cim-fan.md)
</dt> <dt>

[<span data-ttu-id="cf87c-135">**\_Вентилятор CIM**</span><span class="sxs-lookup"><span data-stu-id="cf87c-135">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> </dl>

 

