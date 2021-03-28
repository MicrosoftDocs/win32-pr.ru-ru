---
title: Метод ID3DX11EffectBlendVariable Жетбаккингсторе (D3dx11effect. h)
description: Получает указатель на переменную состояния Blend.
ms.assetid: 809daaad-9bf0-48fb-ae91-f237c43db324
keywords:
- Метод Жетбаккингсторе Direct3D 11
- Метод Жетбаккингсторе Direct3D 11, интерфейс ID3DX11EffectBlendVariable
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11, метод Жетбаккингсторе
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0220481b58931edace2a5dfe7298d83f7bd1325
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273906"
---
# <a name="id3dx11effectblendvariablegetbackingstore-method"></a><span data-ttu-id="0e075-106">Метод ID3DX11EffectBlendVariable:: Жетбаккингсторе</span><span class="sxs-lookup"><span data-stu-id="0e075-106">ID3DX11EffectBlendVariable::GetBackingStore method</span></span>

<span data-ttu-id="0e075-107">Получает указатель на переменную состояния Blend.</span><span class="sxs-lookup"><span data-stu-id="0e075-107">Get a pointer to a blend-state variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e075-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e075-108">Syntax</span></span>


```C++
HRESULT GetBackingStore(
   UINT             Index,
   D3D11_BLEND_DESC *pBlendDesc
);
```



## <a name="parameters"></a><span data-ttu-id="0e075-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e075-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e075-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="0e075-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="0e075-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0e075-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="0e075-112">Индекс в массиве описаний состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="0e075-112">Index into an array of blend-state descriptions.</span></span> <span data-ttu-id="0e075-113">Если в результате имеется только одна переменная состояния Blend, используйте значение 0.</span><span class="sxs-lookup"><span data-stu-id="0e075-113">If there is only one blend-state variable in the effect, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="0e075-114">*пбленддеск*</span><span class="sxs-lookup"><span data-stu-id="0e075-114">*pBlendDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="0e075-115">Тип: **[ **D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***</span><span class="sxs-lookup"><span data-stu-id="0e075-115">Type: **[**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)\***</span></span>

<span data-ttu-id="0e075-116">Указатель на описание состояния Blend (см. [**D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).</span><span class="sxs-lookup"><span data-stu-id="0e075-116">A pointer to a blend-state description (see [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e075-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e075-117">Return value</span></span>

<span data-ttu-id="0e075-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e075-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e075-119">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0e075-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e075-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e075-120">Remarks</span></span>

<span data-ttu-id="0e075-121">Переменные эффектов сохраняются в памяти в резервном хранилище; При применении метода значения в резервном хранилище копируются на устройство.</span><span class="sxs-lookup"><span data-stu-id="0e075-121">Effect variables are saved in memory in the backing store; when a technique is applied, the values in the backing store are copied to the device.</span></span> <span data-ttu-id="0e075-122">Резервные копии данных хранилища могут использоваться для повторного создания переменной при необходимости.</span><span class="sxs-lookup"><span data-stu-id="0e075-122">Backing store data can used to recreate the variable when necessary.</span></span>

> [!Note]  
> <span data-ttu-id="0e075-123">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="0e075-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0e075-124">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="0e075-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0e075-125">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0e075-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0e075-126">Требования</span><span class="sxs-lookup"><span data-stu-id="0e075-126">Requirements</span></span>



| <span data-ttu-id="0e075-127">Требование</span><span class="sxs-lookup"><span data-stu-id="0e075-127">Requirement</span></span> | <span data-ttu-id="0e075-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0e075-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e075-129">Header</span><span class="sxs-lookup"><span data-stu-id="0e075-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0e075-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e075-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0e075-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0e075-131">Library</span></span><br/> | <dl> <span data-ttu-id="0e075-132"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="0e075-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e075-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e075-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e075-134">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="0e075-134">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

