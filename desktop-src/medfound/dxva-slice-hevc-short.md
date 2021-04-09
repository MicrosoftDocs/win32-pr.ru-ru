---
description: Задает данные элемента управления среза.
ms.assetid: ae3399e9-b78c-473d-8ed5-e570dfb676aa
title: Структура DXVA_Slice_HEVC_Short (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Slice_HEVC_Short
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 0d0f88e1534ef3d901023ebdee8ce9c36a8c2cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072567"
---
# <a name="dxva_slice_hevc_short-structure"></a><span data-ttu-id="d7f63-103">\_ \_ Короткая структура среза дксва HEVC \_</span><span class="sxs-lookup"><span data-stu-id="d7f63-103">DXVA\_Slice\_HEVC\_Short structure</span></span>

<span data-ttu-id="d7f63-104">Задает данные элемента управления среза.</span><span class="sxs-lookup"><span data-stu-id="d7f63-104">Specifies slice control data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7f63-105">Syntax</span></span>


```C++
typedef struct _DXVA_Slice_HEVC_Short {
  UINT   BSNALunitDataLocation;
  UINT   SliceBytesInBuffer;
  USHORT wBadSliceChopping;
} DXVA_Slice_HEVC_Short, *LPDXVA_Slice_HEVC_Short;
```



## <a name="members"></a><span data-ttu-id="d7f63-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d7f63-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7f63-107">**бсналунитдаталокатион**</span><span class="sxs-lookup"><span data-stu-id="d7f63-107">**BSNALunitDataLocation**</span></span>
</dt> <dd>

<span data-ttu-id="d7f63-108">Указывает расположение единицы NAL.</span><span class="sxs-lookup"><span data-stu-id="d7f63-108">Specifies the location of the NAL unit.</span></span>

</dd> <dt>

<span data-ttu-id="d7f63-109">**слицебитесинбуффер**</span><span class="sxs-lookup"><span data-stu-id="d7f63-109">**SliceBytesInBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="d7f63-110">Число байтов в буфере данных битовый поток, связанных с этой структурой данных элемента управления срезом.</span><span class="sxs-lookup"><span data-stu-id="d7f63-110">The number of bytes in the bitstream data buffer that are associated with this slice control data structure.</span></span>

</dd> <dt>

<span data-ttu-id="d7f63-111">**вбадслицечоппинг**</span><span class="sxs-lookup"><span data-stu-id="d7f63-111">**wBadSliceChopping**</span></span>
</dt> <dd>

<span data-ttu-id="d7f63-112">Если используется синтаксический анализ битовый поток, это значение указывает на некорректный срез и содержит одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="d7f63-112">If off-host bitstream parsing is used, this value indicates the bad slice chopping and contains one of the following values:</span></span>



| <span data-ttu-id="d7f63-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d7f63-113">Requirement</span></span> | <span data-ttu-id="d7f63-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f63-114">Value</span></span> |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f63-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f63-115">Value</span></span> | <span data-ttu-id="d7f63-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d7f63-116">Description</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="d7f63-117">0</span><span class="sxs-lookup"><span data-stu-id="d7f63-117">0</span></span>     | <span data-ttu-id="d7f63-118">Все биты для среза находятся в соответствующем буфере данных битовый поток.</span><span class="sxs-lookup"><span data-stu-id="d7f63-118">All bits for the slice are located within the corresponding bitstream data buffer.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="d7f63-119">1</span><span class="sxs-lookup"><span data-stu-id="d7f63-119">1</span></span>     | <span data-ttu-id="d7f63-120">Буфер данных битовый поток содержит начало среза, но не весь срез, так как буфер полон.</span><span class="sxs-lookup"><span data-stu-id="d7f63-120">The bitstream data buffer contains the start of the slice, but not the entire slice, because the buffer is full.</span></span>                                                                                                                                        |
| <span data-ttu-id="d7f63-121">2</span><span class="sxs-lookup"><span data-stu-id="d7f63-121">2</span></span>     | <span data-ttu-id="d7f63-122">Буфер данных битовый поток содержит конец среза.</span><span class="sxs-lookup"><span data-stu-id="d7f63-122">The bitstream data buffer contains the end of the slice.</span></span> <span data-ttu-id="d7f63-123">Он не содержит начало среза, так как начало среза находится в предыдущем буфере данных битовый поток.</span><span class="sxs-lookup"><span data-stu-id="d7f63-123">It does not contain the start of the slice, because the start of the slice was located in the previous bitstream data buffer.</span></span>                                                                  |
| <span data-ttu-id="d7f63-124">3</span><span class="sxs-lookup"><span data-stu-id="d7f63-124">3</span></span>     | <span data-ttu-id="d7f63-125">Буфер данных битовый поток не содержит начало среза, так как начало среза было найдено в предыдущем буфере данных битовый поток и не содержит конца среза, так как текущий буфер данных битовый поток также заполнен.</span><span class="sxs-lookup"><span data-stu-id="d7f63-125">The bitstream data buffer does not contain the start of the slice because the start of the slice was located in the previous bitstream data buffer and it does not contain the end of the slice becuase the current bitstream data buffer is also full.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7f63-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7f63-126">Remarks</span></span>

<span data-ttu-id="d7f63-127">**Дксва \_ Параметр срез \_ HEVC \_ Short** содержит данные элемента управления среза, которые передаются аппаратному ускорителю с хост-программного декодера.</span><span class="sxs-lookup"><span data-stu-id="d7f63-127">**DXVA\_Slice\_HEVC\_Short** contains slice control data which is passed to the hardware accelerator from the host software decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f63-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d7f63-128">Requirements</span></span>



| <span data-ttu-id="d7f63-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d7f63-129">Requirement</span></span> | <span data-ttu-id="d7f63-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d7f63-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d7f63-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7f63-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f63-132">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7f63-132">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d7f63-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7f63-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f63-134">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7f63-134">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d7f63-135">Header</span><span class="sxs-lookup"><span data-stu-id="d7f63-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f63-136"><dt>Дксва. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f63-136"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f63-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7f63-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f63-138">Структуры Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7f63-138">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




