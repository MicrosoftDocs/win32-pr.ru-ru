---
description: '\_ \_ Структура шага транспорта MPEG2 описывает формат пакетов транспорта MPEG-2.'
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: Структура MPEG2_TRANSPORT_STRIDE (Бдатипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685189"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="d7ebb-103">\_ \_ Структура шага передачи MPEG2</span><span class="sxs-lookup"><span data-stu-id="d7ebb-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="d7ebb-104">`MPEG2_TRANSPORT_STRIDE`Структура описывает формат пакетов транспортного потока MPEG-2 (TS).</span><span class="sxs-lookup"><span data-stu-id="d7ebb-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="d7ebb-105">Эта структура позволяет передавать потоки, в которых 188-байтные транспортные пакеты не являются смежными.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="d7ebb-106">Для целей этой документации такие пакеты называются *пакетами STRIDE*.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="d7ebb-107">Пакеты STRIDE идентифицируются по следующему типу носителя:</span><span class="sxs-lookup"><span data-stu-id="d7ebb-107">Stride packets are identified by the following media type:</span></span>



|             |                                        |
|-------------|----------------------------------------|
| <span data-ttu-id="d7ebb-108">Основной тип</span><span class="sxs-lookup"><span data-stu-id="d7ebb-108">Major Type</span></span>  | <span data-ttu-id="d7ebb-109">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="d7ebb-109">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="d7ebb-110">Subtype</span><span class="sxs-lookup"><span data-stu-id="d7ebb-110">Subtype</span></span>     | <span data-ttu-id="d7ebb-111">\_ \_ Шаг транспорта медиасубтипе \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="d7ebb-111">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="d7ebb-112">Тип формата</span><span class="sxs-lookup"><span data-stu-id="d7ebb-112">Format Type</span></span> | <span data-ttu-id="d7ebb-113">Отформатировать \_ нет</span><span class="sxs-lookup"><span data-stu-id="d7ebb-113">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="d7ebb-114">Блок формата (**пбформат**) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-114">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="d7ebb-115">Если блок формата включен, он должен начинаться с структуры STRIDE с использованием **\_ \_ транспорта MPEG2** .</span><span class="sxs-lookup"><span data-stu-id="d7ebb-115">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="d7ebb-116">Эта структура определяет макет транспортного пакета в пакете STRIDE.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-116">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="d7ebb-117">Если блок формата имеет **значение NULL**, предполагается, что пакеты используют набор значений по умолчанию. Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="d7ebb-117">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ebb-118">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7ebb-118">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="d7ebb-119">Члены</span><span class="sxs-lookup"><span data-stu-id="d7ebb-119">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7ebb-120">**двоффсет**</span><span class="sxs-lookup"><span data-stu-id="d7ebb-120">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="d7ebb-121">Указывает смещение (в байтах) от начала пакета до первого байта внедренного транспортного пакета.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-121">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="d7ebb-122">Значение должно находиться в диапазоне от нуля до `(dwStride - dwPacketLength)` включительно.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-122">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="d7ebb-123">**двпаккетленгс**</span><span class="sxs-lookup"><span data-stu-id="d7ebb-123">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="d7ebb-124">Указывает длину внедренного транспортного пакета в байтах.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-124">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="d7ebb-125">Для стандартных транспортных пакетов MPEG-2 значение должно быть 188 байт.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-125">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d7ebb-126">**двстриде**</span><span class="sxs-lookup"><span data-stu-id="d7ebb-126">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="d7ebb-127">Указывает длину всего пакета STRIDE в байтах.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-127">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="d7ebb-128">Значение должно быть не меньше `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="d7ebb-128">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7ebb-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7ebb-129">Remarks</span></span>

<span data-ttu-id="d7ebb-130">На следующей схеме показаны связи между членами структуры.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-130">The following diagram illustrates the relations between the structure members.</span></span>

![пакет с шагом MPEG-2](images/mpeg2-stride-packet.png)

<span data-ttu-id="d7ebb-132">Входные буферы, содержащие мультиплексированные пакеты STRIDE, имеют некоторые ограничения.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-132">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="d7ebb-133">Пакеты STRIDE должны упаковываться последовательно в буфер.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-133">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="d7ebb-134">Ни один байт не может предшествовать первому пакету STRIDE или следовать за последним пакетом STRIDE.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-134">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="d7ebb-135">Целое число пакетов STRIDE должно помещаться в буфер; то есть длина буфера% Двстриде равна нулю.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-135">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="d7ebb-136">Количество пакетов STRIDE на один буфер не ограничено.</span><span class="sxs-lookup"><span data-stu-id="d7ebb-136">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="d7ebb-137">Если тип мультимедиа не содержит блок формата (**пбформат** имеет **значение NULL**), используются следующие значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="d7ebb-137">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="d7ebb-138">**двоффсет**: 0</span><span class="sxs-lookup"><span data-stu-id="d7ebb-138">**dwOffset**: 0</span></span>
-   <span data-ttu-id="d7ebb-139">**двпаккетленгс**: 188</span><span class="sxs-lookup"><span data-stu-id="d7ebb-139">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="d7ebb-140">**двстриде**: 188</span><span class="sxs-lookup"><span data-stu-id="d7ebb-140">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ebb-141">Требования</span><span class="sxs-lookup"><span data-stu-id="d7ebb-141">Requirements</span></span>



| <span data-ttu-id="d7ebb-142">Требование</span><span class="sxs-lookup"><span data-stu-id="d7ebb-142">Requirement</span></span> | <span data-ttu-id="d7ebb-143">Значение</span><span class="sxs-lookup"><span data-stu-id="d7ebb-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ebb-144">Header</span><span class="sxs-lookup"><span data-stu-id="d7ebb-144">Header</span></span><br/> | <dl> <span data-ttu-id="d7ebb-145"><dt>Бдатипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ebb-145"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ebb-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7ebb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ebb-147">Структуры DirectShow</span><span class="sxs-lookup"><span data-stu-id="d7ebb-147">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="d7ebb-148">Типы мультимедиа MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d7ebb-148">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




