---
title: Метод ID3DX11EffectPass Жетаннотатионбиндекс (D3dx11effect. h)
description: Получение заметки по индексу. | Метод ID3DX11EffectPass Жетаннотатионбиндекс (D3dx11effect. h)
ms.assetid: 734eeeca-58c2-4f0c-84d1-2898394a03d6
keywords:
- Метод Жетаннотатионбиндекс Direct3D 11
- Метод Жетаннотатионбиндекс Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Жетаннотатионбиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afd43a52758e82434a0e0a4161484ea0d4dcc611
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987113"
---
# <a name="id3dx11effectpassgetannotationbyindex-method"></a><span data-ttu-id="cc173-107">Метод ID3DX11EffectPass:: Жетаннотатионбиндекс</span><span class="sxs-lookup"><span data-stu-id="cc173-107">ID3DX11EffectPass::GetAnnotationByIndex method</span></span>

<span data-ttu-id="cc173-108">Получение заметки по индексу.</span><span class="sxs-lookup"><span data-stu-id="cc173-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc173-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc173-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="cc173-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc173-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc173-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="cc173-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="cc173-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cc173-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cc173-113">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="cc173-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc173-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc173-114">Return value</span></span>

<span data-ttu-id="cc173-115">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc173-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="cc173-116">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="cc173-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc173-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc173-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cc173-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="cc173-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cc173-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="cc173-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cc173-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cc173-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc173-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cc173-121">Requirements</span></span>



| <span data-ttu-id="cc173-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cc173-122">Requirement</span></span> | <span data-ttu-id="cc173-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cc173-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc173-124">Header</span><span class="sxs-lookup"><span data-stu-id="cc173-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cc173-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc173-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cc173-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cc173-126">Library</span></span><br/> | <dl> <span data-ttu-id="cc173-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="cc173-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc173-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc173-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc173-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="cc173-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

