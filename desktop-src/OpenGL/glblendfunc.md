---
title: Функция Глблендфунк (GL. h)
description: Функция Глблендфунк задает арифметику пикселей.
ms.assetid: 6756774b-5eef-419a-a653-0b251aed65a0
keywords:
- Функция Глблендфунк OpenGL
topic_type:
- apiref
api_name:
- glBlendFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6300543bbf589c704da6d941bd743f693e0ed5fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681912"
---
# <a name="glblendfunc-function"></a><span data-ttu-id="829c9-104">Функция Глблендфунк</span><span class="sxs-lookup"><span data-stu-id="829c9-104">glBlendFunc function</span></span>

<span data-ttu-id="829c9-105">Функция **глблендфунк** задает арифметику пикселей.</span><span class="sxs-lookup"><span data-stu-id="829c9-105">The **glBlendFunc** function specifies pixel arithmetic.</span></span>

## <a name="syntax"></a><span data-ttu-id="829c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="829c9-106">Syntax</span></span>


```C++
void WINAPI glBlendFunc(
   GLenum sfactor,
   GLenum dfactor
);
```



## <a name="parameters"></a><span data-ttu-id="829c9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="829c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="829c9-108">*сфактор*</span><span class="sxs-lookup"><span data-stu-id="829c9-108">*sfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="829c9-109">Указывает, как вычисляются факторы красного, зеленого, синего и альфа-смешения источника.</span><span class="sxs-lookup"><span data-stu-id="829c9-109">Specifies how the red, green, blue, and alpha source-blending factors are computed.</span></span> <span data-ttu-id="829c9-110">Принимаются девять символьных констант: \_ ноль, GL, ГК \_ , \_ Цвет летнего времени \_ , \_ 1 \_ минус \_ Цвет летнего времени, GL src, GL \_ \_ \_ , ГК, один минус источник альфа, GL ( \_ \_ \_ \_ \_ альфа DST) \_ , GL \_ 1 \_ минус \_ альфа-летнее \_ и GL \_ Исх \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="829c9-110">Nine symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_DST\_COLOR, GL\_ONE\_MINUS\_DST\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, GL\_ONE\_MINUS\_DST\_ALPHA, and GL\_SRC\_ALPHA\_SATURATE.</span></span>

</dd> <dt>

<span data-ttu-id="829c9-111">*дфактор*</span><span class="sxs-lookup"><span data-stu-id="829c9-111">*dfactor*</span></span> 
</dt> <dd>

<span data-ttu-id="829c9-112">Указывает, как будут вычисляться красные, зеленые, синие и Альфа-назначения.</span><span class="sxs-lookup"><span data-stu-id="829c9-112">Specifies how the red, green, blue, and alpha destination-blending factors are computed.</span></span> <span data-ttu-id="829c9-113">Допускается восемь символьных констант: \_ нулевая, GL, \_ 1, GL, \_ GL, \_ \_ один \_ минус цвет src, ГК src, \_ \_ \_ GL, один минус источник альфа, ГК летнего времени, ГК, один \_ \_ \_ \_ \_ \_ \_ \_ \_ минус Альфа- \_ фактор летнего времени \_ .</span><span class="sxs-lookup"><span data-stu-id="829c9-113">Eight symbolic constants are accepted: GL\_ZERO, GL\_ONE, GL\_SRC\_COLOR, GL\_ONE\_MINUS\_SRC\_COLOR, GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA, GL\_DST\_ALPHA, and GL\_ONE\_MINUS\_DST\_ALPHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="829c9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="829c9-114">Return value</span></span>

<span data-ttu-id="829c9-115">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="829c9-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="829c9-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="829c9-116">Error codes</span></span>

<span data-ttu-id="829c9-117">Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="829c9-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="829c9-118">Имя</span><span class="sxs-lookup"><span data-stu-id="829c9-118">Name</span></span>                                                                                                  | <span data-ttu-id="829c9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="829c9-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="829c9-120"><dt>**\_недействительное \_ перечисление GL**</dt></span><span class="sxs-lookup"><span data-stu-id="829c9-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="829c9-121">Значение *сфактор* или *дфактор* не было принято.</span><span class="sxs-lookup"><span data-stu-id="829c9-121">Either *sfactor* or *dfactor* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="829c9-122"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="829c9-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="829c9-123">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="829c9-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="829c9-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="829c9-124">Remarks</span></span>

<span data-ttu-id="829c9-125">В режиме RGB пикселы можно рисовать с помощью функции, которая смешивает входящие (исходные) значения RGBA с значениями RGBA, которые уже находятся в буфера кадров (значения назначения).</span><span class="sxs-lookup"><span data-stu-id="829c9-125">In RGB mode, pixels can be drawn using a function that blends the incoming (source) RGBA values with the RGBA values that are already in the framebuffer (the destination values).</span></span> <span data-ttu-id="829c9-126">По умолчанию смешивание отключено.</span><span class="sxs-lookup"><span data-stu-id="829c9-126">By default, blending is disabled.</span></span> <span data-ttu-id="829c9-127">Используйте [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) с \_ аргументом GL Blend для включения и отключения смешения.</span><span class="sxs-lookup"><span data-stu-id="829c9-127">Use [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the GL\_BLEND argument to enable and disable blending.</span></span>

<span data-ttu-id="829c9-128">Если этот параметр включен, **глблендфунк** определяет операцию смешения.</span><span class="sxs-lookup"><span data-stu-id="829c9-128">When enabled, **glBlendFunc** defines the operation of blending.</span></span> <span data-ttu-id="829c9-129">Параметр *сфактор* указывает, какой из девяти методов используется для масштабирования компонентов исходного цвета.</span><span class="sxs-lookup"><span data-stu-id="829c9-129">The *sfactor* parameter specifies which of nine methods is used to scale the source color components.</span></span> <span data-ttu-id="829c9-130">Параметр *дфактор* указывает, какой из восьми методов используется для масштабирования компонентов целевого цвета.</span><span class="sxs-lookup"><span data-stu-id="829c9-130">The *dfactor* parameter specifies which of eight methods is used to scale the destination color components.</span></span> <span data-ttu-id="829c9-131">В следующей таблице описаны одиннадцать возможных методов.</span><span class="sxs-lookup"><span data-stu-id="829c9-131">The eleven possible methods are described in the following table.</span></span> <span data-ttu-id="829c9-132">Каждый метод определяет четыре коэффициента масштабирования по одному для красного, зеленого, синего и альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="829c9-132">Each method defines four scale factors one each for red, green, blue, and alpha.</span></span>

<span data-ttu-id="829c9-133">В таблице и в последующих уравнениях компоненты исходного и конечного цветов называются (*R*?</span><span class="sxs-lookup"><span data-stu-id="829c9-133">In the table and in subsequent equations, source and destination color components are referred to as (*R*?</span></span> <span data-ttu-id="829c9-134">, *Ж*?</span><span class="sxs-lookup"><span data-stu-id="829c9-134">, *G*?</span></span> <span data-ttu-id="829c9-135">, *Б*?</span><span class="sxs-lookup"><span data-stu-id="829c9-135">, *B*?</span></span> <span data-ttu-id="829c9-136">, *А*?</span><span class="sxs-lookup"><span data-stu-id="829c9-136">, *A*?</span></span> <span data-ttu-id="829c9-137">) и (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span><span class="sxs-lookup"><span data-stu-id="829c9-137">) and (*R*<sub>d</sub> , *G*<sub>d</sub> , *B*<sub>d</sub> , *A*<sub>d</sub> ).</span></span> <span data-ttu-id="829c9-138">Они могут иметь целочисленные значения от 0 до (*k*<sub>r</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), где</span><span class="sxs-lookup"><span data-stu-id="829c9-138">They are understood to have integer values between zero and (*k*<sub>R</sub> , *k*<sub>G</sub> , *k*<sub>R</sub> , *k*<sub>A</sub> ), where</span></span>

<span data-ttu-id="829c9-139">*k*<sub>r</sub> = 2 <sup>m</sup>*r* -1</span><span class="sxs-lookup"><span data-stu-id="829c9-139">*k*<sub>R</sub> = 2 <sup>m</sup>*R* - 1</span></span>

<span data-ttu-id="829c9-140">*k*<sub>g</sub> = 2 <sup>m</sup>*G* -1</span><span class="sxs-lookup"><span data-stu-id="829c9-140">*k*<sub>G</sub> = 2 <sup>m</sup>*G* - 1</span></span>

<span data-ttu-id="829c9-141">*k*<sub>b</sub> = 2 <sup>m</sup>*b* -1</span><span class="sxs-lookup"><span data-stu-id="829c9-141">*k*<sub>B</sub> = 2 <sup>m</sup>*B* - 1</span></span>

<span data-ttu-id="829c9-142">*k*<sub>a</sub> = 2 <sup>м</sup>*a* – 1</span><span class="sxs-lookup"><span data-stu-id="829c9-142">*k*<sub>A</sub> = 2 <sup>m</sup>*A* - 1</span></span>

<span data-ttu-id="829c9-143">и (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) — число красного, зеленого, синего и альфа-битпланес.</span><span class="sxs-lookup"><span data-stu-id="829c9-143">and (*m*<sub>R</sub> , *m*<sub>G</sub> , *m*<sub>B</sub> , *m*<sub>A</sub> ) is the number of red, green, blue, and alpha bitplanes.</span></span>

<span data-ttu-id="829c9-144">Исходные и целевые факторы масштабирования называются (*s*<sub>r</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) и (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>a</sub> ).</span><span class="sxs-lookup"><span data-stu-id="829c9-144">Source and destination scale factors are referred to as (*s*<sub>R</sub> , *s*<sub>G</sub> , *s*<sub>B</sub> , *s*<sub>A</sub> ) and (*d*<sub>R</sub> , *d*<sub>G</sub> , *d*<sub>B</sub> , *d*<sub>A</sub> ).</span></span> <span data-ttu-id="829c9-145">Коэффициенты масштабирования, описанные в таблице (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), представляют либо исходные, либо целевые факторы.</span><span class="sxs-lookup"><span data-stu-id="829c9-145">The scale factors described in the table, denoted (*f*<sub>R</sub> , *f*<sub>G</sub> , *f*<sub>B</sub> , *f*<sub>A</sub> ), represent either source or destination factors.</span></span> <span data-ttu-id="829c9-146">Все коэффициенты масштабирования имеют диапазон \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="829c9-146">All scale factors have range \[0,1\].</span></span>



| <span data-ttu-id="829c9-147">Параметр</span><span class="sxs-lookup"><span data-stu-id="829c9-147">Parameter</span></span>                  | <span data-ttu-id="829c9-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span><span class="sxs-lookup"><span data-stu-id="829c9-148">(*f*<sub>R</sub>  , *f*<sub>G</sub>  , *f*<sub>B</sub>  , *f*<sub>A</sub>  )</span></span>                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="829c9-149">ноль в ГК \_</span><span class="sxs-lookup"><span data-stu-id="829c9-149">GL\_ZERO</span></span>                   | <span data-ttu-id="829c9-150">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="829c9-150">(0,0,0,0)</span></span>                                                                                                                                                    |
| <span data-ttu-id="829c9-151">\_один GL</span><span class="sxs-lookup"><span data-stu-id="829c9-151">GL\_ONE</span></span>                    | <span data-ttu-id="829c9-152">(1, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="829c9-152">(1,1,1,1)</span></span>                                                                                                                                                    |
| <span data-ttu-id="829c9-153">\_Цвет src в GL \_</span><span class="sxs-lookup"><span data-stu-id="829c9-153">GL\_SRC\_COLOR</span></span>             | <span data-ttu-id="829c9-154">(*R*?</span><span class="sxs-lookup"><span data-stu-id="829c9-154">(*R*?</span></span><span data-ttu-id="829c9-155"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="829c9-155"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="829c9-156"> / *k*<sub>ж</sub> , *б*?</span><span class="sxs-lookup"><span data-stu-id="829c9-156"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="829c9-157"> / *k*<sub>б</sub> , *а*?</span><span class="sxs-lookup"><span data-stu-id="829c9-157"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="829c9-158"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-158"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="829c9-159">\_Цвет источника \_ "один за минус" \_ \_</span><span class="sxs-lookup"><span data-stu-id="829c9-159">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="829c9-160">(1, 1, 1, 1)-(*R*?</span><span class="sxs-lookup"><span data-stu-id="829c9-160">(1,1,1,1) - (*R*?</span></span><span data-ttu-id="829c9-161"> / *k*<sub>R</sub> , *G*?</span><span class="sxs-lookup"><span data-stu-id="829c9-161"> / *k*<sub>R</sub> , *G*?</span></span><span data-ttu-id="829c9-162"> / *k*<sub>ж</sub> , *б*?</span><span class="sxs-lookup"><span data-stu-id="829c9-162"> / *k*<sub>G</sub> , *B*?</span></span><span data-ttu-id="829c9-163"> / *k*<sub>б</sub> , *а*?</span><span class="sxs-lookup"><span data-stu-id="829c9-163"> / *k*<sub>B</sub> , *A*?</span></span><span data-ttu-id="829c9-164"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-164"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="829c9-165">\_Цвет летнего времени \_</span><span class="sxs-lookup"><span data-stu-id="829c9-165">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="829c9-166">(*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>B</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-166">(*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="829c9-167">\_один и тот же \_ \_ Цвет периода летнего времени \_</span><span class="sxs-lookup"><span data-stu-id="829c9-167">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="829c9-168">(1, 1, 1, 1)-(*R*<sub>d</sub>  /  *k*<sub>R</sub> , *g*<sub>d</sub>  /  *k*<sub>g</sub> , *b*<sub>d</sub>  /  *k*<sub>B</sub> , *a*<sub>d</sub>  /  *k*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-168">(1,1,1,1) - (*R*<sub>d</sub> / *k*<sub>R</sub> , *G*<sub>d</sub> / *k*<sub>G</sub> , *B*<sub>d</sub> / *k*<sub>B</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="829c9-169">\_альфа- \_ канал ГК src</span><span class="sxs-lookup"><span data-stu-id="829c9-169">GL\_SRC\_ALPHA</span></span>             | <span data-ttu-id="829c9-170">(*A*?</span><span class="sxs-lookup"><span data-stu-id="829c9-170">(*A*?</span></span><span data-ttu-id="829c9-171"> / *а,*<sub></sub> *а*?</span><span class="sxs-lookup"><span data-stu-id="829c9-171"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="829c9-172"> / *а,*<sub></sub> *а*?</span><span class="sxs-lookup"><span data-stu-id="829c9-172"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="829c9-173"> / *а,*<sub></sub> *а*?</span><span class="sxs-lookup"><span data-stu-id="829c9-173"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="829c9-174"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-174"> / *k*<sub>A</sub> )</span></span>                                                         |
| <span data-ttu-id="829c9-175">1-я, ГК, \_ один \_ минус \_ \_ альфа</span><span class="sxs-lookup"><span data-stu-id="829c9-175">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> | <span data-ttu-id="829c9-176">(1, 1, 1, 1) — (*A*?</span><span class="sxs-lookup"><span data-stu-id="829c9-176">(1,1,1,1) - (*A*?</span></span><span data-ttu-id="829c9-177"> / *а,*<sub></sub> *а*?</span><span class="sxs-lookup"><span data-stu-id="829c9-177"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="829c9-178"> / *а,*<sub></sub> *а*?</span><span class="sxs-lookup"><span data-stu-id="829c9-178"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="829c9-179"> / *а,*<sub></sub> *а*?</span><span class="sxs-lookup"><span data-stu-id="829c9-179"> / *k*<sub>A</sub> , *A*?</span></span><span data-ttu-id="829c9-180"> / *k*<sub>A</sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-180"> / *k*<sub>A</sub> )</span></span>                                             |
| <span data-ttu-id="829c9-181">\_альфа- \_ канал летнего времени</span><span class="sxs-lookup"><span data-stu-id="829c9-181">GL\_DST\_ALPHA</span></span>             | <span data-ttu-id="829c9-182">(*A*<sub>d</sub>  /  *k*<sub>а</sub> , *a*<sub>d</sub>  /  *k*<sub>а</sub> , *a*<sub>d</sub>  /  *k*<sub>а</sub> , *a*<sub>d</sub>  /  *л*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-182">(*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span>             |
| <span data-ttu-id="829c9-183">ГК \_ 1 \_ минус \_ альфа-летнее \_</span><span class="sxs-lookup"><span data-stu-id="829c9-183">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> | <span data-ttu-id="829c9-184">(1, 1, 1, 1) — (*a*<sub>d</sub>  /  *k*<sub>а</sub> , *a*<sub>d</sub>  /  *k*<sub>а</sub> , *a*<sub>d</sub>  /  *k*<sub>а</sub> , *a*<sub>d</sub>  /  *л*<sub>a</sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-184">(1,1,1,1) - (*A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> , *A*<sub>d</sub> / *k*<sub>A</sub> )</span></span> |
| <span data-ttu-id="829c9-185">\_альфа- \_ канал ИСХОДНОГО \_ сегмента GL</span><span class="sxs-lookup"><span data-stu-id="829c9-185">GL\_SRC\_ALPHA\_SATURATE</span></span>   | <span data-ttu-id="829c9-186">(*i,* i, 1)</span><span class="sxs-lookup"><span data-stu-id="829c9-186">(*i,i,i,* 1)</span></span>                                                                                                                                                 |



 

<span data-ttu-id="829c9-187">В этой таблице:</span><span class="sxs-lookup"><span data-stu-id="829c9-187">In the table,</span></span>

<span data-ttu-id="829c9-188">*i* = min (*а*?</span><span class="sxs-lookup"><span data-stu-id="829c9-188">*i* = min (*A*?</span></span> <span data-ttu-id="829c9-189">, *k*<sub>a</sub>   -  <sub>d</sub> )/ *k*<sub></sub></span><span class="sxs-lookup"><span data-stu-id="829c9-189">, *k*<sub>A</sub>  - *A*<sub>d</sub> ) / *k*<sub>A</sub></span></span>

<span data-ttu-id="829c9-190">Чтобы определить смешивание значений RGBA пикселя при рисовании в режиме RGBA, система использует следующие уравнения:</span><span class="sxs-lookup"><span data-stu-id="829c9-190">To determine the blended RGBA values of a pixel when drawing in RGBA mode, the system uses the following equations:</span></span>

<span data-ttu-id="829c9-191">*R* (*d*) = min ( *k*<sub>R</sub> , *r*? *s*<sub>r r</sub>  +  <sub>d</sub> *d*<sub></sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-191">*R* (*d*) = min( *k*<sub>R</sub> , *R*? *s*<sub>R</sub> + *R*<sub>d</sub> *d*<sub>R</sub> )</span></span>

<span data-ttu-id="829c9-192">*G* (*d*) = min ( *k*<sub>G</sub> , *G*? *s*<sub>g</sub>  +  *g*<sub></sub> <sub>d</sub> *г.*)</span><span class="sxs-lookup"><span data-stu-id="829c9-192">*G* (*d*) = min( *k*<sub>G</sub> , *G*? *s*<sub>G</sub> + *G*<sub>d</sub> *d*<sub>G</sub>  )</span></span>

<span data-ttu-id="829c9-193">*B* (*d*) = min ( *k*<sub>B</sub> *, B*? *s*<sub>б</sub>  +  *б б*<sub></sub> <sub></sub> )</span><span class="sxs-lookup"><span data-stu-id="829c9-193">*B* (*d*) = min( *k*<sub>B</sub> *, B*? *s*<sub>B</sub> + *B*<sub>d</sub> *d*<sub>B</sub>  )</span></span>

<span data-ttu-id="829c9-194">*A* (*d*) = min ( *k*<sub>а</sub> , *A*? *а a*<sub></sub>  +  <sub>d</sub> *d*<sub></sub> a)</span><span class="sxs-lookup"><span data-stu-id="829c9-194">*A* (*d*) = min( *k*<sub>A</sub> , *A*? *s*<sub>A</sub> + *A*<sub>d</sub> *d*<sub>A</sub>  )</span></span>

<span data-ttu-id="829c9-195">Несмотря на очевидную точность приведенных выше уравнений, арифметическая операция смешения не указана точно, так как смешивание работает с неточными целочисленными значениями цвета.</span><span class="sxs-lookup"><span data-stu-id="829c9-195">Despite the apparent precision of the above equations, blending arithmetic is not exactly specified, because blending operates with imprecise integer color values.</span></span> <span data-ttu-id="829c9-196">Однако коэффициент смешения, который должен быть равен одному, гарантирует не изменять его множимое, а коэффициент смешения равен нулю сокращает множимое до нуля.</span><span class="sxs-lookup"><span data-stu-id="829c9-196">However, a blend factor that should be equal to one is guaranteed not to modify its multiplicand, and a blend factor equal to zero reduces its multiplicand to zero.</span></span> <span data-ttu-id="829c9-197">Таким образом, например, если *сфактор* — GL \_ src \_ , *дфактор* — это \_ 1 минус единица \_ \_ src \_ , а ? равно *k*<sub>a</sub>, уравнения уменьшаются в простую замену:</span><span class="sxs-lookup"><span data-stu-id="829c9-197">Thus, for example, when *sfactor* is GL\_SRC\_ALPHA, *dfactor* is GL\_ONE\_MINUS\_SRC\_ALPHA, and *A*? is equal to *k*<sub>A</sub>, the equations reduce to simple replacement:</span></span>

<span data-ttu-id="829c9-198">*R*<sub>d</sub>  =  *r*?</span><span class="sxs-lookup"><span data-stu-id="829c9-198">*R*<sub>d</sub> = *R*?</span></span>

<span data-ttu-id="829c9-199">*G*<sub>d</sub>  =  *g*?</span><span class="sxs-lookup"><span data-stu-id="829c9-199">*G*<sub>d</sub> = *G*?</span></span>

<span data-ttu-id="829c9-200">B <sub>d</sub>  =  *б*?</span><span class="sxs-lookup"><span data-stu-id="829c9-200">B <sub>d</sub> = *B*?</span></span>

<span data-ttu-id="829c9-201">*A*<sub>d</sub>  =  ?</span><span class="sxs-lookup"><span data-stu-id="829c9-201">*A*<sub>d</sub> = *A*?</span></span>

## <a name="examples"></a><span data-ttu-id="829c9-202">Примеры</span><span class="sxs-lookup"><span data-stu-id="829c9-202">Examples</span></span>

<span data-ttu-id="829c9-203">Прозрачность лучше всего реализуется с помощью **глблендфунк**(GL \_ src \_ альфа, GL \_ 1 \_ минус \_ src \_ альфа) с примитивами, отсортированными от ближайшего к ближайшему.</span><span class="sxs-lookup"><span data-stu-id="829c9-203">Transparency is best implemented using **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) with primitives sorted from farthest to nearest.</span></span> <span data-ttu-id="829c9-204">Обратите внимание, что для этого вычисления прозрачности не требуется наличие Alpha битпланес в буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="829c9-204">Note that this transparency calculation does not require the presence of alpha bitplanes in the framebuffer.</span></span>

<span data-ttu-id="829c9-205"> \_ \_ \_ \_ \_ \_ Для отрисовки точек и линий в произвольном порядке можно также использовать глблендфунк (GL src Alpha, GL 1 минус Альфа).</span><span class="sxs-lookup"><span data-stu-id="829c9-205">You can also use **glBlendFunc**(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) for rendering antialiased points and lines in arbitrary order.</span></span>

<span data-ttu-id="829c9-206">Чтобы оптимизировать сглаживание многоугольников, используйте **глблендфунк**(параметр " \_ альфа-канал исходного \_ сегмента GL \_ ", GL \_ 1) с многоугольниками, отсортированными от ближайшего к крайнему.</span><span class="sxs-lookup"><span data-stu-id="829c9-206">To optimize polygon antialiasing, use **glBlendFunc**(GL\_SRC\_ALPHA\_SATURATE, GL\_ONE) with polygons sorted from nearest to farthest.</span></span> <span data-ttu-id="829c9-207">(См. в GL \_ \_Аргумент гладкого многоугольника в [**гленабле**](glenable.md) для получения сведений о сглаживание многоугольников.) Назначение Alpha битпланес, которое должно присутствовать, чтобы эта функция Blend работала правильно, сохранить накопленное покрытие.</span><span class="sxs-lookup"><span data-stu-id="829c9-207">(See the GL\_POLYGON\_SMOOTH argument in [**glEnable**](glenable.md) for information on polygon antialiasing.) Destination alpha bitplanes, which must be present for this blend function to operate correctly, store the accumulated coverage.</span></span>

<span data-ttu-id="829c9-208">Входящий (исходный) альфа-код — это непрозрачность материала, в диапазоне от 1,0 (*K*<sub>a</sub> ), представляющая полную непрозрачность, до 0,0 (0), представляющая полную прозрачность.</span><span class="sxs-lookup"><span data-stu-id="829c9-208">Incoming (source) alpha is a material opacity, ranging from 1.0 (*K*<sub>A</sub> ), representing complete opacity, to 0.0 (0), representing complete transparency.</span></span>

<span data-ttu-id="829c9-209">При включении нескольких цветовых буферов для рисования каждый включенный буфер смешивается отдельно, а содержимое буфера используется для целевого цвета.</span><span class="sxs-lookup"><span data-stu-id="829c9-209">When you enable more than one color buffer for drawing, each enabled buffer is blended separately, and the contents of the buffer is used for destination color.</span></span> <span data-ttu-id="829c9-210">(См. [**глдравбуффер**](gldrawbuffer.md).)</span><span class="sxs-lookup"><span data-stu-id="829c9-210">(See [**glDrawBuffer**](gldrawbuffer.md).)</span></span>

<span data-ttu-id="829c9-211">Смешивание влияет только на отрисовку RGBA.</span><span class="sxs-lookup"><span data-stu-id="829c9-211">Blending affects only RGBA rendering.</span></span> <span data-ttu-id="829c9-212">Он игнорируется модулями подготовки к просмотру цветового индекса.</span><span class="sxs-lookup"><span data-stu-id="829c9-212">It is ignored by color-index renderers.</span></span>

<span data-ttu-id="829c9-213">Следующие функции извлекают сведения, относящиеся к **глблендфунк**:</span><span class="sxs-lookup"><span data-stu-id="829c9-213">The following functions retrieve information related to **glBlendFunc**:</span></span>

<span data-ttu-id="829c9-214">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Blend \_ src</span><span class="sxs-lookup"><span data-stu-id="829c9-214">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_SRC</span></span>

<span data-ttu-id="829c9-215">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) с аргументом GL \_ Blend \_ DST</span><span class="sxs-lookup"><span data-stu-id="829c9-215">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_BLEND\_DST</span></span>

<span data-ttu-id="829c9-216">[**глисенаблед**](glisenabled.md) с аргументом GL \_ Blend</span><span class="sxs-lookup"><span data-stu-id="829c9-216">[**glIsEnabled**](glisenabled.md) with argument GL\_BLEND</span></span>

## <a name="requirements"></a><span data-ttu-id="829c9-217">Требования</span><span class="sxs-lookup"><span data-stu-id="829c9-217">Requirements</span></span>



| <span data-ttu-id="829c9-218">Требование</span><span class="sxs-lookup"><span data-stu-id="829c9-218">Requirement</span></span> | <span data-ttu-id="829c9-219">Значение</span><span class="sxs-lookup"><span data-stu-id="829c9-219">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="829c9-220">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="829c9-220">Minimum supported client</span></span><br/> | <span data-ttu-id="829c9-221">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="829c9-221">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="829c9-222">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="829c9-222">Minimum supported server</span></span><br/> | <span data-ttu-id="829c9-223">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="829c9-223">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="829c9-224">Заголовок</span><span class="sxs-lookup"><span data-stu-id="829c9-224">Header</span></span><br/>                   | <dl> <span data-ttu-id="829c9-225"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="829c9-225"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="829c9-226">Библиотека</span><span class="sxs-lookup"><span data-stu-id="829c9-226">Library</span></span><br/>                  | <dl> <span data-ttu-id="829c9-227"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="829c9-227"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="829c9-228">DLL</span><span class="sxs-lookup"><span data-stu-id="829c9-228">DLL</span></span><br/>                      | <dl> <span data-ttu-id="829c9-229"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="829c9-229"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="829c9-230">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="829c9-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829c9-231">**глалфафунк**</span><span class="sxs-lookup"><span data-stu-id="829c9-231">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="829c9-232">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="829c9-232">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="829c9-233">**глклеар**</span><span class="sxs-lookup"><span data-stu-id="829c9-233">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="829c9-234">**глдисабле**</span><span class="sxs-lookup"><span data-stu-id="829c9-234">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="829c9-235">**глдравбуффер**</span><span class="sxs-lookup"><span data-stu-id="829c9-235">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="829c9-236">**гленабле**</span><span class="sxs-lookup"><span data-stu-id="829c9-236">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="829c9-237">**глжет**</span><span class="sxs-lookup"><span data-stu-id="829c9-237">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="829c9-238">**глисенаблед**</span><span class="sxs-lookup"><span data-stu-id="829c9-238">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="829c9-239">**гллогикоп**</span><span class="sxs-lookup"><span data-stu-id="829c9-239">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="829c9-240">**глстенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="829c9-240">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





