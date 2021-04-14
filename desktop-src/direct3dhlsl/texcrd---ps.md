---
title: текскрд-PS
description: Копирует данные координат текстуры из исходного итератора координат текстуры в качестве данных цвета в регистр назначения.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997067"
---
# <a name="texcrd---ps"></a><span data-ttu-id="08e69-103">текскрд-PS</span><span class="sxs-lookup"><span data-stu-id="08e69-103">texcrd - ps</span></span>

<span data-ttu-id="08e69-104">Копирует данные координат текстуры из исходного итератора координат текстуры в качестве данных цвета в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="08e69-104">Copies texture coordinate data from the source texture coordinate iterator register as color data in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e69-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08e69-105">Syntax</span></span>



| <span data-ttu-id="08e69-106">текскрд DST, src</span><span class="sxs-lookup"><span data-stu-id="08e69-106">texcrd dst, src</span></span> |
|-----------------|



 

<span data-ttu-id="08e69-107">где</span><span class="sxs-lookup"><span data-stu-id="08e69-107">where</span></span>

-   <span data-ttu-id="08e69-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="08e69-108">dst is the destination register.</span></span>
-   <span data-ttu-id="08e69-109">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="08e69-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="08e69-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="08e69-110">Remarks</span></span>



| <span data-ttu-id="08e69-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="08e69-111">Pixel shader versions</span></span> | <span data-ttu-id="08e69-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="08e69-112">1\_1</span></span> | <span data-ttu-id="08e69-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="08e69-113">1\_2</span></span> | <span data-ttu-id="08e69-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="08e69-114">1\_3</span></span> | <span data-ttu-id="08e69-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="08e69-115">1\_4</span></span> | <span data-ttu-id="08e69-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="08e69-116">2\_0</span></span> | <span data-ttu-id="08e69-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="08e69-117">2\_x</span></span> | <span data-ttu-id="08e69-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="08e69-118">2\_sw</span></span> | <span data-ttu-id="08e69-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="08e69-119">3\_0</span></span> | <span data-ttu-id="08e69-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="08e69-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="08e69-121">текскрд</span><span class="sxs-lookup"><span data-stu-id="08e69-121">texcrd</span></span>                |      |      |      | <span data-ttu-id="08e69-122">x</span><span class="sxs-lookup"><span data-stu-id="08e69-122">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="08e69-123">Эта инструкция интерпретирует данные о координатах как данные цвета (RGBA).</span><span class="sxs-lookup"><span data-stu-id="08e69-123">This instruction interprets coordinate data as color data (RGBA).</span></span>

<span data-ttu-id="08e69-124">Эта инструкция не демонстрирует выборку текстуры.</span><span class="sxs-lookup"><span data-stu-id="08e69-124">No texture is sampled by this instruction.</span></span> <span data-ttu-id="08e69-125">Только координаты текстуры, заданные на этом этапе текстуры, являются релевантными.</span><span class="sxs-lookup"><span data-stu-id="08e69-125">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="08e69-126">При использовании текскрд учитывайте следующие сведения о копировании данных из исходной регистрации в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="08e69-126">When using texcrd, keep in mind the following detail about how data is copied from the source register to the destination register.</span></span> <span data-ttu-id="08e69-127">Исходная регистр координаты текстуры (t \# ) содержит данные в диапазоне \[ — D3DCAPS9. Макстекстуререпеат, D3DCAPS9. Макстекстуререпеат \] , в то время как регистр назначения (r \# ) может хранить данные только в (скорее всего, уменьшенном) диапазоне \[ — D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] .</span><span class="sxs-lookup"><span data-stu-id="08e69-127">The source texture coordinate register (t\#) holds data in the range \[-D3DCAPS9.MaxTextureRepeat, D3DCAPS9.MaxTextureRepeat\], while the destination register (r\#) can hold data only in the (likely smaller) range \[-D3DCAPS9.PixelShader1xMaxValue, D3DCAPS9.PixelShader1xMaxValue\].</span></span> <span data-ttu-id="08e69-128">Обратите внимание, что для Pixel Shader версии 1 \_ 4, D3DCAPS9. PixelShader1xMaxValue должно быть не менее восьми.</span><span class="sxs-lookup"><span data-stu-id="08e69-128">Note that for pixel shader version 1\_4, D3DCAPS9.PixelShader1xMaxValue must be a minimum of eight.</span></span> <span data-ttu-id="08e69-129">Инструкция текскрд в процессе фиксации исходных данных, находящихся вне диапазона регистра назначения, может вести себя по-разному на разных устройствах.</span><span class="sxs-lookup"><span data-stu-id="08e69-129">The texcrd instruction, in the process of clamping source data that is out of range of the destination register, is likely to behave differently on different hardware.</span></span> <span data-ttu-id="08e69-130">Первое оборудование построителя текстуры версии 1 \_ 4 на рынке выполнит Специальный зажим для значений вне диапазона.</span><span class="sxs-lookup"><span data-stu-id="08e69-130">The first pixel shader version 1\_4 hardware on the market will perform a special clamp for values outside of range.</span></span> <span data-ttu-id="08e69-131">Этот зажим предназначен для получения числа, которое может поместиться в регистр назначения, но также для сохранения поведения адресации текстур для данных вне диапазона (см. [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)), если данные должны быть впоследствии использованы для выборки текстуры.</span><span class="sxs-lookup"><span data-stu-id="08e69-131">This clamp is designed to produce a number that can fit into the destination register, but also to preserve texture addressing behavior for out-of-range data (see [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) if the data were to be subsequently used for texture sampling.</span></span> <span data-ttu-id="08e69-132">Однако новое оборудование от разных производителей может не столкнуться с этим поведением и может просто Чоп данные в соответствии с диапазоном регистров места назначения.</span><span class="sxs-lookup"><span data-stu-id="08e69-132">However, new hardware from different manufacturers might not exhibit this behavior and might just chop data to fit the destination register range.</span></span> <span data-ttu-id="08e69-133">Таким образом, самый надежный вариант действий при использовании пиксельного шейдера версии 1 \_ 4 текскрд заключается в предоставлении данных координат текстуры только в шейдер пикселей, который уже находится в диапазоне \[ от-8, 8, \] чтобы не полагаться на способ аппаратных фиксаций.</span><span class="sxs-lookup"><span data-stu-id="08e69-133">Therefore, the safest course of action when using pixel shader version 1\_4 texcrd is to supply texture coordinate data only into the pixel shader that is already within the range \[-8,8\] so that you do not rely on the way hardware clamps.</span></span>

<span data-ttu-id="08e69-134">В отличие от текскурд \_ , текскрд не выполняет срез значений между 0 и 1.</span><span class="sxs-lookup"><span data-stu-id="08e69-134">Unlike texcoord\_, texcrd does not clamp values between 0 and 1.</span></span>

<span data-ttu-id="08e69-135">Правила использования текскрд:</span><span class="sxs-lookup"><span data-stu-id="08e69-135">Rules for using texcrd :</span></span>

1.  <span data-ttu-id="08e69-136">Один и тот же модификатор. XYZ или. ксив должен применяться к каждому чтению отдельного регистра t (n) в инструкции текскрд или текслд.</span><span class="sxs-lookup"><span data-stu-id="08e69-136">The same .xyz or .xyw modifier must be applied to every read of an individual t(n) register within a texcrd or texld instruction.</span></span>
2.  <span data-ttu-id="08e69-137">Четвертый канал текскрд не определен во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="08e69-137">The fourth channel result of texcrd is unset/undefined in all cases.</span></span>
3.  <span data-ttu-id="08e69-138">Третий канал не определен для \_ случая ксив DW.</span><span class="sxs-lookup"><span data-stu-id="08e69-138">The third channel is unset/undefined for the xyw\_dw case.</span></span>

## <a name="examples"></a><span data-ttu-id="08e69-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="08e69-139">Examples</span></span>

<span data-ttu-id="08e69-140">Полный набор разрешенных синтаксиса для текскрд, учитывающий все допустимые сочетания модификатора источника, селектора и целевой маски записи, приведен ниже.</span><span class="sxs-lookup"><span data-stu-id="08e69-140">The complete set of allowed syntax for texcrd, taking into account all valid source modifier/selector and destination write mask combinations, is shown below.</span></span> <span data-ttu-id="08e69-141">Обратите внимание, что нотацию. RGBA и. ксизв можно использовать в качестве взаимозаменяемых.</span><span class="sxs-lookup"><span data-stu-id="08e69-141">Note that the .rgba and .xyzw notation can be used interchangeably.</span></span>

<span data-ttu-id="08e69-142">Копирует первые три канала в регистре итератора координат текстуры, t (n), в r (m).</span><span class="sxs-lookup"><span data-stu-id="08e69-142">Copies first three channels of texture coordinate iterator register, t(n), into r(m).</span></span> <span data-ttu-id="08e69-143">Четвертый канал r (m) не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="08e69-143">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



<span data-ttu-id="08e69-144">Помещает первый, второй и четвертый компоненты t (n) в первые три канала r (m).</span><span class="sxs-lookup"><span data-stu-id="08e69-144">Puts first, second, and fourth components of t(n) into first three channels of r(m).</span></span> <span data-ttu-id="08e69-145">Четвертый канал r (m) не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="08e69-145">The fourth channel of r(m) is uninitialized.</span></span>


```
texcrd  r(m).rgb, t(n).xyw
```



<span data-ttu-id="08e69-146">Ниже приведен пример проецированного деления с использованием \_ модификатора хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="08e69-146">Here is a projective divide example using the \_dw modifier.</span></span>

<span data-ttu-id="08e69-147">Этот пример копирует x/w и y/w из t (n) в первые два канала r (m).</span><span class="sxs-lookup"><span data-stu-id="08e69-147">This example copies x/w and y/w from t(n) into the first two channels of r(m).</span></span> <span data-ttu-id="08e69-148">Третий и четвертый каналы r (m) не инициализированы.</span><span class="sxs-lookup"><span data-stu-id="08e69-148">The third and fourth channels of r(m) are uninitialized.</span></span> <span data-ttu-id="08e69-149">Все данные, ранее записанные в третий канал r (m), будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="08e69-149">Any data previously written to the third channel of r(m) will be lost.</span></span> <span data-ttu-id="08e69-150">Данные в четвертом канале r (m) теряются из-за маркера этапа.</span><span class="sxs-lookup"><span data-stu-id="08e69-150">Data in the fourth channel of r(m) is lost due to the phase marker.</span></span> <span data-ttu-id="08e69-151">Для версии 1 \_ 4 \_ флаг прогноза D3DTTFF игнорируется.</span><span class="sxs-lookup"><span data-stu-id="08e69-151">For version 1\_4, the D3DTTFF\_PROJECTED flag is ignored.</span></span>


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a><span data-ttu-id="08e69-152">См. также</span><span class="sxs-lookup"><span data-stu-id="08e69-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e69-153">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="08e69-153">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 