---
title: Метод ID3DX11EffectGroup Жеттечникуебинаме (D3dx11effect. h)
description: Получите метод по имени. | Метод ID3DX11EffectGroup Жеттечникуебинаме (D3dx11effect. h)
ms.assetid: 160c6d57-bec4-4718-8fad-fc9c0746736c
keywords:
- Метод Жеттечникуебинаме Direct3D 11
- Метод Жеттечникуебинаме Direct3D 11, интерфейс ID3DX11EffectGroup
- Интерфейс ID3DX11EffectGroup Direct3D 11, метод Жеттечникуебинаме
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetTechniqueByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5121f67345ba863d773d8e7a73a5d6fa8b69895
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986966"
---
# <a name="id3dx11effectgroupgettechniquebyname-method"></a><span data-ttu-id="51156-107">Метод ID3DX11EffectGroup:: Жеттечникуебинаме</span><span class="sxs-lookup"><span data-stu-id="51156-107">ID3DX11EffectGroup::GetTechniqueByName method</span></span>

<span data-ttu-id="51156-108">Получите метод по имени.</span><span class="sxs-lookup"><span data-stu-id="51156-108">Get a technique by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="51156-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51156-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="51156-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="51156-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51156-111">*имя*;</span><span class="sxs-lookup"><span data-stu-id="51156-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="51156-112">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="51156-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="51156-113">Имя метода.</span><span class="sxs-lookup"><span data-stu-id="51156-113">The name of the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51156-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51156-114">Return value</span></span>

<span data-ttu-id="51156-115">Тип: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="51156-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="51156-116">Указатель на [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)или **значение NULL** , если метод не найден.</span><span class="sxs-lookup"><span data-stu-id="51156-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md), or **NULL** if the technique is not found.</span></span>

## <a name="remarks"></a><span data-ttu-id="51156-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="51156-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="51156-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="51156-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="51156-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="51156-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="51156-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="51156-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51156-121">Требования</span><span class="sxs-lookup"><span data-stu-id="51156-121">Requirements</span></span>



| <span data-ttu-id="51156-122">Требование</span><span class="sxs-lookup"><span data-stu-id="51156-122">Requirement</span></span> | <span data-ttu-id="51156-123">Значение</span><span class="sxs-lookup"><span data-stu-id="51156-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51156-124">Header</span><span class="sxs-lookup"><span data-stu-id="51156-124">Header</span></span><br/>  | <dl> <span data-ttu-id="51156-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="51156-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="51156-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="51156-126">Library</span></span><br/> | <dl> <span data-ttu-id="51156-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="51156-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51156-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51156-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51156-129">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="51156-129">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

