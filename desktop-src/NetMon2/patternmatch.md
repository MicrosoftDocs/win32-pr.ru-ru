---
description: Структура ПАТТЕРНМАТЧ определяет элементы шаблона, используемые для вычисления кадра.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Структура ПАТТЕРНМАТЧ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998782"
---
# <a name="patternmatch-structure"></a><span data-ttu-id="9f3e9-103">Структура ПАТТЕРНМАТЧ</span><span class="sxs-lookup"><span data-stu-id="9f3e9-103">PATTERNMATCH structure</span></span>

<span data-ttu-id="9f3e9-104">Структура **паттернматч** определяет элементы шаблона, используемые для вычисления кадра.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-104">The **PATTERNMATCH** structure defines pattern elements used to evaluate a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f3e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f3e9-105">Syntax</span></span>


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a><span data-ttu-id="9f3e9-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9f3e9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f3e9-107">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="9f3e9-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9f3e9-108">Флаги соответствия шаблону:</span><span class="sxs-lookup"><span data-stu-id="9f3e9-108">Pattern match flags:</span></span>



| <span data-ttu-id="9f3e9-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9f3e9-109">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="9f3e9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9f3e9-110">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <span data-ttu-id="9f3e9-111"><dt>**Шаблон \_ \_Флаги соответствия \_ не**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="9f3e9-111"><dt>**PATTERN\_MATCH\_FLAGS\_NOT**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="9f3e9-112">Если этот флажок установлен, этот флаг оставляет кадры, в которых отсутствует указанный шаблон, в нужном месте.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-112">When set, this flag retains frames that lack the specified pattern in the proper spot.</span></span><br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <span data-ttu-id="9f3e9-113"><dt>**Шаблон \_ \_Флаг соответствия \_ \_ указанному порту**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="9f3e9-113"><dt>**PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="9f3e9-114">Поиск значения номера порта.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-114">Seeks a port number value.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="9f3e9-115">**оффсетбасис**</span><span class="sxs-lookup"><span data-stu-id="9f3e9-115">**OffsetBasis**</span></span>
</dt> <dd>

<span data-ttu-id="9f3e9-116">Типы смещения, которые могут быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="9f3e9-116">Types of offset, which can be one of the following:</span></span>



| <span data-ttu-id="9f3e9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9f3e9-117">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="9f3e9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9f3e9-118">Meaning</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <span data-ttu-id="9f3e9-119"><dt>**\_Базис по смещению \_ относительно \_ \_ рамки**</dt></span><span class="sxs-lookup"><span data-stu-id="9f3e9-119"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_FRAME**</dt></span></span> </dl>                                         | <span data-ttu-id="9f3e9-120">Задает смещение в байтах относительно начала кадра.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-120">Sets an offset, in bytes, relative to start of the frame.</span></span><br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <span data-ttu-id="9f3e9-121"><dt>**\_основание смещения \_ относительно \_ \_ действующего \_ протокола**</dt></span><span class="sxs-lookup"><span data-stu-id="9f3e9-121"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="9f3e9-122">Задает смещение в байтах относительно начала указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-122">Sets an offset, in bytes, relative to the start of the referenced protocol.</span></span><br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <span data-ttu-id="9f3e9-123"><dt>**\_Базис по смещению \_ относительно \_ \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="9f3e9-123"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IPX**</dt></span></span> </dl>                                               | <span data-ttu-id="9f3e9-124">Задает смещение (в байтах) только относительно IPX.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-124">Sets an offset, in bytes, only relative to IPX.</span></span><br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <span data-ttu-id="9f3e9-125"><dt>**\_Базис по смещению \_ относительно \_ \_ IP**</dt></span><span class="sxs-lookup"><span data-stu-id="9f3e9-125"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IP**</dt></span></span> </dl>                                                  | <span data-ttu-id="9f3e9-126">Задает смещение в байтах только относительно IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-126">Sets an offset, in bytes, only relative to IP.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="9f3e9-127">**порт**.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-127">**Port**</span></span>
</dt> <dd>

<span data-ttu-id="9f3e9-128">Значение порта, если оно указано.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-128">Port value, if specified.</span></span>

</dd> <dt>

<span data-ttu-id="9f3e9-129">**Offset**</span><span class="sxs-lookup"><span data-stu-id="9f3e9-129">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="9f3e9-130">Смещение в байтах относительно **оффсетбасис**.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-130">The offset, in bytes, relative to the **OffsetBasis**.</span></span>

</dd> <dt>

<span data-ttu-id="9f3e9-131">**Длина**</span><span class="sxs-lookup"><span data-stu-id="9f3e9-131">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="9f3e9-132">Длина сопоставленного шаблона.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-132">Length of the matched pattern.</span></span>

</dd> <dt>

<span data-ttu-id="9f3e9-133">**паттернтоматч**</span><span class="sxs-lookup"><span data-stu-id="9f3e9-133">**PatternToMatch**</span></span>
</dt> <dd>

<span data-ttu-id="9f3e9-134">Шаблон для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-134">Pattern to match.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f3e9-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f3e9-135">Remarks</span></span>

<span data-ttu-id="9f3e9-136">Эта структура используется для создания фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="9f3e9-136">This structure is used to construct a capture filter.</span></span> <span data-ttu-id="9f3e9-137">Дополнительные сведения о реализации этой структуры см. в разделе [фильтры записи](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="9f3e9-137">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

<span data-ttu-id="9f3e9-138">Фильтр записи может содержать до четырех структур **паттернматч** .</span><span class="sxs-lookup"><span data-stu-id="9f3e9-138">A capture filter can contain up to four **PATTERNMATCH** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f3e9-139">Требования</span><span class="sxs-lookup"><span data-stu-id="9f3e9-139">Requirements</span></span>



| <span data-ttu-id="9f3e9-140">Требование</span><span class="sxs-lookup"><span data-stu-id="9f3e9-140">Requirement</span></span> | <span data-ttu-id="9f3e9-141">Значение</span><span class="sxs-lookup"><span data-stu-id="9f3e9-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9f3e9-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f3e9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9f3e9-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f3e9-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9f3e9-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f3e9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9f3e9-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f3e9-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9f3e9-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f3e9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f3e9-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f3e9-147"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f3e9-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f3e9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f3e9-149">каптурефилтер</span><span class="sxs-lookup"><span data-stu-id="9f3e9-149">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




