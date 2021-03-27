---
title: Метод ID3DX11EffectPass Жетаннотатионбинаме (D3dx11effect. h)
description: Получение заметки по имени. | Метод ID3DX11EffectPass Жетаннотатионбинаме (D3dx11effect. h)
ms.assetid: b54a4fb0-62c7-4d96-af30-f9ae04ff7dab
keywords:
- Метод Жетаннотатионбинаме Direct3D 11
- Метод Жетаннотатионбинаме Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Жетаннотатионбинаме
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129f1548e7f63c47906ac736cbddb5f6b2548b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000448"
---
# <a name="id3dx11effectpassgetannotationbyname-method"></a><span data-ttu-id="95159-107">Метод ID3DX11EffectPass:: Жетаннотатионбинаме</span><span class="sxs-lookup"><span data-stu-id="95159-107">ID3DX11EffectPass::GetAnnotationByName method</span></span>

<span data-ttu-id="95159-108">Получение заметки по имени.</span><span class="sxs-lookup"><span data-stu-id="95159-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="95159-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95159-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="95159-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="95159-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95159-111">*имя*;</span><span class="sxs-lookup"><span data-stu-id="95159-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="95159-112">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="95159-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="95159-113">Имя заметки.</span><span class="sxs-lookup"><span data-stu-id="95159-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95159-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95159-114">Return value</span></span>

<span data-ttu-id="95159-115">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="95159-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="95159-116">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="95159-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="95159-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="95159-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95159-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="95159-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="95159-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="95159-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="95159-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="95159-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95159-121">Требования</span><span class="sxs-lookup"><span data-stu-id="95159-121">Requirements</span></span>



| <span data-ttu-id="95159-122">Требование</span><span class="sxs-lookup"><span data-stu-id="95159-122">Requirement</span></span> | <span data-ttu-id="95159-123">Значение</span><span class="sxs-lookup"><span data-stu-id="95159-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95159-124">Header</span><span class="sxs-lookup"><span data-stu-id="95159-124">Header</span></span><br/>  | <dl> <span data-ttu-id="95159-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="95159-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="95159-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95159-126">Library</span></span><br/> | <dl> <span data-ttu-id="95159-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="95159-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95159-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95159-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95159-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="95159-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

