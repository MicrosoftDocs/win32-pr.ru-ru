---
description: Структура набора определяет набор значений.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: ЗАДАТЬ структуру (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264508"
---
# <a name="set-structure"></a><span data-ttu-id="c14a2-103">ЗАДАТЬ структуру</span><span class="sxs-lookup"><span data-stu-id="c14a2-103">SET structure</span></span>

<span data-ttu-id="c14a2-104">Структура **набора** определяет набор значений.</span><span class="sxs-lookup"><span data-stu-id="c14a2-104">The **SET** structure defines a set of values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c14a2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c14a2-105">Syntax</span></span>


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a><span data-ttu-id="c14a2-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c14a2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c14a2-107">**нентриес**</span><span class="sxs-lookup"><span data-stu-id="c14a2-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-108">Общее число записей в наборе.</span><span class="sxs-lookup"><span data-stu-id="c14a2-108">Total number of entries in a set.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-109">**лпбитетабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-109">**lpByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-110">Указатель на массив БАЙТовых значений.</span><span class="sxs-lookup"><span data-stu-id="c14a2-110">Pointer to an array of BYTE values.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-111">**лпвордтабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-111">**lpWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-112">Указатель на массив значений слов.</span><span class="sxs-lookup"><span data-stu-id="c14a2-112">Pointer to an array of WORD values.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-113">**лпдвордтабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-113">**lpDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-114">Указатель на массив значений типа DWORD.</span><span class="sxs-lookup"><span data-stu-id="c14a2-114">Pointer to an array of DWORD values.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-115">**лпларжеинттабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-115">**lpLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-116">Указатель на массив структур [ларжеинт](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="c14a2-116">Pointer to an array of [LARGEINT](largeint.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-117">**лпсистемтиметабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-117">**lpSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-118">Указатель на массив значений SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="c14a2-118">Pointer to an array of SYSTEMTIME values.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-119">**лплабеледбитетабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-119">**lpLabeledByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-120">Указатель на массив с [помеченными структурами \_ байтов](labeled-byte.md) .</span><span class="sxs-lookup"><span data-stu-id="c14a2-120">Pointer to an array of [LABELED\_BYTE](labeled-byte.md) structures.</span></span> <span data-ttu-id="c14a2-121">Каждая структура **\_ байтов с меткой** определяет значение и метку.</span><span class="sxs-lookup"><span data-stu-id="c14a2-121">Each **LABELED\_BYTE** structure defines a value and label.</span></span> <span data-ttu-id="c14a2-122">Сетевой монитор отображает метку, если находит соответствующее значение в пакете протокола.</span><span class="sxs-lookup"><span data-stu-id="c14a2-122">Network Monitor displays a label if it finds a corresponding value in the protocol packet.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-123">**лплабеледвордтабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-123">**lpLabeledWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-124">Указатель на массив структурных [ \_ слов с метками](labeled-word.md) , определяющих набор значений и меток слов.</span><span class="sxs-lookup"><span data-stu-id="c14a2-124">Pointer to an array of [LABELED\_WORD](labeled-word.md) structures that define a set of WORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-125">**лплабеледдвордтабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-125">**lpLabeledDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-126">Указатель на массив структур [с меткой \_ типа DWORD](labeled-dword.md) , который определяет набор значений и меток DWORD.</span><span class="sxs-lookup"><span data-stu-id="c14a2-126">Pointer to an array of [LABELED\_DWORD](labeled-dword.md) structures that define a set of DWORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-127">**лплабеледларжеинттабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-127">**lpLabeledLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-128">Указатель на массив с [помеченными \_ ларжеинт](labeled-largeint.md) структурами, которые ОПРЕДЕЛЯЮТ набор значений ларжеинт и меток.</span><span class="sxs-lookup"><span data-stu-id="c14a2-128">Pointer to an array of [LABELED\_LARGEINT](labeled-largeint.md) structures that define a set of LARGEINT values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-129">**лплабеледсистемтиметабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-129">**lpLabeledSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-130">Указатель на массив структур [с меткой \_ SYSTEMTIME](labeled-systemtime.md) , определяющих набор системных значений и меток.</span><span class="sxs-lookup"><span data-stu-id="c14a2-130">Pointer to an array of [LABELED\_SYSTEMTIME](labeled-systemtime.md) structures that define a set of SYSTEM values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-131">**лплабеледбит**</span><span class="sxs-lookup"><span data-stu-id="c14a2-131">**lpLabeledBit**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-132">Указатель на массив [ \_ битовых структур с метками](labeled-bit.md) , ОПРЕДЕЛЯЮЩих набор битовых пар с метками.</span><span class="sxs-lookup"><span data-stu-id="c14a2-132">Pointer to an array of [LABELED\_BIT](labeled-bit.md) structures that define a set of labeled BIT pairs.</span></span> <span data-ttu-id="c14a2-133">Каждый бит может указывать две метки для каждого состояния бита (0 или 1).</span><span class="sxs-lookup"><span data-stu-id="c14a2-133">Each BIT can specify two labels   one label for each state (0 or 1) of the BIT.</span></span>

</dd> <dt>

<span data-ttu-id="c14a2-134">**лпвоидтабле**</span><span class="sxs-lookup"><span data-stu-id="c14a2-134">**lpVoidTable**</span></span>
</dt> <dd>

<span data-ttu-id="c14a2-135">Указатель на массив значений.</span><span class="sxs-lookup"><span data-stu-id="c14a2-135">Pointer to an array of values.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c14a2-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c14a2-136">Remarks</span></span>

<span data-ttu-id="c14a2-137">Структура **набора** используется для определения набора данных сравнения, которые сетевой монитор могут использовать для интерпретации значения свойства в пакете протокола.</span><span class="sxs-lookup"><span data-stu-id="c14a2-137">The **SET** structure is used to define a set of comparison data that Network Monitor can use to interpret the value of a property in a protocol packet.</span></span> <span data-ttu-id="c14a2-138">Если требуется набор данных сравнения, указатель на структуру **Set** указывается в элементе **лпсет** структуры [PROPERTYINFO](propertyinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c14a2-138">When a set of comparison data is required, a pointer to the **SET** structure is specified in the **lpSet** member of the [PROPERTYINFO](propertyinfo.md) structure.</span></span>

<span data-ttu-id="c14a2-139">Библиотека DLL средства синтаксического анализа может предоставлять набор значений и метку.</span><span class="sxs-lookup"><span data-stu-id="c14a2-139">The parser DLL can provide a value set and a label set.</span></span> <span data-ttu-id="c14a2-140">Член **объединения** , выбранный в **наборе** , указывает на массив структур, определяющих каждый элемент набора.</span><span class="sxs-lookup"><span data-stu-id="c14a2-140">The member of the **UNION** that you select in a **SET** structure points to an array of structures that define each member of a set.</span></span>

-   <span data-ttu-id="c14a2-141">Набор значений</span><span class="sxs-lookup"><span data-stu-id="c14a2-141">Value set</span></span>

    <span data-ttu-id="c14a2-142">Набор значений используется, если требуется, чтобы сетевой монитор включить индикатор in-Set или unin-Set со значением, найденным в пакете протокола.</span><span class="sxs-lookup"><span data-stu-id="c14a2-142">A value set is used when you want Network Monitor to include an in-set or not-in-set indicator with the value found in the protocol packet.</span></span> <span data-ttu-id="c14a2-143">Например, если задан параметр DWORD, сетевой монитор отображает метку для каждого значения DWORD, найденного в пакете протокола, указывая, что параметр DWORD имеет значение или не указан в наборе.</span><span class="sxs-lookup"><span data-stu-id="c14a2-143">For example, if a DWORD set is specified, Network Monitor displays a label for each DWORD value found in the protocol packet, indicating that the DWORD is or is not specified in the set.</span></span>

    <span data-ttu-id="c14a2-144">Набор значений может основываться на типах данных BYTE, WORD, DWORD, ЛАРЖЕИНТ и SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="c14a2-144">A value set can be based on BYTE, WORD, DWORD, LARGEINT, and SYSTEMTIME data types.</span></span>

-   <span data-ttu-id="c14a2-145">Набор меток</span><span class="sxs-lookup"><span data-stu-id="c14a2-145">Label set</span></span>

    <span data-ttu-id="c14a2-146">Набор меток используется, если требуется, чтобы сетевой монитор отображала определенная пользователем метка вместо значений свойств, указанных в наборе.</span><span class="sxs-lookup"><span data-stu-id="c14a2-146">A label set is used when you want Network Monitor to display a user-defined label instead of the property values specified in a set.</span></span>

    <span data-ttu-id="c14a2-147">Набор меток может быть основан на парах BYTE, WORD, DWORD, ЛАРЖЕИНТ, SYSTEMTIME и BIT меток.</span><span class="sxs-lookup"><span data-stu-id="c14a2-147">A label set can be based on BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME and BIT label pairs.</span></span>

## <a name="requirements"></a><span data-ttu-id="c14a2-148">Требования</span><span class="sxs-lookup"><span data-stu-id="c14a2-148">Requirements</span></span>



| <span data-ttu-id="c14a2-149">Требование</span><span class="sxs-lookup"><span data-stu-id="c14a2-149">Requirement</span></span> | <span data-ttu-id="c14a2-150">Значение</span><span class="sxs-lookup"><span data-stu-id="c14a2-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c14a2-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c14a2-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c14a2-152">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c14a2-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c14a2-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c14a2-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c14a2-154">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c14a2-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c14a2-155">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c14a2-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="c14a2-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c14a2-156"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c14a2-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c14a2-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c14a2-158">бит с МЕТКОЙ \_</span><span class="sxs-lookup"><span data-stu-id="c14a2-158">LABELED\_BIT</span></span>](labeled-bit.md)
</dt> <dt>

[<span data-ttu-id="c14a2-159">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="c14a2-159">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




