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
ms.openlocfilehash: 5153f6f79c2807634149222a126a7256a65ffe8a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908492"
---
# <a name="mpeg2_transport_stride-structure"></a><span data-ttu-id="08487-103">\_ \_ Структура шага передачи MPEG2</span><span class="sxs-lookup"><span data-stu-id="08487-103">MPEG2\_TRANSPORT\_STRIDE structure</span></span>

<span data-ttu-id="08487-104">`MPEG2_TRANSPORT_STRIDE`Структура описывает формат пакетов транспортного потока MPEG-2 (TS).</span><span class="sxs-lookup"><span data-stu-id="08487-104">The `MPEG2_TRANSPORT_STRIDE` structure describes the format of MPEG-2 transport stream (TS) packets.</span></span> <span data-ttu-id="08487-105">Эта структура позволяет передавать потоки, в которых 188-байтные транспортные пакеты не являются смежными.</span><span class="sxs-lookup"><span data-stu-id="08487-105">This structure allows for transports streams in which the 188-byte transport packets are not contiguous.</span></span> <span data-ttu-id="08487-106">Для целей этой документации такие пакеты называются *пакетами STRIDE*.</span><span class="sxs-lookup"><span data-stu-id="08487-106">For the purpose of this documentation, such packets are referred to as *stride packets*.</span></span>

<span data-ttu-id="08487-107">Пакеты STRIDE идентифицируются по следующему типу носителя:</span><span class="sxs-lookup"><span data-stu-id="08487-107">Stride packets are identified by the following media type:</span></span>



| <span data-ttu-id="08487-108">Метка</span><span class="sxs-lookup"><span data-stu-id="08487-108">Label</span></span> | <span data-ttu-id="08487-109">Значение</span><span class="sxs-lookup"><span data-stu-id="08487-109">Value</span></span> |
|-------------|----------------------------------------|
| <span data-ttu-id="08487-110">Основной тип</span><span class="sxs-lookup"><span data-stu-id="08487-110">Major Type</span></span>  | <span data-ttu-id="08487-111">\_Поток MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="08487-111">MEDIATYPE\_Stream</span></span>                      |
| <span data-ttu-id="08487-112">Subtype</span><span class="sxs-lookup"><span data-stu-id="08487-112">Subtype</span></span>     | <span data-ttu-id="08487-113">\_ \_ Шаг транспорта медиасубтипе \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="08487-113">MEDIASUBTYPE\_MPEG2\_TRANSPORT\_STRIDE</span></span> |
| <span data-ttu-id="08487-114">Тип формата</span><span class="sxs-lookup"><span data-stu-id="08487-114">Format Type</span></span> | <span data-ttu-id="08487-115">Отформатировать \_ нет</span><span class="sxs-lookup"><span data-stu-id="08487-115">FORMAT\_None</span></span>                           |



 

<span data-ttu-id="08487-116">Блок формата (**пбформат**) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="08487-116">The format block (**pbFormat**) is optional.</span></span> <span data-ttu-id="08487-117">Если блок формата включен, он должен начинаться с структуры STRIDE с использованием **\_ \_ транспорта MPEG2** .</span><span class="sxs-lookup"><span data-stu-id="08487-117">If the format block is included, it must begin with an **MPEG2\_TRANSPORT\_STRIDE** structure.</span></span> <span data-ttu-id="08487-118">Эта структура определяет макет транспортного пакета в пакете STRIDE.</span><span class="sxs-lookup"><span data-stu-id="08487-118">This structure defines the layout of the transport packet within the stride packet.</span></span> <span data-ttu-id="08487-119">Если блок формата имеет **значение NULL**, предполагается, что пакеты используют набор значений по умолчанию. Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="08487-119">If the format block is **NULL**, the packets are assumed to use a set of default values; see the Remarks section for details.</span></span>

## <a name="syntax"></a><span data-ttu-id="08487-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08487-120">Syntax</span></span>


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a><span data-ttu-id="08487-121">Члены</span><span class="sxs-lookup"><span data-stu-id="08487-121">Members</span></span>

<dl> <dt>

<span data-ttu-id="08487-122">**двоффсет**</span><span class="sxs-lookup"><span data-stu-id="08487-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="08487-123">Указывает смещение (в байтах) от начала пакета до первого байта внедренного транспортного пакета.</span><span class="sxs-lookup"><span data-stu-id="08487-123">Specifies the offset, in bytes, from the beginning of the packet to the first byte of the embedded transport packet.</span></span> <span data-ttu-id="08487-124">Значение должно находиться в диапазоне от нуля до `(dwStride - dwPacketLength)` включительно.</span><span class="sxs-lookup"><span data-stu-id="08487-124">The value must range from zero to `(dwStride - dwPacketLength)`, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="08487-125">**двпаккетленгс**</span><span class="sxs-lookup"><span data-stu-id="08487-125">**dwPacketLength**</span></span>
</dt> <dd>

<span data-ttu-id="08487-126">Указывает длину внедренного транспортного пакета в байтах.</span><span class="sxs-lookup"><span data-stu-id="08487-126">Specifies the length of the embedded transport packet, in bytes.</span></span> <span data-ttu-id="08487-127">Для стандартных транспортных пакетов MPEG-2 значение должно быть 188 байт.</span><span class="sxs-lookup"><span data-stu-id="08487-127">For standard MPEG-2 transport packets, the value must be 188 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="08487-128">**двстриде**</span><span class="sxs-lookup"><span data-stu-id="08487-128">**dwStride**</span></span>
</dt> <dd>

<span data-ttu-id="08487-129">Указывает длину всего пакета STRIDE в байтах.</span><span class="sxs-lookup"><span data-stu-id="08487-129">Specifies the length of the entire stride packet, in bytes.</span></span> <span data-ttu-id="08487-130">Значение должно быть не меньше `(dwOffset + dwPacketLength)` .</span><span class="sxs-lookup"><span data-stu-id="08487-130">The value must be at least `(dwOffset + dwPacketLength)`.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08487-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08487-131">Remarks</span></span>

<span data-ttu-id="08487-132">На следующей схеме показаны связи между членами структуры.</span><span class="sxs-lookup"><span data-stu-id="08487-132">The following diagram illustrates the relations between the structure members.</span></span>

![пакет с шагом MPEG-2](images/mpeg2-stride-packet.png)

<span data-ttu-id="08487-134">Входные буферы, содержащие мультиплексированные пакеты STRIDE, имеют некоторые ограничения.</span><span class="sxs-lookup"><span data-stu-id="08487-134">Input buffers that contain multiplexed stride packets have some restrictions:</span></span>

-   <span data-ttu-id="08487-135">Пакеты STRIDE должны упаковываться последовательно в буфер.</span><span class="sxs-lookup"><span data-stu-id="08487-135">Stride packets must be packed contiguously within the buffer.</span></span>
-   <span data-ttu-id="08487-136">Ни один байт не может предшествовать первому пакету STRIDE или следовать за последним пакетом STRIDE.</span><span class="sxs-lookup"><span data-stu-id="08487-136">No bytes may precede the first stride packet or follow the last stride packet.</span></span>
-   <span data-ttu-id="08487-137">Целое число пакетов STRIDE должно помещаться в буфер; то есть длина буфера% Двстриде равна нулю.</span><span class="sxs-lookup"><span data-stu-id="08487-137">An integral number of stride packets must fit in the buffer; that is, buffer length % dwStride equals zero.</span></span>

<span data-ttu-id="08487-138">Количество пакетов STRIDE на один буфер не ограничено.</span><span class="sxs-lookup"><span data-stu-id="08487-138">There is no restriction on the number of stride packets per buffer.</span></span>

<span data-ttu-id="08487-139">Если тип мультимедиа не содержит блок формата (**пбформат** имеет **значение NULL**), используются следующие значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="08487-139">If the media type does not contain a format block (**pbFormat** is **NULL**), the following default values are used:</span></span>

-   <span data-ttu-id="08487-140">**двоффсет**: 0</span><span class="sxs-lookup"><span data-stu-id="08487-140">**dwOffset**: 0</span></span>
-   <span data-ttu-id="08487-141">**двпаккетленгс**: 188</span><span class="sxs-lookup"><span data-stu-id="08487-141">**dwPacketLength**: 188</span></span>
-   <span data-ttu-id="08487-142">**двстриде**: 188</span><span class="sxs-lookup"><span data-stu-id="08487-142">**dwStride**: 188</span></span>

## <a name="requirements"></a><span data-ttu-id="08487-143">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="08487-143">Requirements</span></span>



| <span data-ttu-id="08487-144">Требование</span><span class="sxs-lookup"><span data-stu-id="08487-144">Requirement</span></span> | <span data-ttu-id="08487-145">Значение</span><span class="sxs-lookup"><span data-stu-id="08487-145">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08487-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="08487-146">Header</span></span><br/> | <dl> <span data-ttu-id="08487-147"><dt>Бдатипес. h</dt></span><span class="sxs-lookup"><span data-stu-id="08487-147"><dt>Bdatypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08487-148">См. также</span><span class="sxs-lookup"><span data-stu-id="08487-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08487-149">Структуры DirectShow</span><span class="sxs-lookup"><span data-stu-id="08487-149">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="08487-150">Типы мультимедиа MPEG-2</span><span class="sxs-lookup"><span data-stu-id="08487-150">MPEG-2 Media Types</span></span>](mpeg-2-media-types.md)
</dt> </dl>

 

 




