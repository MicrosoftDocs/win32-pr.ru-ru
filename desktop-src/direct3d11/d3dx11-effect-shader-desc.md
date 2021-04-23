---
title: Структура D3DX11_EFFECT_SHADER_DESC (D3dx11effect. h)
description: Описывает шейдер эффектов.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914800"
---
# <a name="d3dx11_effect_shader_desc-structure"></a><span data-ttu-id="8b903-104">\_ \_ Структура построителя шейдеров D3DX11 Effect \_</span><span class="sxs-lookup"><span data-stu-id="8b903-104">D3DX11\_EFFECT\_SHADER\_DESC structure</span></span>

<span data-ttu-id="8b903-105">Описывает шейдер эффектов.</span><span class="sxs-lookup"><span data-stu-id="8b903-105">Describes an effect shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b903-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b903-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="8b903-107">Участники</span><span class="sxs-lookup"><span data-stu-id="8b903-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b903-108">**пинпутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="8b903-108">**pInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="8b903-109">Тип: **Константный [**байт**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="8b903-109">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="8b903-110">Передано в Креатеинпутлайаут.</span><span class="sxs-lookup"><span data-stu-id="8b903-110">Passed into CreateInputLayout.</span></span> <span data-ttu-id="8b903-111">Допустим только для шейдера вершин или шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="8b903-111">Only valid on a vertex shader or geometry shader.</span></span> <span data-ttu-id="8b903-112">См. раздел [**ID3D11Device:: креатеинпутлайаут**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="8b903-112">See [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="8b903-113">**исинлине**</span><span class="sxs-lookup"><span data-stu-id="8b903-113">**IsInline**</span></span>
</dt> <dd>

<span data-ttu-id="8b903-114">Тип: **[ **bool** .](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b903-114">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8b903-115">**Значение true** , если шейдер определяется встроенным; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="8b903-115">**TRUE** is the shader is defined inline; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8b903-116">**пбитекоде**</span><span class="sxs-lookup"><span data-stu-id="8b903-116">**pBytecode**</span></span>
</dt> <dd>

<span data-ttu-id="8b903-117">Тип: **Константный [**байт**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="8b903-117">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="8b903-118">Байтовый код шейдера.</span><span class="sxs-lookup"><span data-stu-id="8b903-118">Shader bytecode.</span></span>

</dd> <dt>

<span data-ttu-id="8b903-119">**битекоделенгс**</span><span class="sxs-lookup"><span data-stu-id="8b903-119">**BytecodeLength**</span></span>
</dt> <dd>

<span data-ttu-id="8b903-120">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b903-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8b903-121">Длина Пбитекоде.</span><span class="sxs-lookup"><span data-stu-id="8b903-121">The length of pBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="8b903-122">**содеклс**</span><span class="sxs-lookup"><span data-stu-id="8b903-122">**SODecls**</span></span>
</dt> <dd>

<span data-ttu-id="8b903-123">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b903-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8b903-124">Потоковая строка объявления (для шейдера Geometry с таким образом).</span><span class="sxs-lookup"><span data-stu-id="8b903-124">Stream out declaration string (for geometry shader with SO).</span></span>

</dd> <dt>

<span data-ttu-id="8b903-125">**растеризедстреам**</span><span class="sxs-lookup"><span data-stu-id="8b903-125">**RasterizedStream**</span></span>
</dt> <dd>

<span data-ttu-id="8b903-126">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b903-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8b903-127">Указывает, какой поток является растровым.</span><span class="sxs-lookup"><span data-stu-id="8b903-127">Indicates which stream is rasterized.</span></span> <span data-ttu-id="8b903-128">Шейдеры D3D11 Geometry могут выводить до четырех потоков данных, один из которых может быть растрирования.</span><span class="sxs-lookup"><span data-stu-id="8b903-128">D3D11 geometry shaders can output up to four streams of data, one of which can be rasterized.</span></span>

</dd> <dt>

<span data-ttu-id="8b903-129">**нуминпутсигнатуринтриес**</span><span class="sxs-lookup"><span data-stu-id="8b903-129">**NumInputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="8b903-130">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b903-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8b903-131">Число записей во входной подписи.</span><span class="sxs-lookup"><span data-stu-id="8b903-131">Number of entries in the input signature.</span></span>

</dd> <dt>

<span data-ttu-id="8b903-132">**нумаутпутсигнатуринтриес**</span><span class="sxs-lookup"><span data-stu-id="8b903-132">**NumOutputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="8b903-133">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b903-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8b903-134">Число записей в выходной подписи.</span><span class="sxs-lookup"><span data-stu-id="8b903-134">Number of entries in the output signature.</span></span>

</dd> <dt>

<span data-ttu-id="8b903-135">**нумпатчконстантсигнатуринтриес**</span><span class="sxs-lookup"><span data-stu-id="8b903-135">**NumPatchConstantSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="8b903-136">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8b903-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="8b903-137">Число записей в сигнатуре константы исправления.</span><span class="sxs-lookup"><span data-stu-id="8b903-137">Number of entries in the patch constant signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b903-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b903-138">Remarks</span></span>

<span data-ttu-id="8b903-139">D3DX11 \_ Effect \_ Shader \_ DESC используется с [**ID3DX11EffectShaderVariable:: жетшадердеск**](id3dx11effectshadervariable-getshaderdesc.md).</span><span class="sxs-lookup"><span data-stu-id="8b903-139">D3DX11\_EFFECT\_SHADER\_DESC is used with [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b903-140">Требования</span><span class="sxs-lookup"><span data-stu-id="8b903-140">Requirements</span></span>



| <span data-ttu-id="8b903-141">Требование</span><span class="sxs-lookup"><span data-stu-id="8b903-141">Requirement</span></span> | <span data-ttu-id="8b903-142">Значение</span><span class="sxs-lookup"><span data-stu-id="8b903-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b903-143">Header</span><span class="sxs-lookup"><span data-stu-id="8b903-143">Header</span></span><br/> | <dl> <span data-ttu-id="8b903-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b903-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b903-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b903-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b903-146">Эффекты с 11 по структурам</span><span class="sxs-lookup"><span data-stu-id="8b903-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

