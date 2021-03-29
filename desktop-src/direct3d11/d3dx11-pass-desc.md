---
title: Структура D3DX11_PASS_DESC (D3dx11effect. h)
description: Описывает пройденный результат, который содержит состояние конвейера.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987203"
---
# <a name="d3dx11_pass_desc-structure"></a><span data-ttu-id="34568-104">\_Структура D3DX11 Pass \_ DESC</span><span class="sxs-lookup"><span data-stu-id="34568-104">D3DX11\_PASS\_DESC structure</span></span>

<span data-ttu-id="34568-105">Описывает пройденный результат, который содержит состояние конвейера.</span><span class="sxs-lookup"><span data-stu-id="34568-105">Describes an effect pass, which contains pipeline state.</span></span>

## <a name="syntax"></a><span data-ttu-id="34568-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34568-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a><span data-ttu-id="34568-107">Участники</span><span class="sxs-lookup"><span data-stu-id="34568-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="34568-108">**имя**;</span><span class="sxs-lookup"><span data-stu-id="34568-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="34568-109">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34568-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="34568-110">Имя этого этапа (**null** , если он не является анонимным).</span><span class="sxs-lookup"><span data-stu-id="34568-110">Name of this pass (**NULL** if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="34568-111">**Заметки**</span><span class="sxs-lookup"><span data-stu-id="34568-111">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="34568-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34568-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="34568-113">Число заметок на этом проходе.</span><span class="sxs-lookup"><span data-stu-id="34568-113">Number of annotations on this pass.</span></span>

</dd> <dt>

<span data-ttu-id="34568-114">**пиаинпутсигнатуре**</span><span class="sxs-lookup"><span data-stu-id="34568-114">**pIAInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="34568-115">Тип: **[ **Byte**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="34568-115">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="34568-116">Сигнатура из шейдера вершин или шейдера Geometry (Если шейдер вершин отсутствует) или **значение NULL** , если ни один из них не существует.</span><span class="sxs-lookup"><span data-stu-id="34568-116">Signature from the vertex shader or geometry shader (if there is no vertex shader) or **NULL** if neither exists.</span></span>

</dd> <dt>

<span data-ttu-id="34568-117">**иаинпутсигнатуресизе**</span><span class="sxs-lookup"><span data-stu-id="34568-117">**IAInputSignatureSize**</span></span>
</dt> <dd>

<span data-ttu-id="34568-118">Type: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34568-118">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="34568-119">Размер сингатуре в байтах.</span><span class="sxs-lookup"><span data-stu-id="34568-119">Singature size in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="34568-120">**стенЦилреф**</span><span class="sxs-lookup"><span data-stu-id="34568-120">**StencilRef**</span></span>
</dt> <dd>

<span data-ttu-id="34568-121">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34568-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="34568-122">Значение ссылки на набор элементов, используемое в состоянии трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="34568-122">The stencil-reference value used in the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="34568-123">**самплемаск**</span><span class="sxs-lookup"><span data-stu-id="34568-123">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="34568-124">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34568-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="34568-125">Образец маски для состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="34568-125">The sample mask for the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="34568-126">**блендфактор**</span><span class="sxs-lookup"><span data-stu-id="34568-126">**BlendFactor**</span></span>
</dt> <dd>

<span data-ttu-id="34568-127">Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34568-127">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="34568-128">Коэффициенты смешения для каждого компонента (RGBA) для состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="34568-128">The per-component blend factors (RGBA) for the blend state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34568-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="34568-129">Remarks</span></span>

<span data-ttu-id="34568-130">D3DX11 \_ Pass \_ DESC используется с [**ID3DX11EffectPass:: DESC**](id3dx11effectpass-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="34568-130">D3DX11\_PASS\_DESC is used with [**ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34568-131">Требования</span><span class="sxs-lookup"><span data-stu-id="34568-131">Requirements</span></span>



| <span data-ttu-id="34568-132">Требование</span><span class="sxs-lookup"><span data-stu-id="34568-132">Requirement</span></span> | <span data-ttu-id="34568-133">Значение</span><span class="sxs-lookup"><span data-stu-id="34568-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="34568-134">Header</span><span class="sxs-lookup"><span data-stu-id="34568-134">Header</span></span><br/> | <dl> <span data-ttu-id="34568-135"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="34568-135"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34568-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34568-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34568-137">Эффекты с 11 по структурам</span><span class="sxs-lookup"><span data-stu-id="34568-137">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

