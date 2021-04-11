---
title: Метод ID3DX11EffectRasterizerVariable Сетрастеризерстате (D3dx11effect. h)
description: Задает состояние средства программной прорисовки.
ms.assetid: b2cd93fb-77bb-4a39-b686-7b8f683c9172
keywords:
- Метод Сетрастеризерстате Direct3D 11
- Метод Сетрастеризерстате Direct3D 11, интерфейс ID3DX11EffectRasterizerVariable
- Интерфейс ID3DX11EffectRasterizerVariable Direct3D 11, метод Сетрастеризерстате
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.SetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c1f44df653339f274207bfa4283fc8470c8844f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273980"
---
# <a name="id3dx11effectrasterizervariablesetrasterizerstate-method"></a><span data-ttu-id="3c390-106">Метод ID3DX11EffectRasterizerVariable:: Сетрастеризерстате</span><span class="sxs-lookup"><span data-stu-id="3c390-106">ID3DX11EffectRasterizerVariable::SetRasterizerState method</span></span>

<span data-ttu-id="3c390-107">Задает состояние средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="3c390-107">Sets the rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c390-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c390-108">Syntax</span></span>


```C++
HRESULT SetRasterizerState(
   UINT                  Index,
   ID3D11RasterizerState *pRasterizerState
);
```



## <a name="parameters"></a><span data-ttu-id="3c390-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c390-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c390-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="3c390-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="3c390-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3c390-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3c390-112">Индексировать в массив интерфейсов средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="3c390-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="3c390-113">Если имеется только один интерфейс, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="3c390-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="3c390-114">*прастеризерстате*</span><span class="sxs-lookup"><span data-stu-id="3c390-114">*pRasterizerState*</span></span> 
</dt> <dd>

<span data-ttu-id="3c390-115">Тип: **[ **ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span><span class="sxs-lookup"><span data-stu-id="3c390-115">Type: **[**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate)\***</span></span>

<span data-ttu-id="3c390-116">Указатель на интерфейс [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) .</span><span class="sxs-lookup"><span data-stu-id="3c390-116">Pointer to an [**ID3D11RasterizerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c390-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c390-117">Return value</span></span>

<span data-ttu-id="3c390-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c390-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c390-119">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3c390-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c390-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c390-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c390-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="3c390-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3c390-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="3c390-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3c390-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3c390-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c390-124">Требования</span><span class="sxs-lookup"><span data-stu-id="3c390-124">Requirements</span></span>



| <span data-ttu-id="3c390-125">Требование</span><span class="sxs-lookup"><span data-stu-id="3c390-125">Requirement</span></span> | <span data-ttu-id="3c390-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3c390-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c390-127">Header</span><span class="sxs-lookup"><span data-stu-id="3c390-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3c390-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c390-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3c390-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c390-129">Library</span></span><br/> | <dl> <span data-ttu-id="3c390-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="3c390-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c390-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c390-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c390-132">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="3c390-132">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

