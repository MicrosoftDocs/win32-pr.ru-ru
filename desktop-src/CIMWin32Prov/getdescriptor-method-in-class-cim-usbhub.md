---
description: Метод WebMethod возвращает дескриптор USB-концентратора, как указано в параметрах входных параметров.
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: Метод метода вмкодекдсп класса CIM_USBHub (. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d68374b4a9267dbc50fbb5b2cd8f1f46018e7f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990497"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a><span data-ttu-id="fec89-103">Метод \_ усбхуб класса CIM</span><span class="sxs-lookup"><span data-stu-id="fec89-103">GetDescriptor method of the CIM\_USBHub class</span></span>

<span data-ttu-id="fec89-104">Метод **WebMethod** возвращает дескриптор USB-концентратора, как указано в параметрах входных параметров.</span><span class="sxs-lookup"><span data-stu-id="fec89-104">The **GetDescriptor** method returns the USB hub descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fec89-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="fec89-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fec89-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fec89-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fec89-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="fec89-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fec89-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fec89-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fec89-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fec89-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="fec89-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="fec89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fec89-111">*RequestType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fec89-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fec89-112">Побитовый сопоставленный идентификатор для типа запроса дескриптора и получателя.</span><span class="sxs-lookup"><span data-stu-id="fec89-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="fec89-113">Соответствующие значения для каждого бита см. в спецификации USB.</span><span class="sxs-lookup"><span data-stu-id="fec89-113">For the appropriate values for each bit, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="fec89-114">*Рекуествалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fec89-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fec89-115">Содержит тип дескриптора в высоком байте и индекс дескриптора (например, индекс или смещение в массиве дескрипторов) в младших байтах.</span><span class="sxs-lookup"><span data-stu-id="fec89-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="fec89-116">Дополнительные сведения см. в спецификации USB.</span><span class="sxs-lookup"><span data-stu-id="fec89-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="fec89-117">*Рекуестиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fec89-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fec89-118">Задает 2-байтовый код языка, используемый USB-устройством при возврате данных дескриптора строки.</span><span class="sxs-lookup"><span data-stu-id="fec89-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="fec89-119">Параметр обычно имеет значение 0 (ноль) для нестроковых дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="fec89-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="fec89-120">Дополнительные сведения см. в спецификации USB.</span><span class="sxs-lookup"><span data-stu-id="fec89-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="fec89-121">*Рекуестленгс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="fec89-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fec89-122">Во входных данных — длина (в октетах) дескриптора, который должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="fec89-122">On input, the length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="fec89-123">Если это значение меньше фактической длины дескриптора, возвращается только запрошенная длина.</span><span class="sxs-lookup"><span data-stu-id="fec89-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="fec89-124">Если он превышает фактическую длину, возвращается фактическая длина.</span><span class="sxs-lookup"><span data-stu-id="fec89-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="fec89-125">На выходе Длина возвращаемого буфера (в октетах).</span><span class="sxs-lookup"><span data-stu-id="fec89-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="fec89-126">Если запрашиваемый дескриптор не существует, содержимое этого параметра не определено.</span><span class="sxs-lookup"><span data-stu-id="fec89-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="fec89-127">*Буфер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fec89-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fec89-128">Функция buffer возвращает запрошенные сведения о дескрипторе.</span><span class="sxs-lookup"><span data-stu-id="fec89-128">Buffer returns the requested descriptor information.</span></span> <span data-ttu-id="fec89-129">Если дескриптор не существует, содержимое буфера не определено.</span><span class="sxs-lookup"><span data-stu-id="fec89-129">If the descriptor does not exist, the contents of the buffer are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fec89-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fec89-130">Return value</span></span>

<span data-ttu-id="fec89-131">Возвращает значение 0 (нуль), если дескриптор USB возвращен успешно, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="fec89-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="fec89-132">В подклассе набор возможных кодов возврата можно указать с помощью квалификатора **ValueMap** в методе.</span><span class="sxs-lookup"><span data-stu-id="fec89-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="fec89-133">Строки, в которые транслируются содержимое **мофкуалифиер** , также могут быть указаны в подклассе как квалификатор массива **Values** .</span><span class="sxs-lookup"><span data-stu-id="fec89-133">The strings to which the **mofqualifier** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec89-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fec89-134">Remarks</span></span>

<span data-ttu-id="fec89-135">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="fec89-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fec89-136">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="fec89-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fec89-137">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="fec89-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fec89-138">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="fec89-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fec89-139">Требования</span><span class="sxs-lookup"><span data-stu-id="fec89-139">Requirements</span></span>



| <span data-ttu-id="fec89-140">Требование</span><span class="sxs-lookup"><span data-stu-id="fec89-140">Requirement</span></span> | <span data-ttu-id="fec89-141">Значение</span><span class="sxs-lookup"><span data-stu-id="fec89-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fec89-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fec89-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fec89-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fec89-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fec89-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fec89-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fec89-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fec89-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fec89-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fec89-146">Namespace</span></span><br/>                | <span data-ttu-id="fec89-147">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fec89-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fec89-148">Header</span><span class="sxs-lookup"><span data-stu-id="fec89-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="fec89-149"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="fec89-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="fec89-150">MOF</span><span class="sxs-lookup"><span data-stu-id="fec89-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fec89-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fec89-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fec89-152">DLL</span><span class="sxs-lookup"><span data-stu-id="fec89-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fec89-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fec89-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec89-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fec89-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec89-155">**\_УСБХУБ CIM**</span><span class="sxs-lookup"><span data-stu-id="fec89-155">**CIM\_USBHub**</span></span>](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[<span data-ttu-id="fec89-156">**\_УСБХУБ CIM**</span><span class="sxs-lookup"><span data-stu-id="fec89-156">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> </dl>

 

