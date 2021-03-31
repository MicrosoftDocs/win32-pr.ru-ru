---
title: Функция Гллинестиппле (GL. h)
description: Функция Гллинестиппле указывает шаблон Line стиппле.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- Функция Гллинестиппле OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801000"
---
# <a name="gllinestipple-function"></a><span data-ttu-id="13f8e-104">Функция Гллинестиппле</span><span class="sxs-lookup"><span data-stu-id="13f8e-104">glLineStipple function</span></span>

<span data-ttu-id="13f8e-105">Функция **гллинестиппле** указывает шаблон Line стиппле.</span><span class="sxs-lookup"><span data-stu-id="13f8e-105">The **glLineStipple** function specifies the line stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f8e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13f8e-106">Syntax</span></span>


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a><span data-ttu-id="13f8e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="13f8e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f8e-108">*многофакторной*</span><span class="sxs-lookup"><span data-stu-id="13f8e-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="13f8e-109">Множитель для каждого бита в шаблоне стиппле линии.</span><span class="sxs-lookup"><span data-stu-id="13f8e-109">A multiplier for each bit in the line stipple pattern.</span></span> <span data-ttu-id="13f8e-110">Например, если *Коэффициент* равен 3, то каждый бит в шаблоне будет использоваться три раза до того, как будет использован следующий бит в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="13f8e-110">If *factor* is 3, for example, each bit in the pattern will be used three times before the next bit in the pattern is used.</span></span> <span data-ttu-id="13f8e-111">Параметр *коэффициента* задается в виде фиксации по диапазону \[ 1, 256 \] и по умолчанию равным единице.</span><span class="sxs-lookup"><span data-stu-id="13f8e-111">The *factor* parameter is clamped to the range \[1, 256\] and defaults to one.</span></span>

</dd> <dt>

<span data-ttu-id="13f8e-112">*pattern*</span><span class="sxs-lookup"><span data-stu-id="13f8e-112">*pattern*</span></span> 
</dt> <dd>

<span data-ttu-id="13f8e-113">16-разрядное целое число, битовый шаблон которого определяет, какие фрагменты линии будут отображаться при растрировании строки.</span><span class="sxs-lookup"><span data-stu-id="13f8e-113">A 16-bit integer whose bit pattern determines which fragments of a line will be drawn when the line is rasterized.</span></span> <span data-ttu-id="13f8e-114">Сначала используется нулевой разряд, а шаблон по умолчанию — все.</span><span class="sxs-lookup"><span data-stu-id="13f8e-114">Bit zero is used first, and the default pattern is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f8e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13f8e-115">Return value</span></span>

<span data-ttu-id="13f8e-116">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="13f8e-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13f8e-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="13f8e-117">Error codes</span></span>

<span data-ttu-id="13f8e-118">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="13f8e-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="13f8e-119">Имя</span><span class="sxs-lookup"><span data-stu-id="13f8e-119">Name</span></span>                                                                                                  | <span data-ttu-id="13f8e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="13f8e-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13f8e-121"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13f8e-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="13f8e-122">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="13f8e-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="13f8e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13f8e-123">Remarks</span></span>

<span data-ttu-id="13f8e-124">Функция **гллинестиппле** указывает шаблон Line стиппле.</span><span class="sxs-lookup"><span data-stu-id="13f8e-124">The **glLineStipple** function specifies the line stipple pattern.</span></span> <span data-ttu-id="13f8e-125">Line стипплинг маскирует определенные фрагменты, созданные с помощью растрирования; Эти фрагменты не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="13f8e-125">Line stippling masks out certain fragments produced by rasterization; those fragments will not be drawn.</span></span> <span data-ttu-id="13f8e-126">Маскирование достигается с помощью трех параметров: 16-разрядный *шаблон стиппле Line,* *Коэффициент* числа повторов и целочисленный стиппле счетчиков *s*.</span><span class="sxs-lookup"><span data-stu-id="13f8e-126">The masking is achieved by using three parameters: the 16-bit line stipple pattern *pattern*, the repeat count *factor*, and an integer stipple counter *s*.</span></span>

<span data-ttu-id="13f8e-127">Счетчик *s* сбрасывается в ноль каждый раз, когда вызывается [**глбегин**](glbegin.md) , и до создания каждого сегмента строки **глбегин**(GL \_ Lines)/**гленд** Sequence.</span><span class="sxs-lookup"><span data-stu-id="13f8e-127">Counter *s* is reset to zero whenever [**glBegin**](glbegin.md) is called, and before each line segment of a **glBegin**(GL\_LINES)/**glEnd** sequence is generated.</span></span> <span data-ttu-id="13f8e-128">Он увеличивается после создания *каждого фрагмента* сегмента линии с псевдонимом или после создания каждого фрагмента *строки толщины* линии.</span><span class="sxs-lookup"><span data-stu-id="13f8e-128">It is incremented after each fragment of a unit width aliased line segment is generated, or after each *i* fragments of an *i* width line segment are generated.</span></span> <span data-ttu-id="13f8e-129">Фрагменты *i* , связанные с *Count, замаскированы, если* бит *шаблона* (  /  *Коэффициент* s) MOD 16 равен нулю.</span><span class="sxs-lookup"><span data-stu-id="13f8e-129">The *i* fragments associated with count *s* are masked out if *pattern* bit (*s* / *factor*) mod 16 is zero.</span></span> <span data-ttu-id="13f8e-130">В противном случае эти фрагменты отправляются в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="13f8e-130">Otherwise these fragments are sent to the framebuffer.</span></span> <span data-ttu-id="13f8e-131">Нулевой бит *шаблона* является наименее значащим битом.</span><span class="sxs-lookup"><span data-stu-id="13f8e-131">Bit zero of *pattern* is the least significant bit.</span></span>

<span data-ttu-id="13f8e-132">Сглаженные линии обрабатываются как последовательность прямоугольников *толщины* в 1 – 1 в целях стипплинг.</span><span class="sxs-lookup"><span data-stu-id="13f8e-132">Antialiased lines are treated as a sequence of 1x *width* rectangles for purposes of stippling.</span></span> <span data-ttu-id="13f8e-133">Прямоугольники *с* растровым изображением или не основаны на правиле фрагментов, описанных для строк с псевдонимами. Он учитывает прямоугольники, а не группы фрагментов.</span><span class="sxs-lookup"><span data-stu-id="13f8e-133">Rectangle *s* is rasterized or not based on the fragment rule described for aliased lines; it counts rectangles rather than groups of fragments.</span></span>

<span data-ttu-id="13f8e-134">Строка стипплинг включена или отключена с помощью [**гленабле**](glenable.md) и **глдисабле** с аргументом GL \_ Line \_ стиппле.</span><span class="sxs-lookup"><span data-stu-id="13f8e-134">Line stippling is enabled or disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_STIPPLE.</span></span> <span data-ttu-id="13f8e-135">Если этот параметр включен, применяется шаблон Line стиппле, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="13f8e-135">When enabled, the line stipple pattern is applied as described above.</span></span> <span data-ttu-id="13f8e-136">Если этот параметр отключен, это так, как если бы шаблон был все.</span><span class="sxs-lookup"><span data-stu-id="13f8e-136">When disabled, it is as if the pattern were all ones.</span></span> <span data-ttu-id="13f8e-137">Изначально строка стипплинг отключена.</span><span class="sxs-lookup"><span data-stu-id="13f8e-137">Initially, line stippling is disabled.</span></span>

<span data-ttu-id="13f8e-138">Следующие функции извлекают сведения, относящиеся к **гллинестиппле**:</span><span class="sxs-lookup"><span data-stu-id="13f8e-138">The following functions retrieve information related to **glLineStipple**:</span></span>

<span data-ttu-id="13f8e-139">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Line \_ стиппле \_ pattern</span><span class="sxs-lookup"><span data-stu-id="13f8e-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_STIPPLE\_PATTERN</span></span>

<span data-ttu-id="13f8e-140">**глжет** с аргументом GL \_ Line \_ стиппле \_ Повтор</span><span class="sxs-lookup"><span data-stu-id="13f8e-140">**glGet** with argument GL\_LINE\_STIPPLE\_REPEAT</span></span>

<span data-ttu-id="13f8e-141">[**глисенаблед**](glisenabled.md) с аргументом GL \_ Line \_ стиппле</span><span class="sxs-lookup"><span data-stu-id="13f8e-141">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="13f8e-142">Требования</span><span class="sxs-lookup"><span data-stu-id="13f8e-142">Requirements</span></span>



| <span data-ttu-id="13f8e-143">Требование</span><span class="sxs-lookup"><span data-stu-id="13f8e-143">Requirement</span></span> | <span data-ttu-id="13f8e-144">Значение</span><span class="sxs-lookup"><span data-stu-id="13f8e-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13f8e-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13f8e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="13f8e-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="13f8e-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="13f8e-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13f8e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="13f8e-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="13f8e-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13f8e-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="13f8e-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="13f8e-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="13f8e-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="13f8e-151">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13f8e-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="13f8e-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13f8e-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="13f8e-153">DLL</span><span class="sxs-lookup"><span data-stu-id="13f8e-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13f8e-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13f8e-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f8e-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13f8e-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f8e-156">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="13f8e-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="13f8e-157">**гленд**</span><span class="sxs-lookup"><span data-stu-id="13f8e-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="13f8e-158">**гллиневидс**</span><span class="sxs-lookup"><span data-stu-id="13f8e-158">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="13f8e-159">**глполигонстиппле**</span><span class="sxs-lookup"><span data-stu-id="13f8e-159">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





