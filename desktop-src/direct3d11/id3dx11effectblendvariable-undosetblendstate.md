---
title: Метод ID3DX11EffectBlendVariable Ундосетблендстате (D3dx11effect. h)
description: Восстанавливает ранее установленное состояние Blend.
ms.assetid: 375c225b-558f-4ad0-81e7-62eff3e28cf1
keywords:
- Метод Ундосетблендстате Direct3D 11
- Метод Ундосетблендстате Direct3D 11, интерфейс ID3DX11EffectBlendVariable
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11, метод Ундосетблендстате
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.UndoSetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e117eafa9b6379b2240cf491809c58d8600d840f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998591"
---
# <a name="id3dx11effectblendvariableundosetblendstate-method"></a><span data-ttu-id="949a7-106">Метод ID3DX11EffectBlendVariable:: Ундосетблендстате</span><span class="sxs-lookup"><span data-stu-id="949a7-106">ID3DX11EffectBlendVariable::UndoSetBlendState method</span></span>

<span data-ttu-id="949a7-107">Восстанавливает ранее установленное состояние Blend.</span><span class="sxs-lookup"><span data-stu-id="949a7-107">Reverts a previously set blend-state.</span></span>

## <a name="syntax"></a><span data-ttu-id="949a7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="949a7-108">Syntax</span></span>


```C++
HRESULT UndoSetBlendState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="949a7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="949a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="949a7-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="949a7-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="949a7-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="949a7-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="949a7-112">Индекс в массиве интерфейсов состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="949a7-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="949a7-113">Если имеется только один интерфейс состояния Blend, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="949a7-113">If there is only one blend-state interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="949a7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="949a7-114">Return value</span></span>

<span data-ttu-id="949a7-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="949a7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="949a7-116">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="949a7-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="949a7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="949a7-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="949a7-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="949a7-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="949a7-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="949a7-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="949a7-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="949a7-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="949a7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="949a7-121">Requirements</span></span>



| <span data-ttu-id="949a7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="949a7-122">Requirement</span></span> | <span data-ttu-id="949a7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="949a7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="949a7-124">Header</span><span class="sxs-lookup"><span data-stu-id="949a7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="949a7-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="949a7-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="949a7-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="949a7-126">Library</span></span><br/> | <dl> <span data-ttu-id="949a7-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="949a7-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="949a7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="949a7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="949a7-129">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="949a7-129">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

