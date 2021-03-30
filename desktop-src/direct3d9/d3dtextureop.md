---
description: Определяет операции смешения текстур для каждого этапа.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Перечисление D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354513"
---
# <a name="d3dtextureop-enumeration"></a><span data-ttu-id="b6a63-103">Перечисление D3DTEXTUREOP</span><span class="sxs-lookup"><span data-stu-id="b6a63-103">D3DTEXTUREOP enumeration</span></span>

<span data-ttu-id="b6a63-104">Определяет операции смешения текстур для каждого этапа.</span><span class="sxs-lookup"><span data-stu-id="b6a63-104">Defines per-stage texture-blending operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6a63-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a><span data-ttu-id="b6a63-106">Константы</span><span class="sxs-lookup"><span data-stu-id="b6a63-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b6a63-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**\_Отключение D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="b6a63-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-108">Отключает вывод этого этапа текстуры и всех стадий с более высоким индексом.</span><span class="sxs-lookup"><span data-stu-id="b6a63-108">Disables output from this texture stage and all stages with a higher index.</span></span> <span data-ttu-id="b6a63-109">Чтобы отключить сопоставление текстур, установите его в качестве цветовой операции для первой стадии текстуры (этап 0).</span><span class="sxs-lookup"><span data-stu-id="b6a63-109">To disable texture mapping, set this as the color operation for the first texture stage (stage 0).</span></span> <span data-ttu-id="b6a63-110">Операции Alpha не могут быть отключены, если включены цветовые операции.</span><span class="sxs-lookup"><span data-stu-id="b6a63-110">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="b6a63-111">Установка для операции Alpha значения D3DTOP \_ Disable, если включено смешение цветов, приводит к неопределенному поведению.</span><span class="sxs-lookup"><span data-stu-id="b6a63-111">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

</dd> <dt>

<span data-ttu-id="b6a63-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**</span><span class="sxs-lookup"><span data-stu-id="b6a63-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP\_SELECTARG1**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-113">Используйте первый цвет или альфа-параметр этого этапа текстуры в качестве выходных данных в неизмененном виде.</span><span class="sxs-lookup"><span data-stu-id="b6a63-113">Use this texture stage's first color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="b6a63-114">Эта операция влияет на аргумент Color при использовании с \_ состоянием этапа текстуры D3DTSS колороп и альфа-аргумент при использовании с D3DTSS \_ алфаоп.</span><span class="sxs-lookup"><span data-stu-id="b6a63-114">This operation affects the color argument when used with the D3DTSS\_COLOROP texture-stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![уравнение этого аргумента (s (RGBA) = arg1)](images/topfrm1.png)

</dd> <dt>

<span data-ttu-id="b6a63-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**</span><span class="sxs-lookup"><span data-stu-id="b6a63-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP\_SELECTARG2**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-117">Используйте второй цвет или альфа-параметр этого этапа текстуры без изменений в качестве выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b6a63-117">Use this texture stage's second color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="b6a63-118">Эта операция влияет на аргумент Color при использовании с \_ состоянием этапа текстуры D3DTSS колороп и альфа-аргумент при использовании с D3DTSS \_ алфаоп.</span><span class="sxs-lookup"><span data-stu-id="b6a63-118">This operation affects the color argument when used with the D3DTSS\_COLOROP texture stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![уравнение этого аргумента (s (RGBA) = arg2)](images/topfrm2.png)

</dd> <dt>

<span data-ttu-id="b6a63-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOPная \_ модуляция**</span><span class="sxs-lookup"><span data-stu-id="b6a63-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP\_MODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-121">Умножьте компоненты аргументов.</span><span class="sxs-lookup"><span data-stu-id="b6a63-121">Multiply the components of the arguments.</span></span>

![уравнение операции модуляции (s (RGBA) = arg1 x ARG 2)](images/topfrm3.png)

</dd> <dt>

<span data-ttu-id="b6a63-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**</span><span class="sxs-lookup"><span data-stu-id="b6a63-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP\_MODULATE2X**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-124">Умножьте компоненты аргументов и переместит продукты влево на 1 бит (что значительно умножает их на 2) для повышения яркости.</span><span class="sxs-lookup"><span data-stu-id="b6a63-124">Multiply the components of the arguments, and shift the products to the left 1 bit (effectively multiplying them by 2) for brightening.</span></span>

![уравнение операции modulate2x (s (RGBA) = (arg1 x ARG 2), затем сдвиг влево 1)](images/topfrm4.png)

</dd> <dt>

<span data-ttu-id="b6a63-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**</span><span class="sxs-lookup"><span data-stu-id="b6a63-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP\_MODULATE4X**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-127">Умножьте компоненты аргументов и переместит продукты влево на 2 бита (по сути, умножая их на 4) для повышения яркости.</span><span class="sxs-lookup"><span data-stu-id="b6a63-127">Multiply the components of the arguments, and shift the products to the left 2 bits (effectively multiplying them by 4) for brightening.</span></span>

![уравнение операции modulate4x (s (RGBA) = (arg1 x ARG 2), затем сдвиг влево 2)](images/topfrm5.png)

</dd> <dt>

<span data-ttu-id="b6a63-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Добавить**</span><span class="sxs-lookup"><span data-stu-id="b6a63-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-130">Добавьте компоненты аргументов.</span><span class="sxs-lookup"><span data-stu-id="b6a63-130">Add the components of the arguments.</span></span>

![уравнение операции добавления (s (RGBA) = arg1 + ARG 2)](images/topfrm6.png)

</dd> <dt>

<span data-ttu-id="b6a63-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ аддсигнед**</span><span class="sxs-lookup"><span data-stu-id="b6a63-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP\_ADDSIGNED**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-133">Добавьте компоненты аргументов с помощью смещения-0,5, сделав эффективный диапазон значений от-0,5 до 0,5.</span><span class="sxs-lookup"><span data-stu-id="b6a63-133">Add the components of the arguments with a - 0.5 bias, making the effective range of values from - 0.5 through 0.5.</span></span>

![Уравнение для операции добавления подписанного (s (RGBA) = arg1 + ARG 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span data-ttu-id="b6a63-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**</span><span class="sxs-lookup"><span data-stu-id="b6a63-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP\_ADDSIGNED2X**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-136">Добавьте компоненты аргументов с помощью смещения-0,5 и переместит продукты на левый 1 бит.</span><span class="sxs-lookup"><span data-stu-id="b6a63-136">Add the components of the arguments with a - 0.5 bias, and shift the products to the left 1 bit.</span></span>

![уравнение операции добавления 2x ((s (RGBA) = arg1 + ARG 2-0,5), затем сдвиг влево 1)](images/topfrm8.png)

</dd> <dt>

<span data-ttu-id="b6a63-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**\_Вычитание D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="b6a63-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-139">Вычтите компоненты второго аргумента из значений первого аргумента.</span><span class="sxs-lookup"><span data-stu-id="b6a63-139">Subtract the components of the second argument from those of the first argument.</span></span>

![уравнение операции вычитания (s (RGBA) = arg1-ARG 2)](images/topfrm9.png)

</dd> <dt>

<span data-ttu-id="b6a63-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ аддсмус**</span><span class="sxs-lookup"><span data-stu-id="b6a63-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP\_ADDSMOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-142">Добавьте первый и второй аргументы. затем вычтите свой продукт из суммы.</span><span class="sxs-lookup"><span data-stu-id="b6a63-142">Add the first and second arguments; then subtract their product from the sum.</span></span>

![уравнение операции добавления сглаживания (s (RGBA) = arg1 + ARG 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span data-ttu-id="b6a63-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ бленддиффусеалфа**</span><span class="sxs-lookup"><span data-stu-id="b6a63-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP\_BLENDDIFFUSEALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-145">Линейный переход на эту стадию текстуры с помощью интерполяции альфа-канала из каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="b6a63-145">Linearly blend this texture stage, using the interpolated alpha from each vertex.</span></span>

![уравнение операции смешения альфа-канала (s (RGBA) = arg1 x альфа + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="b6a63-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ блендтекстуреалфа**</span><span class="sxs-lookup"><span data-stu-id="b6a63-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP\_BLENDTEXTUREALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-148">Линейное смешение этой стадии текстуры с помощью альфа-канала на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="b6a63-148">Linearly blend this texture stage, using the alpha from this stage's texture.</span></span>

![Формула Альфа-операции смешения текстур (s (RGBA) = arg1 x альфа + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="b6a63-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ блендфакторалфа**</span><span class="sxs-lookup"><span data-stu-id="b6a63-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP\_BLENDFACTORALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-151">Линейный переход на эту стадию текстуры с помощью скалярного набора альфа-каналов с \_ состоянием отрисовки D3DRS текстурефактор.</span><span class="sxs-lookup"><span data-stu-id="b6a63-151">Linearly blend this texture stage, using a scalar alpha set with the D3DRS\_TEXTUREFACTOR render state.</span></span>

![уравнение операции альфа-канала коэффициента смешения (s (RGBA) = arg1 x альфа + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="b6a63-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ блендтекстуреалфапм**</span><span class="sxs-lookup"><span data-stu-id="b6a63-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP\_BLENDTEXTUREALPHAPM**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-154">Линейное смешение этапа текстуры с использованием предварительно умноженного альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="b6a63-154">Linearly blend a texture stage that uses a premultiplied alpha.</span></span>

![Уравнение для операции смешения текстур альфа-канала (s (RGBA) = arg1 + ARG 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span data-ttu-id="b6a63-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ блендкурренталфа**</span><span class="sxs-lookup"><span data-stu-id="b6a63-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP\_BLENDCURRENTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-157">Линейный переход на эту стадию текстуры с использованием альфа-канала, взятого из предыдущей стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="b6a63-157">Linearly blend this texture stage, using the alpha taken from the previous texture stage.</span></span>

![уравнение текущей Альфа-операции Blend (s (RGBA) = arg1 x альфа + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="b6a63-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOPная \_ ПОДмодуляция**</span><span class="sxs-lookup"><span data-stu-id="b6a63-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP\_PREMODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-160">\_Предварительная модуляция D3DTOP установлена на этапе n.</span><span class="sxs-lookup"><span data-stu-id="b6a63-160">D3DTOP\_PREMODULATE is set in stage n.</span></span> <span data-ttu-id="b6a63-161">Выходные данные этапа n — это arg1.</span><span class="sxs-lookup"><span data-stu-id="b6a63-161">The output of stage n is arg1.</span></span> <span data-ttu-id="b6a63-162">Кроме того, если на этапе n + 1 имеется текстура, все D3DTA, \_ текущие в шаге n + 1, предварительно умножаются на текстуру на этапе n + 1.</span><span class="sxs-lookup"><span data-stu-id="b6a63-162">Additionally, if there is a texture in stage n + 1, any D3DTA\_CURRENT in stage n + 1 is premultiplied by texture in stage n + 1.</span></span>

</dd> <dt>

<span data-ttu-id="b6a63-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ модулатеалфа \_ аддколор**</span><span class="sxs-lookup"><span data-stu-id="b6a63-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP\_MODULATEALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-164">Модуляция цвета второго аргумента с помощью альфа-канала первого аргумента; Затем добавьте результат в аргумент один.</span><span class="sxs-lookup"><span data-stu-id="b6a63-164">Modulate the color of the second argument, using the alpha of the first argument; then add the result to argument one.</span></span> <span data-ttu-id="b6a63-165">Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).</span><span class="sxs-lookup"><span data-stu-id="b6a63-165">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![уравнение операции добавления цветовой модуляции альфа (s (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB))](images/topfrm13.png)

</dd> <dt>

<span data-ttu-id="b6a63-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ модулатеколор \_ аддалфа**</span><span class="sxs-lookup"><span data-stu-id="b6a63-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP\_MODULATECOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-168">Модуляция аргументов; Затем добавьте альфа-канал первого аргумента.</span><span class="sxs-lookup"><span data-stu-id="b6a63-168">Modulate the arguments; then add the alpha of the first argument.</span></span> <span data-ttu-id="b6a63-169">Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).</span><span class="sxs-lookup"><span data-stu-id="b6a63-169">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![уравнение операции добавления цвета для альфа-модуляции (s (RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span data-ttu-id="b6a63-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ модулатеинвалфа \_ аддколор**</span><span class="sxs-lookup"><span data-stu-id="b6a63-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP\_MODULATEINVALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-172">Аналогично D3DTOP \_ модулатеалфа \_ аддколор, но используйте обратную букву альфа-канала первого аргумента.</span><span class="sxs-lookup"><span data-stu-id="b6a63-172">Similar to D3DTOP\_MODULATEALPHA\_ADDCOLOR, but use the inverse of the alpha of the first argument.</span></span> <span data-ttu-id="b6a63-173">Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).</span><span class="sxs-lookup"><span data-stu-id="b6a63-173">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![уравнение добавления цветовой модуляции обратная альфа-операция (s (RGBA) = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span data-ttu-id="b6a63-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ модулатеинвколор \_ аддалфа**</span><span class="sxs-lookup"><span data-stu-id="b6a63-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP\_MODULATEINVCOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-176">Аналогично D3DTOP \_ модулатеколор \_ аддалфа, но используйте инверсию цвета первого аргумента.</span><span class="sxs-lookup"><span data-stu-id="b6a63-176">Similar to D3DTOP\_MODULATECOLOR\_ADDALPHA, but use the inverse of the color of the first argument.</span></span> <span data-ttu-id="b6a63-177">Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).</span><span class="sxs-lookup"><span data-stu-id="b6a63-177">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![Формула операции добавления цвета инверсии альфа-модуляции (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span data-ttu-id="b6a63-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ бумпенвмап**</span><span class="sxs-lookup"><span data-stu-id="b6a63-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP\_BUMPENVMAP**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-180">Выполняйте сопоставление выпуклости по пикселям, используя карту окружения на следующей стадии текстуры без освещенности.</span><span class="sxs-lookup"><span data-stu-id="b6a63-180">Perform per-pixel bump mapping, using the environment map in the next texture stage, without luminance.</span></span> <span data-ttu-id="b6a63-181">Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).</span><span class="sxs-lookup"><span data-stu-id="b6a63-181">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="b6a63-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ бумпенвмаплуминанце**</span><span class="sxs-lookup"><span data-stu-id="b6a63-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP\_BUMPENVMAPLUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-183">Выполняйте сопоставление выпуклости по пикселям, используя карту окружения на следующей стадии текстуры с яркостью.</span><span class="sxs-lookup"><span data-stu-id="b6a63-183">Perform per-pixel bump mapping, using the environment map in the next texture stage, with luminance.</span></span> <span data-ttu-id="b6a63-184">Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).</span><span class="sxs-lookup"><span data-stu-id="b6a63-184">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="b6a63-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**</span><span class="sxs-lookup"><span data-stu-id="b6a63-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP\_DOTPRODUCT3**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-186">Модуляция компонентов каждого аргумента как подписанных компонентов, добавление их продуктов; затем реплицирует сумму во все цветовые каналы, включая альфа.</span><span class="sxs-lookup"><span data-stu-id="b6a63-186">Modulate the components of each argument as signed components, add their products; then replicate the sum to all color channels, including alpha.</span></span> <span data-ttu-id="b6a63-187">Эта операция поддерживается для операций Color и Alpha.</span><span class="sxs-lookup"><span data-stu-id="b6a63-187">This operation is supported for color and alpha operations.</span></span>

![Формула операции с точкой 3 (s) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b))](images/topfrm17.png)

<span data-ttu-id="b6a63-189">В DirectX 6 и DirectX 7 при работе с несколькими текстурами указанные выше входные данные сдвигаются вниз (y = x-0,5) перед использованием для имитации подписанных данных, а скалярный результат автоматически переносится в положительные значения и реплицируется во все три выходных канала.</span><span class="sxs-lookup"><span data-stu-id="b6a63-189">In DirectX 6 and DirectX 7, multitexture operations the above inputs are all shifted down by half (y = x - 0.5) before use to simulate signed data, and the scalar result is automatically clamped to positive values and replicated to all three output channels.</span></span> <span data-ttu-id="b6a63-190">Кроме того, обратите внимание, что в качестве цветовой операции альфа-канал просто обновляет компоненты RGB.</span><span class="sxs-lookup"><span data-stu-id="b6a63-190">Also, note that as a color operation this does not updated the alpha it just updates the RGB components.</span></span>

<span data-ttu-id="b6a63-191">Однако в шейдерах DirectX 8,1 можно указать, что выходные данные направляются в. RGB или. a или оба (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b6a63-191">However, in DirectX 8.1 shaders you can specify that the output be routed to the .rgb or the .a components or both (the default).</span></span> <span data-ttu-id="b6a63-192">В альфа-канале можно также указать отдельную скалярную операцию.</span><span class="sxs-lookup"><span data-stu-id="b6a63-192">You can also specify a separate scalar operation on the alpha channel.</span></span>

</dd> <dt>

<span data-ttu-id="b6a63-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ мултиплядд**</span><span class="sxs-lookup"><span data-stu-id="b6a63-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP\_MULTIPLYADD**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-194">Выполняет операцию умножения накопления.</span><span class="sxs-lookup"><span data-stu-id="b6a63-194">Performs a multiply-accumulate operation.</span></span> <span data-ttu-id="b6a63-195">Он принимает два последних аргумента, умножает их вместе и добавляет их к оставшимся аргументам ввода-вывода и помещает их в результат.</span><span class="sxs-lookup"><span data-stu-id="b6a63-195">It takes the last two arguments, multiplies them together, and adds them to the remaining input/source argument, and places that into the result.</span></span>

<span data-ttu-id="b6a63-196">S<sub>RGBA</sub> = arg1 + arg2 \* arg3</span><span class="sxs-lookup"><span data-stu-id="b6a63-196">S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3</span></span>

</dd> <dt>

<span data-ttu-id="b6a63-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ лерп**</span><span class="sxs-lookup"><span data-stu-id="b6a63-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP\_LERP**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-198">Линейная интерполяция между вторым и третьим исходными аргументами по пропорции, указанной в первом аргументе источника.</span><span class="sxs-lookup"><span data-stu-id="b6a63-198">Linearly interpolates between the second and third source arguments by a proportion specified in the first source argument.</span></span>

<span data-ttu-id="b6a63-199">S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* arg3.</span><span class="sxs-lookup"><span data-stu-id="b6a63-199">S<sub>RGBA</sub> = (Arg1) \* Arg2 + (1- Arg1) \* Arg3.</span></span>

</dd> <dt>

<span data-ttu-id="b6a63-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b6a63-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b6a63-201">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="b6a63-201">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b6a63-202">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="b6a63-202">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b6a63-203">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="b6a63-203">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6a63-204">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6a63-204">Remarks</span></span>

<span data-ttu-id="b6a63-205">Элементы этого типа используются при задании цветов или альфа-операций с помощью \_ значений D3DTSS колороп или D3DTSS \_ алфаоп с помощью метода [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="b6a63-205">The members of this type are used when setting color or alpha operations by using the D3DTSS\_COLOROP or D3DTSS\_ALPHAOP values with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span>

<span data-ttu-id="b6a63-206">В приведенных выше формулах<sub>RGBA</sub> — это цвет RGBA, созданный операцией текстуры, а arg1, arg2 и arg3 — полный цвет RGBA для аргументов текстуры.</span><span class="sxs-lookup"><span data-stu-id="b6a63-206">In the above formulas, S<sub>RGBA</sub> is the RGBA color produced by a texture operation, and Arg1, Arg2, and Arg3 represent the complete RGBA color of the texture arguments.</span></span> <span data-ttu-id="b6a63-207">Отдельные компоненты аргумента отображаются с помощью индексов.</span><span class="sxs-lookup"><span data-stu-id="b6a63-207">Individual components of an argument are shown with subscripts.</span></span> <span data-ttu-id="b6a63-208">Например, альфа-компонент для аргумента 1 будет показан как arg1<sub>A</sub>.</span><span class="sxs-lookup"><span data-stu-id="b6a63-208">For example, the alpha component for argument 1 would be shown as Arg1<sub>A</sub>.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a63-209">Требования</span><span class="sxs-lookup"><span data-stu-id="b6a63-209">Requirements</span></span>



| <span data-ttu-id="b6a63-210">Требование</span><span class="sxs-lookup"><span data-stu-id="b6a63-210">Requirement</span></span> | <span data-ttu-id="b6a63-211">Значение</span><span class="sxs-lookup"><span data-stu-id="b6a63-211">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a63-212">Header</span><span class="sxs-lookup"><span data-stu-id="b6a63-212">Header</span></span><br/> | <dl> <span data-ttu-id="b6a63-213"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6a63-213"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6a63-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6a63-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a63-215">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="b6a63-215">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="b6a63-216">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="b6a63-216">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
