---
description: Функция D3DX10ComputeNormalMap — преобразует карту высоты в обычную карту. Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Функция D3DX10ComputeNormalMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 173a8e0c1b3130a399152187eb52288a0306051c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105322"
---
# <a name="d3dx10computenormalmap-function"></a><span data-ttu-id="135fa-104">Функция D3DX10ComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="135fa-104">D3DX10ComputeNormalMap function</span></span>

<span data-ttu-id="135fa-105">Преобразует карту высоты в обычную карту.</span><span class="sxs-lookup"><span data-stu-id="135fa-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="135fa-106">Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.</span><span class="sxs-lookup"><span data-stu-id="135fa-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="135fa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="135fa-107">Syntax</span></span>


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a><span data-ttu-id="135fa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="135fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="135fa-109">*псрктекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="135fa-109">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="135fa-110">Тип: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="135fa-110">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="135fa-111">Указатель на интерфейс ID3D10Texture2D, представляющий текстуру исходной карты с высотой.</span><span class="sxs-lookup"><span data-stu-id="135fa-111">Pointer to an ID3D10Texture2D interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="135fa-112">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="135fa-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="135fa-113">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="135fa-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="135fa-114">Один или несколько \_ флагов НОРМАЛМАП D3DX, управляющих созданием обычных карт.</span><span class="sxs-lookup"><span data-stu-id="135fa-114">One or more D3DX\_NORMALMAP flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="135fa-115">*Канал* \[ связи окне\]</span><span class="sxs-lookup"><span data-stu-id="135fa-115">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="135fa-116">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="135fa-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="135fa-117">Один \_ флаг канала D3DX, указывающий источник сведений о высоте.</span><span class="sxs-lookup"><span data-stu-id="135fa-117">One D3DX\_CHANNEL flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="135fa-118">*Амплитуда* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="135fa-118">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="135fa-119">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="135fa-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="135fa-120">Коэффициент величины постоянного значения, увеличивающий (или уменьшающий) значения в нормальном сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="135fa-120">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="135fa-121">Более высокие значения обычно делают выпуклости более видимыми, а более низкие значения обычно делают невидимыми более выпуклости.</span><span class="sxs-lookup"><span data-stu-id="135fa-121">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> <dt>

<span data-ttu-id="135fa-122">*пдесттекстуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="135fa-122">*pDestTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="135fa-123">Тип: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="135fa-123">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="135fa-124">Указатель на интерфейс ID3D10Texture2D, представляющий текстуру назначения.</span><span class="sxs-lookup"><span data-stu-id="135fa-124">Pointer to an ID3D10Texture2D interface, representing the destination texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="135fa-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="135fa-125">Return value</span></span>

<span data-ttu-id="135fa-126">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="135fa-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="135fa-127">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="135fa-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="135fa-128">Если функция завершается ошибкой, возвращаемое значение может иметь следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="135fa-128">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="135fa-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="135fa-129">Remarks</span></span>

<span data-ttu-id="135fa-130">Этот метод рассчитывает нормальную работу, используя Центральное различие с размером ядра 3X3.</span><span class="sxs-lookup"><span data-stu-id="135fa-130">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="135fa-131">Каналы RGB в назначении содержат смещенные компоненты (x, y, z) нормали.</span><span class="sxs-lookup"><span data-stu-id="135fa-131">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span> <span data-ttu-id="135fa-132">Центральный разностный знаменатель жестко закодирован в 2,0.</span><span class="sxs-lookup"><span data-stu-id="135fa-132">The central differencing denominator is hardcoded to 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="135fa-133">Требования</span><span class="sxs-lookup"><span data-stu-id="135fa-133">Requirements</span></span>



| <span data-ttu-id="135fa-134">Требование</span><span class="sxs-lookup"><span data-stu-id="135fa-134">Requirement</span></span> | <span data-ttu-id="135fa-135">Значение</span><span class="sxs-lookup"><span data-stu-id="135fa-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="135fa-136">Header</span><span class="sxs-lookup"><span data-stu-id="135fa-136">Header</span></span><br/>  | <dl> <span data-ttu-id="135fa-137"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="135fa-137"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="135fa-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="135fa-138">Library</span></span><br/> | <dl> <span data-ttu-id="135fa-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="135fa-139"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="135fa-140">См. также</span><span class="sxs-lookup"><span data-stu-id="135fa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135fa-141">Функции текстуры в D3DX 10</span><span class="sxs-lookup"><span data-stu-id="135fa-141">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
