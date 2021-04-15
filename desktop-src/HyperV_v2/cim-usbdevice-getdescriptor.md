---
description: Возвращает дескриптор Усбдевице, заданный входными параметрами.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Метод метода-дескриптора класса CIM_USBDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662810"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="a75ec-103">Метод метода-дескриптора класса CIM_USBDevice (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="a75ec-103">GetDescriptor method of the CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="a75ec-104">Возвращает дескриптор Усбдевице, заданный входными параметрами.</span><span class="sxs-lookup"><span data-stu-id="a75ec-104">Returns the USBDevice descriptor as specified by the input parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="a75ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a75ec-105">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="a75ec-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a75ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a75ec-107">*RequestType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a75ec-107">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a75ec-108">Битовая схема, идентифицирующая тип запроса дескриптора и получателя.</span><span class="sxs-lookup"><span data-stu-id="a75ec-108">Bit-map that identifies the type of Descriptor request and the recipient.</span></span> <span data-ttu-id="a75ec-109">Тип запроса может быть "Standard", "class" или "Vendor-зависящий".</span><span class="sxs-lookup"><span data-stu-id="a75ec-109">The type of request may be 'standard', 'class' or 'vendor-specific'.</span></span> <span data-ttu-id="a75ec-110">Получатель может иметь значение "Device", "Interface", "Endpoint" или "Other".</span><span class="sxs-lookup"><span data-stu-id="a75ec-110">The recipient may be 'device', 'interface', 'endpoint' or 'other'.</span></span> <span data-ttu-id="a75ec-111">Соответствующие значения для каждого бита приведены в спецификации USB.</span><span class="sxs-lookup"><span data-stu-id="a75ec-111">Refer to the USB Specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="a75ec-112">*Рекуествалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a75ec-112">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a75ec-113">Содержит тип дескриптора в высоком байте и индекс дескриптора (например, индекс или смещение в массиве дескрипторов) в младших байтах.</span><span class="sxs-lookup"><span data-stu-id="a75ec-113">Contains the Descriptor Type in the high byte and the Descriptor Index (for example, index or offset into the Descriptor array) in the low byte.</span></span> <span data-ttu-id="a75ec-114">Дополнительные сведения см. в спецификации USB.</span><span class="sxs-lookup"><span data-stu-id="a75ec-114">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="a75ec-115">*Рекуестиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a75ec-115">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a75ec-116">Определяет код языка 2 байта, используемый Усбдевице при возврате данных дескриптора строки.</span><span class="sxs-lookup"><span data-stu-id="a75ec-116">Defines the 2 byte Language ID code used by the USBDevice when returning string Descriptor data.</span></span> <span data-ttu-id="a75ec-117">Параметр обычно равен 0 для дескрипторов, не являющихся строковыми.</span><span class="sxs-lookup"><span data-stu-id="a75ec-117">The parameter is typically 0 for non-string Descriptors.</span></span> <span data-ttu-id="a75ec-118">Дополнительные сведения см. в спецификации USB.</span><span class="sxs-lookup"><span data-stu-id="a75ec-118">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="a75ec-119">*Рекуестленгс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a75ec-119">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a75ec-120">На входе содержит длину (в октетах) дескриптора, который должен быть возвращен.</span><span class="sxs-lookup"><span data-stu-id="a75ec-120">On input, contains the length (in octets) of the Descriptor that should be returned.</span></span> <span data-ttu-id="a75ec-121">Если это значение меньше фактической длины дескриптора, будет возвращена только запрошенная длина.</span><span class="sxs-lookup"><span data-stu-id="a75ec-121">If this value is less than the actual length of the Descriptor, only the requested length will be returned.</span></span> <span data-ttu-id="a75ec-122">Если он превышает фактическую длину, возвращается фактическая длина.</span><span class="sxs-lookup"><span data-stu-id="a75ec-122">If it is more than the actual length, the actual length is returned.</span></span> <span data-ttu-id="a75ec-123">В выходных данных этот параметр представляет собой длину возвращаемого буфера в октетах.</span><span class="sxs-lookup"><span data-stu-id="a75ec-123">On output, this parameter is the length, in octets, of the Buffer being returned.</span></span> <span data-ttu-id="a75ec-124">Если запрашиваемый дескриптор не существует, содержимое этого параметра не определено.</span><span class="sxs-lookup"><span data-stu-id="a75ec-124">If the requested Descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="a75ec-125">*Буфер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a75ec-125">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a75ec-126">Возвращает запрошенные сведения о дескрипторе.</span><span class="sxs-lookup"><span data-stu-id="a75ec-126">Returns the requested Descriptor information.</span></span> <span data-ttu-id="a75ec-127">Если дескриптор не существует, содержимое параметра не определено.</span><span class="sxs-lookup"><span data-stu-id="a75ec-127">If the Descriptor does not exist, the contents of the parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a75ec-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a75ec-128">Return value</span></span>

<span data-ttu-id="a75ec-129">Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="a75ec-129">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75ec-130">Требования</span><span class="sxs-lookup"><span data-stu-id="a75ec-130">Requirements</span></span>



| <span data-ttu-id="a75ec-131">Требование</span><span class="sxs-lookup"><span data-stu-id="a75ec-131">Requirement</span></span> | <span data-ttu-id="a75ec-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a75ec-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a75ec-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a75ec-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a75ec-134">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a75ec-134">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a75ec-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a75ec-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a75ec-136">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a75ec-136">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a75ec-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a75ec-137">Namespace</span></span><br/>                | <span data-ttu-id="a75ec-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a75ec-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a75ec-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a75ec-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a75ec-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a75ec-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a75ec-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a75ec-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a75ec-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a75ec-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a75ec-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a75ec-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a75ec-144">**\_УСБДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="a75ec-144">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

 




