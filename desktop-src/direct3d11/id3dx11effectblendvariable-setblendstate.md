---
title: Метод ID3DX11EffectBlendVariable Сетблендстате (D3dx11effect. h)
description: Задает состояние смешения для действия.
ms.assetid: 46100721-65a3-46de-aa22-3e7e2fb7b960
keywords:
- Метод Сетблендстате Direct3D 11
- Метод Сетблендстате Direct3D 11, интерфейс ID3DX11EffectBlendVariable
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11, метод Сетблендстате
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.SetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce781f29c521df7b81821cb19a56e6fd3999310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821309"
---
# <a name="id3dx11effectblendvariablesetblendstate-method"></a><span data-ttu-id="8fc0e-106">Метод ID3DX11EffectBlendVariable:: Сетблендстате</span><span class="sxs-lookup"><span data-stu-id="8fc0e-106">ID3DX11EffectBlendVariable::SetBlendState method</span></span>

<span data-ttu-id="8fc0e-107">Задает состояние смешения для действия.</span><span class="sxs-lookup"><span data-stu-id="8fc0e-107">Sets an effect's blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc0e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fc0e-108">Syntax</span></span>


```C++
HRESULT SetBlendState(
   UINT             Index,
   ID3D11BlendState *pBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="8fc0e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fc0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc0e-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="8fc0e-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc0e-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8fc0e-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8fc0e-112">Индекс в массиве интерфейсов состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="8fc0e-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="8fc0e-113">Если имеется только один интерфейс состояния Blend, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="8fc0e-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="8fc0e-114">*пблендстате*</span><span class="sxs-lookup"><span data-stu-id="8fc0e-114">*pBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc0e-115">Тип: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span><span class="sxs-lookup"><span data-stu-id="8fc0e-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\***</span></span>

<span data-ttu-id="8fc0e-116">Указатель на интерфейс [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) , содержащий заданное состояние смешения.</span><span class="sxs-lookup"><span data-stu-id="8fc0e-116">A pointer to an [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate) interface containing the blend-state to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc0e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fc0e-117">Return value</span></span>

<span data-ttu-id="8fc0e-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8fc0e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8fc0e-119">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8fc0e-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc0e-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="8fc0e-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8fc0e-121">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="8fc0e-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8fc0e-122">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="8fc0e-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8fc0e-123">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8fc0e-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8fc0e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8fc0e-124">Requirements</span></span>



| <span data-ttu-id="8fc0e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8fc0e-125">Requirement</span></span> | <span data-ttu-id="8fc0e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8fc0e-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc0e-127">Header</span><span class="sxs-lookup"><span data-stu-id="8fc0e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8fc0e-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc0e-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8fc0e-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8fc0e-129">Library</span></span><br/> | <dl> <span data-ttu-id="8fc0e-130"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="8fc0e-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc0e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fc0e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc0e-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="8fc0e-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

