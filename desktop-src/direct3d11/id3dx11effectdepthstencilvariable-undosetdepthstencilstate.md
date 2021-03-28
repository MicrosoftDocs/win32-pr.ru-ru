---
title: Метод ID3DX11EffectDepthStencilVariable УндосетдепсстенЦилстате (D3dx11effect. h)
description: Восстанавливает ранее заданное состояние трафарета глубины.
ms.assetid: 558bc777-a520-4235-84d3-db2d9f1ce4b6
keywords:
- Метод УндосетдепсстенЦилстате Direct3D 11
- Метод УндосетдепсстенЦилстате Direct3D 11, интерфейс ID3DX11EffectDepthStencilVariable
- Интерфейс ID3DX11EffectDepthStencilVariable Direct3D 11, метод УндосетдепсстенЦилстате
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.UndoSetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd44d486d2613406617f0534046c54818267dd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998648"
---
# <a name="id3dx11effectdepthstencilvariableundosetdepthstencilstate-method"></a><span data-ttu-id="97958-106">Метод ID3DX11EffectDepthStencilVariable:: УндосетдепсстенЦилстате</span><span class="sxs-lookup"><span data-stu-id="97958-106">ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState method</span></span>

<span data-ttu-id="97958-107">Восстанавливает ранее заданное состояние трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="97958-107">Reverts a previously set depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="97958-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97958-108">Syntax</span></span>


```C++
HRESULT UndoSetDepthStencilState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="97958-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="97958-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97958-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="97958-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="97958-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97958-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97958-112">Индекс в массиве интерфейсов трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="97958-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="97958-113">Если имеется только один интерфейс трафарета глубины, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="97958-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97958-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97958-114">Return value</span></span>

<span data-ttu-id="97958-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97958-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97958-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="97958-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97958-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="97958-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="97958-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="97958-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="97958-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="97958-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="97958-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="97958-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="97958-121">Требования</span><span class="sxs-lookup"><span data-stu-id="97958-121">Requirements</span></span>



| <span data-ttu-id="97958-122">Требование</span><span class="sxs-lookup"><span data-stu-id="97958-122">Requirement</span></span> | <span data-ttu-id="97958-123">Значение</span><span class="sxs-lookup"><span data-stu-id="97958-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97958-124">Header</span><span class="sxs-lookup"><span data-stu-id="97958-124">Header</span></span><br/>  | <dl> <span data-ttu-id="97958-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="97958-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="97958-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="97958-126">Library</span></span><br/> | <dl> <span data-ttu-id="97958-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="97958-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97958-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97958-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97958-129">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="97958-129">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

