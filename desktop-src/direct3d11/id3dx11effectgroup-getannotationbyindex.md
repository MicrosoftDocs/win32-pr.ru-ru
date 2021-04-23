---
title: Метод ID3DX11EffectGroup Жетаннотатионбиндекс (D3dx11effect. h)
description: Получение заметки по индексу. | Метод ID3DX11EffectGroup Жетаннотатионбиндекс (D3dx11effect. h)
ms.assetid: 9d3a54b1-384b-4ed4-96a3-09d6bacafda1
keywords:
- Метод Жетаннотатионбиндекс Direct3D 11
- Метод Жетаннотатионбиндекс Direct3D 11, интерфейс ID3DX11EffectGroup
- Интерфейс ID3DX11EffectGroup Direct3D 11, метод Жетаннотатионбиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 663dc8d487552dba521c8e47f9a1eecf6db38122
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273866"
---
# <a name="id3dx11effectgroupgetannotationbyindex-method"></a><span data-ttu-id="c9d97-107">Метод ID3DX11EffectGroup:: Жетаннотатионбиндекс</span><span class="sxs-lookup"><span data-stu-id="c9d97-107">ID3DX11EffectGroup::GetAnnotationByIndex method</span></span>

<span data-ttu-id="c9d97-108">Получение заметки по индексу.</span><span class="sxs-lookup"><span data-stu-id="c9d97-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d97-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9d97-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="c9d97-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9d97-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9d97-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="c9d97-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="c9d97-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c9d97-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c9d97-113">Индекс заметки.</span><span class="sxs-lookup"><span data-stu-id="c9d97-113">Index of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9d97-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9d97-114">Return value</span></span>

<span data-ttu-id="c9d97-115">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9d97-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="c9d97-116">Указатель на интерфейс [**ID3DX11EffectVariable**](id3dx11effectvariable.md) .</span><span class="sxs-lookup"><span data-stu-id="c9d97-116">Pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9d97-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="c9d97-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c9d97-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="c9d97-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c9d97-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="c9d97-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c9d97-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c9d97-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9d97-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c9d97-121">Requirements</span></span>



| <span data-ttu-id="c9d97-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c9d97-122">Requirement</span></span> | <span data-ttu-id="c9d97-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c9d97-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d97-124">Header</span><span class="sxs-lookup"><span data-stu-id="c9d97-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c9d97-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d97-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c9d97-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9d97-126">Library</span></span><br/> | <dl> <span data-ttu-id="c9d97-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="c9d97-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d97-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9d97-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d97-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="c9d97-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

