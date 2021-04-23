---
description: Структура КАПТУРЕФИЛТЕР содержит данные фильтра записи.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Структура КАПТУРЕФИЛТЕР (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663648"
---
# <a name="capturefilter-structure"></a><span data-ttu-id="2e39f-103">Структура КАПТУРЕФИЛТЕР</span><span class="sxs-lookup"><span data-stu-id="2e39f-103">CAPTUREFILTER structure</span></span>

<span data-ttu-id="2e39f-104">Структура **каптурефилтер** содержит данные фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="2e39f-104">The **CAPTUREFILTER** structure contains capture filter data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e39f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e39f-105">Syntax</span></span>


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a><span data-ttu-id="2e39f-106">Члены</span><span class="sxs-lookup"><span data-stu-id="2e39f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e39f-107">**филтерфлагс**</span><span class="sxs-lookup"><span data-stu-id="2e39f-107">**FilterFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-108">Флаги, описывающие содержимое фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="2e39f-108">Flags that describe the contents of the capture filter.</span></span>



| <span data-ttu-id="2e39f-109">Значение</span><span class="sxs-lookup"><span data-stu-id="2e39f-109">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="2e39f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="2e39f-110">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <span data-ttu-id="2e39f-111"><dt>**Каптурефилтер \_ ФЛАГи \_ включают \_ все \_ SAPS**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="2e39f-111"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS**</dt> <dt>0x0001</dt></span></span> </dl>       | <span data-ttu-id="2e39f-112">Включает все SAPs в качестве допустимых кадров.</span><span class="sxs-lookup"><span data-stu-id="2e39f-112">Includes all SAPs as acceptable frames.</span></span><br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <span data-ttu-id="2e39f-113"><dt>**Каптурефилтер \_ ФЛАГи \_ включают \_ все \_ ETYPE**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="2e39f-113"><dt>**CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="2e39f-114">Включите все ETYPE в качестве допустимых кадров.</span><span class="sxs-lookup"><span data-stu-id="2e39f-114">Include all Etypes as acceptable frames.</span></span><br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <span data-ttu-id="2e39f-115"><dt>**Каптурефилтер \_ ПОМЕЧАЕТ \_ \_ только локальные**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="2e39f-115"><dt>**CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY**</dt> <dt>0x0008</dt></span></span> </dl>                          | <span data-ttu-id="2e39f-116">Без режима P-Mode</span><span class="sxs-lookup"><span data-stu-id="2e39f-116">No P-mode</span></span><br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <span data-ttu-id="2e39f-117"><dt>**Каптурефилтер \_ ФЛАГи \_ сохраняют \_ необработанные**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="2e39f-117"><dt>**CAPTUREFILTER\_FLAGS\_KEEP\_RAW**</dt> <dt>0x0020</dt></span></span> </dl>                                | <span data-ttu-id="2e39f-118">Не используйте кадры MAC SMT и Token Ring.</span><span class="sxs-lookup"><span data-stu-id="2e39f-118">Keep SMT and token ring MAC frames.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="2e39f-119">**лпсаптабле**</span><span class="sxs-lookup"><span data-stu-id="2e39f-119">**lpSapTable**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-120">Указатель на массив значений SAP.</span><span class="sxs-lookup"><span data-stu-id="2e39f-120">Pointer to an array of SAP values.</span></span> <span data-ttu-id="2e39f-121">Этот элемент указывает значения SAP, допустимые для передачи в драйвер.</span><span class="sxs-lookup"><span data-stu-id="2e39f-121">This member indicates the SAP values that are valid to pass to the driver.</span></span> <span data-ttu-id="2e39f-122">Если \_ Флаги каптурефилтер \_ включают \_ все \_ SAPS, это становится списком исключений (включая все SAPS, Кроме этих).</span><span class="sxs-lookup"><span data-stu-id="2e39f-122">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_SAPS is set, this becomes an exception list (include all SAPS except these).</span></span>

</dd> <dt>

<span data-ttu-id="2e39f-123">**лпетипетабле**</span><span class="sxs-lookup"><span data-stu-id="2e39f-123">**lpEtypeTable**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-124">Указатель на массив значений etype.</span><span class="sxs-lookup"><span data-stu-id="2e39f-124">Pointer to an array of Etype values.</span></span> <span data-ttu-id="2e39f-125">Это означает, что значения ETYPE, допустимые для передачи в драйвер.</span><span class="sxs-lookup"><span data-stu-id="2e39f-125">This indicates those Etype values that are valid to pass to the driver.</span></span> <span data-ttu-id="2e39f-126">Если \_ установлены флаги каптурефилтер \_ \_ \_ , то он становится списком исключений (включая все типы ETYPE, Кроме этих).</span><span class="sxs-lookup"><span data-stu-id="2e39f-126">If CAPTUREFILTER\_FLAGS\_INCLUDE\_ALL\_ETYPES is set, this becomes an exception list (include all Etypes except these).</span></span>

</dd> <dt>

<span data-ttu-id="2e39f-127">**нсапс**</span><span class="sxs-lookup"><span data-stu-id="2e39f-127">**nSaps**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-128">Число SAPs в таблице SAP.</span><span class="sxs-lookup"><span data-stu-id="2e39f-128">Number of SAPs in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="2e39f-129">**нетипес**</span><span class="sxs-lookup"><span data-stu-id="2e39f-129">**nEtypes**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-130">Число ETYPE в таблице etype.</span><span class="sxs-lookup"><span data-stu-id="2e39f-130">Number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="2e39f-131">**аддресстабле**</span><span class="sxs-lookup"><span data-stu-id="2e39f-131">**AddressTable**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-132">Имя таблицы адресов.</span><span class="sxs-lookup"><span data-stu-id="2e39f-132">Name of the address table.</span></span>

</dd> <dt>

<span data-ttu-id="2e39f-133">**FilterExpression**</span><span class="sxs-lookup"><span data-stu-id="2e39f-133">**FilterExpression**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-134">Структура выражения.</span><span class="sxs-lookup"><span data-stu-id="2e39f-134">An EXPRESSION structure.</span></span> <span data-ttu-id="2e39f-135">Он содержит часть фильтра записи, соответствующую шаблону.</span><span class="sxs-lookup"><span data-stu-id="2e39f-135">This contains the pattern match portion of the capture filter.</span></span>

</dd> <dt>

<span data-ttu-id="2e39f-136">**Триггер**</span><span class="sxs-lookup"><span data-stu-id="2e39f-136">**Trigger**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-137">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="2e39f-137">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2e39f-138">**нфрамебитестокопи**</span><span class="sxs-lookup"><span data-stu-id="2e39f-138">**nFrameBytesToCopy**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-139">Если этот элемент не равен 0, то он указывает, сколько байтов следует удерживать для каждого полученного кадра.</span><span class="sxs-lookup"><span data-stu-id="2e39f-139">If this member is not 0, then it specifies how many bytes to keep of each frame received.</span></span> <span data-ttu-id="2e39f-140">Если это 0, сохраните весь кадр целиком.</span><span class="sxs-lookup"><span data-stu-id="2e39f-140">If it is 0, then keep the whole frame.</span></span>

</dd> <dt>

<span data-ttu-id="2e39f-141">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="2e39f-141">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="2e39f-142">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="2e39f-142">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e39f-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e39f-143">Remarks</span></span>

<span data-ttu-id="2e39f-144">Сочетание флагов, значений и выражений определяет, какие кадры будут переданы драйвером, использующим эти данные структуры.</span><span class="sxs-lookup"><span data-stu-id="2e39f-144">The combination of flags, values, and expressions determine which frames will be passed by the driver that uses this structure data.</span></span> <span data-ttu-id="2e39f-145">Дополнительные сведения о реализации структуры **каптурефилтер** см. в разделе [фильтры записи](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="2e39f-145">For more information about implementing a **CAPTUREFILTER** structure, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e39f-146">Требования</span><span class="sxs-lookup"><span data-stu-id="2e39f-146">Requirements</span></span>



| <span data-ttu-id="2e39f-147">Требование</span><span class="sxs-lookup"><span data-stu-id="2e39f-147">Requirement</span></span> | <span data-ttu-id="2e39f-148">Значение</span><span class="sxs-lookup"><span data-stu-id="2e39f-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2e39f-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e39f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="2e39f-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e39f-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2e39f-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e39f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="2e39f-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2e39f-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2e39f-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2e39f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e39f-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e39f-154"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e39f-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e39f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e39f-156">аддресстабле</span><span class="sxs-lookup"><span data-stu-id="2e39f-156">ADDRESSTABLE</span></span>](addresstable.md)
</dt> <dt>

[<span data-ttu-id="2e39f-157">аддресспаир</span><span class="sxs-lookup"><span data-stu-id="2e39f-157">ADDRESSPAIR</span></span>](addresspair.md)
</dt> <dt>

[<span data-ttu-id="2e39f-158">ВЫРАЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e39f-158">EXPRESSION</span></span>](expression.md)
</dt> <dt>

[<span data-ttu-id="2e39f-159">андексп</span><span class="sxs-lookup"><span data-stu-id="2e39f-159">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="2e39f-160">паттернматч</span><span class="sxs-lookup"><span data-stu-id="2e39f-160">PATTERNMATCH</span></span>](patternmatch.md)
</dt> </dl>

 

 




