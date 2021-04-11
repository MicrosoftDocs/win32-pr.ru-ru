---
description: Состояния этапов текстуры определяют операции текстуры с несколькими операциями смешения.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Перечисление D3DTEXTURESTAGESTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273743"
---
# <a name="d3dtexturestagestatetype-enumeration"></a><span data-ttu-id="b5927-103">Перечисление D3DTEXTURESTAGESTATETYPE</span><span class="sxs-lookup"><span data-stu-id="b5927-103">D3DTEXTURESTAGESTATETYPE enumeration</span></span>

<span data-ttu-id="b5927-104">Состояния этапов текстуры определяют операции текстуры с несколькими операциями смешения.</span><span class="sxs-lookup"><span data-stu-id="b5927-104">Texture stage states define multi-blender texture operations.</span></span> <span data-ttu-id="b5927-105">Некоторые состояния образца настроили обработку вершин и некоторые настройки обработки пикселей.</span><span class="sxs-lookup"><span data-stu-id="b5927-105">Some sampler states set up vertex processing, and some set up pixel processing.</span></span> <span data-ttu-id="b5927-106">Состояния стадии текстуры можно сохранить и восстановить с помощью статеблоккс (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="b5927-106">Texture stage states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5927-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5927-107">Syntax</span></span>


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="b5927-108">Константы</span><span class="sxs-lookup"><span data-stu-id="b5927-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b5927-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ колороп**</span><span class="sxs-lookup"><span data-stu-id="b5927-109"><span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS\_COLOROP**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-110">Состояние стадии текстуры — это операция смешения цветов текстуры, определяемая одним элементом перечисляемого типа [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="b5927-110">Texture-stage state is a texture color blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="b5927-111">Значение по умолчанию для первой стадии текстуры (Стадия 0) — D3DTOP \_ модуляция, для всех остальных этапов значение по умолчанию — D3DTOP \_ disable.</span><span class="sxs-lookup"><span data-stu-id="b5927-111">The default value for the first texture stage (stage 0) is D3DTOP\_MODULATE; for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**</span><span class="sxs-lookup"><span data-stu-id="b5927-112"><span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS\_COLORARG1**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-113">Состояние стадии текстуры — это первый аргумент цвета для этапа, идентифицируемый одним из [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-113">Texture-stage state is the first color argument for the stage, identified by one of the [D3DTA](d3dta.md).</span></span> <span data-ttu-id="b5927-114">Аргументом по умолчанию является D3DTA \_ текстура.</span><span class="sxs-lookup"><span data-stu-id="b5927-114">The default argument is D3DTA\_TEXTURE.</span></span>

<span data-ttu-id="b5927-115">Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="b5927-115">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="b5927-116">D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп.</span><span class="sxs-lookup"><span data-stu-id="b5927-116">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="b5927-117">По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="b5927-117">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="b5927-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**</span><span class="sxs-lookup"><span data-stu-id="b5927-118"><span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS\_COLORARG2**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-119">Состояние этапа текстуры — это второй цветовой аргумент для этапа, идентифицируемый [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-119">Texture-stage state is the second color argument for the stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="b5927-120">Аргумент по умолчанию — D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="b5927-120">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="b5927-121">Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="b5927-121">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="b5927-122">D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп.</span><span class="sxs-lookup"><span data-stu-id="b5927-122">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="b5927-123">По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="b5927-123">The default value for the register is (0.0, 0.0, 0.0, 0.0)</span></span>

</dd> <dt>

<span data-ttu-id="b5927-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ алфаоп**</span><span class="sxs-lookup"><span data-stu-id="b5927-124"><span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS\_ALPHAOP**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-125">Состояние стадии текстуры — это операция смешения текстур, определяемая одним членом перечисляемого типа [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="b5927-125">Texture-stage state is a texture alpha blending operation identified by one member of the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span> <span data-ttu-id="b5927-126">Значение по умолчанию для первой стадии текстуры (Стадия 0) — D3DTOP \_ SELECTARG1, а для всех остальных этапов значение по умолчанию — D3DTOP \_ disable.</span><span class="sxs-lookup"><span data-stu-id="b5927-126">The default value for the first texture stage (stage 0) is D3DTOP\_SELECTARG1, and for all other stages the default is D3DTOP\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**</span><span class="sxs-lookup"><span data-stu-id="b5927-127"><span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS\_ALPHAARG1**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-128">Состояние этапа текстуры — это первый альфа-аргумент для этапа, идентифицируемый по [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-128">Texture-stage state is the first alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="b5927-129">Аргументом по умолчанию является D3DTA \_ текстура.</span><span class="sxs-lookup"><span data-stu-id="b5927-129">The default argument is D3DTA\_TEXTURE.</span></span> <span data-ttu-id="b5927-130">Если для этого этапа не задана текстура, аргументом по умолчанию является D3DTA \_ диффузия.</span><span class="sxs-lookup"><span data-stu-id="b5927-130">If no texture is set for this stage, the default argument is D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="b5927-131">Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="b5927-131">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="b5927-132">D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп.</span><span class="sxs-lookup"><span data-stu-id="b5927-132">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="b5927-133">По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="b5927-133">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="b5927-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**</span><span class="sxs-lookup"><span data-stu-id="b5927-134"><span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS\_ALPHAARG2**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-135">Состояние этапа текстуры — это второй альфа-аргумент для этапа, идентифицируемый по [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-135">Texture-stage state is the second alpha argument for the stage, identified by by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="b5927-136">Аргумент по умолчанию — D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="b5927-136">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="b5927-137">Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="b5927-137">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="b5927-138">D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп.</span><span class="sxs-lookup"><span data-stu-id="b5927-138">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="b5927-139">По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="b5927-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="b5927-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**</span><span class="sxs-lookup"><span data-stu-id="b5927-140"><span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS\_BUMPENVMAT00**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-141">Состояние этапа текстуры — это значение с плавающей запятой для \[ \] \[ \] коэффициента 0 0 в матрице сопоставления выпуклости.</span><span class="sxs-lookup"><span data-stu-id="b5927-141">Texture-stage state is a floating-point value for the \[0\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="b5927-142">Значение по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="b5927-142">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**</span><span class="sxs-lookup"><span data-stu-id="b5927-143"><span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS\_BUMPENVMAT01**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-144">Состояние этапа текстуры — это значение с плавающей запятой для \[ \] \[ \] коэффициента 0 1 в матрице сопоставления выпуклости.</span><span class="sxs-lookup"><span data-stu-id="b5927-144">Texture-stage state is a floating-point value for the \[0\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="b5927-145">Значение по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="b5927-145">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**</span><span class="sxs-lookup"><span data-stu-id="b5927-146"><span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS\_BUMPENVMAT10**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-147">Состояние этапа текстуры — это значение с плавающей запятой для \[ \] \[ \] коэффициента 1 0 в матрице сопоставления выпуклости.</span><span class="sxs-lookup"><span data-stu-id="b5927-147">Texture-stage state is a floating-point value for the \[1\]\[0\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="b5927-148">Значение по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="b5927-148">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**</span><span class="sxs-lookup"><span data-stu-id="b5927-149"><span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS\_BUMPENVMAT11**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-150">Состояние этапа текстуры — это значение с плавающей запятой для \[ \] \[ \] коэффициента 1 1 в матрице сопоставления выпуклости.</span><span class="sxs-lookup"><span data-stu-id="b5927-150">Texture-stage state is a floating-point value for the \[1\]\[1\] coefficient in a bump-mapping matrix.</span></span> <span data-ttu-id="b5927-151">Значение по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="b5927-151">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ текскурдиндекс**</span><span class="sxs-lookup"><span data-stu-id="b5927-152"><span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS\_TEXCOORDINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-153">Индекс набора координат текстуры для использования с этой стадией текстуры.</span><span class="sxs-lookup"><span data-stu-id="b5927-153">Index of the texture coordinate set to use with this texture stage.</span></span> <span data-ttu-id="b5927-154">Для каждой вершины можно указать до восьми наборов координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="b5927-154">You can specify up to eight sets of texture coordinates per vertex.</span></span> <span data-ttu-id="b5927-155">Если вершина не включает набор координат текстуры по указанному индексу, система по умолчанию использует координаты, заданные вами и v (0, 0).</span><span class="sxs-lookup"><span data-stu-id="b5927-155">If a vertex does not include a set of texture coordinates at the specified index, the system defaults to the u and v coordinates (0,0).</span></span>

<span data-ttu-id="b5927-156">При подготовке к просмотру с помощью шейдеров вершин в каждом из индексов координат текстуры каждого этапа должно быть задано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5927-156">When rendering using vertex shaders, each stage's texture coordinate index must be set to its default value.</span></span> <span data-ttu-id="b5927-157">Индекс по умолчанию для каждого этапа равен индексу этапа.</span><span class="sxs-lookup"><span data-stu-id="b5927-157">The default index for each stage is equal to the stage index.</span></span> <span data-ttu-id="b5927-158">Присвойте этому состоянию Отсчитываемый от нуля индекс набора координат для каждой вершины, используемой этой стадией текстуры.</span><span class="sxs-lookup"><span data-stu-id="b5927-158">Set this state to the zero-based index of the coordinate set for each vertex that this texture stage uses.</span></span>

<span data-ttu-id="b5927-159">Кроме того, приложения могут включать в качестве логического или с заданным индексом одну из констант для запроса, что Direct3D автоматически создает координаты входной текстуры для преобразования текстур.</span><span class="sxs-lookup"><span data-stu-id="b5927-159">Additionally, applications can include, as logical OR with the index being set, one of the constants to request that Direct3D automatically generate the input texture coordinates for a texture transformation.</span></span> <span data-ttu-id="b5927-160">Список всех констант см. в разделе [D3DTSS \_ тЦи](d3dtss-tci.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-160">For a list of all the constants, see [D3DTSS\_TCI](d3dtss-tci.md).</span></span>

<span data-ttu-id="b5927-161">За исключением D3DTSS \_ тЦи \_ PassThru, который разрешается в ноль, если любое из следующих значений включено в заданный индекс, система использует индекс строго для определения режима переноса текстур.</span><span class="sxs-lookup"><span data-stu-id="b5927-161">With the exception of D3DTSS\_TCI\_PASSTHRU, which resolves to zero, if any of the following values is included with the index being set, the system uses the index strictly to determine texture wrapping mode.</span></span> <span data-ttu-id="b5927-162">Эти флаги наиболее полезны при выполнении сопоставления среды.</span><span class="sxs-lookup"><span data-stu-id="b5927-162">These flags are most useful when performing environment mapping.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ бумпенвлскале**</span><span class="sxs-lookup"><span data-stu-id="b5927-163"><span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS\_BUMPENVLSCALE**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-164">Значение масштаба с плавающей запятой для светимости схемы выпуклости.</span><span class="sxs-lookup"><span data-stu-id="b5927-164">Floating-point scale value for bump-map luminance.</span></span> <span data-ttu-id="b5927-165">Значение по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="b5927-165">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ бумпенвлоффсет**</span><span class="sxs-lookup"><span data-stu-id="b5927-166"><span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS\_BUMPENVLOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-167">Значение смещения с плавающей точкой для светимости схемы выпуклости.</span><span class="sxs-lookup"><span data-stu-id="b5927-167">Floating-point offset value for bump-map luminance.</span></span> <span data-ttu-id="b5927-168">Значение по умолчанию — 0,0.</span><span class="sxs-lookup"><span data-stu-id="b5927-168">The default value is 0.0.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ текстуретрансформфлагс**</span><span class="sxs-lookup"><span data-stu-id="b5927-169"><span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS\_TEXTURETRANSFORMFLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-170">Член перечисляемого типа [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) , который управляет преобразованием координат текстуры для этой стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="b5927-170">Member of the [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) enumerated type that controls the transformation of texture coordinates for this texture stage.</span></span> <span data-ttu-id="b5927-171">Значение по умолчанию — D3DTTFF \_ disable.</span><span class="sxs-lookup"><span data-stu-id="b5927-171">The default value is D3DTTFF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**</span><span class="sxs-lookup"><span data-stu-id="b5927-172"><span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS\_COLORARG0**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-173">Параметры для третьего операнда цвета для операций триадик (умножение, Добавление и линейная интерполяция), идентифицируемые [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-173">Settings for the third color operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="b5927-174">Этот параметр поддерживается, если имеются \_ возможности устройства D3DTEXOPCAPS мултиплядд или D3DTEXOPCAPS \_ лерп.</span><span class="sxs-lookup"><span data-stu-id="b5927-174">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="b5927-175">Аргумент по умолчанию — D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="b5927-175">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="b5927-176">Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="b5927-176">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="b5927-177">D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп.</span><span class="sxs-lookup"><span data-stu-id="b5927-177">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="b5927-178">По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="b5927-178">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="b5927-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**</span><span class="sxs-lookup"><span data-stu-id="b5927-179"><span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS\_ALPHAARG0**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-180">Параметры для операнда выбора альфа-канала для операций триадик (умножение, Добавление и линейная интерполяция), идентифицируемые [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-180">Settings for the alpha channel selector operand for triadic operations (multiply, add, and linearly interpolate), identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="b5927-181">Этот параметр поддерживается, если имеются \_ возможности устройства D3DTEXOPCAPS мултиплядд или D3DTEXOPCAPS \_ лерп.</span><span class="sxs-lookup"><span data-stu-id="b5927-181">This setting is supported if the D3DTEXOPCAPS\_MULTIPLYADD or D3DTEXOPCAPS\_LERP device capabilities are present.</span></span> <span data-ttu-id="b5927-182">Аргумент по умолчанию — D3DTA \_ Current.</span><span class="sxs-lookup"><span data-stu-id="b5927-182">The default argument is D3DTA\_CURRENT.</span></span> <span data-ttu-id="b5927-183">Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="b5927-183">Specify D3DTA\_TEMP to select a temporary register color for read or write.</span></span> <span data-ttu-id="b5927-184">D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп.</span><span class="sxs-lookup"><span data-stu-id="b5927-184">D3DTA\_TEMP is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span> <span data-ttu-id="b5927-185">Аргумент по умолчанию — (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="b5927-185">The default argument is (0.0, 0.0, 0.0, 0.0).</span></span>

</dd> <dt>

<span data-ttu-id="b5927-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ ресултарг**</span><span class="sxs-lookup"><span data-stu-id="b5927-186"><span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS\_RESULTARG**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-187">Параметр для выбора регистра назначения для результата этого этапа, идентифицируемого [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-187">Setting to select destination register for the result of this stage, identified by [D3DTA](d3dta.md).</span></span> <span data-ttu-id="b5927-188">Это значение можно задать равным D3DTA \_ Current (значение по умолчанию) или D3DTA \_ TEMP, то есть единственный временный регистр, который можно считать на последующие этапы в качестве входного аргумента.</span><span class="sxs-lookup"><span data-stu-id="b5927-188">This value can be set to D3DTA\_CURRENT (the default value) or to D3DTA\_TEMP, which is a single temporary register that can be read into subsequent stages as an input argument.</span></span> <span data-ttu-id="b5927-189">Окончательный цвет, передаваемый для смешения тумана и буфера кадров, берется из D3DTA \_ Current, поэтому для последней активной стадии текстуры должно быть задано значение запись в текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="b5927-189">The final color passed to the fog blender and frame buffer is taken from D3DTA\_CURRENT, so the last active texture stage state must be set to write to current.</span></span> <span data-ttu-id="b5927-190">Этот параметр поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп.</span><span class="sxs-lookup"><span data-stu-id="b5927-190">This setting is supported if the D3DPMISCCAPS\_TSSARGTEMP device capability is present.</span></span>

</dd> <dt>

<span data-ttu-id="b5927-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**\_Константа D3DTSS**</span><span class="sxs-lookup"><span data-stu-id="b5927-191"><span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**D3DTSS\_CONSTANT**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-192">Постоянный цвет для каждого этапа.</span><span class="sxs-lookup"><span data-stu-id="b5927-192">Per-stage constant color.</span></span> <span data-ttu-id="b5927-193">Чтобы узнать, поддерживает ли устройство постоянную цветовую константу, ознакомьтесь с \_ константой D3DPMISCCAPS перстажеконстант в [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-193">To see if a device supports a per-stage constant color, see the D3DPMISCCAPS\_PERSTAGECONSTANT constant in [D3DPMISCCAPS](d3dpmisccaps.md).</span></span> <span data-ttu-id="b5927-194">Константа D3DTSS \_ используется \_ константой D3DTA.</span><span class="sxs-lookup"><span data-stu-id="b5927-194">D3DTSS\_CONSTANT is used by D3DTA\_CONSTANT.</span></span> <span data-ttu-id="b5927-195">См. [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="b5927-195">See [D3DTA](d3dta.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5927-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b5927-196"><span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b5927-197">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="b5927-197">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b5927-198">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="b5927-198">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b5927-199">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="b5927-199">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5927-200">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5927-200">Remarks</span></span>

<span data-ttu-id="b5927-201">Члены этого перечислимого типа используются с методами [**IDirect3DDevice9:: жеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) и [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) для получения и задания значений состояния текстуры.</span><span class="sxs-lookup"><span data-stu-id="b5927-201">Members of this enumerated type are used with the [**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) and [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) methods to retrieve and set texture state values.</span></span>

<span data-ttu-id="b5927-202">Допустимый диапазон значений для \_ \_ коэффициентов матрицы D3DTSS BUMPENVMAT00, D3DTSS BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 и D3DTSS BUMPENVMAT11, которые \_ больше или равны-8,0 и меньше 8,0.</span><span class="sxs-lookup"><span data-stu-id="b5927-202">The valid range of values for the D3DTSS\_BUMPENVMAT00, D3DTSS\_BUMPENVMAT01, D3DTSS\_BUMPENVMAT10, and D3DTSS\_BUMPENVMAT11 bump-mapping matrix coefficients is greater than or equal to -8.0 and less than 8.0.</span></span> <span data-ttu-id="b5927-203">Этот диапазон, выраженный в математической нотации, — (-8.0, 8.0).</span><span class="sxs-lookup"><span data-stu-id="b5927-203">This range, expressed in mathematical notation is (-8.0,8.0).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5927-204">Требования</span><span class="sxs-lookup"><span data-stu-id="b5927-204">Requirements</span></span>



| <span data-ttu-id="b5927-205">Требование</span><span class="sxs-lookup"><span data-stu-id="b5927-205">Requirement</span></span> | <span data-ttu-id="b5927-206">Значение</span><span class="sxs-lookup"><span data-stu-id="b5927-206">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5927-207">Header</span><span class="sxs-lookup"><span data-stu-id="b5927-207">Header</span></span><br/> | <dl> <span data-ttu-id="b5927-208"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5927-208"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5927-209">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5927-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5927-210">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="b5927-210">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="b5927-211">**IDirect3DDevice9:: Жеттекстурестажестате**</span><span class="sxs-lookup"><span data-stu-id="b5927-211">**IDirect3DDevice9::GetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[<span data-ttu-id="b5927-212">**IDirect3DDevice9:: Сеттекстурестажестате**</span><span class="sxs-lookup"><span data-stu-id="b5927-212">**IDirect3DDevice9::SetTextureStageState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
