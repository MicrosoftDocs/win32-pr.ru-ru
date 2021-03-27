---
title: Метод ID3DX11Effect Жетграупбиндекс (D3dx11effect. h)
description: Возвращает группу эффектов по индексу.
ms.assetid: b38ecdbf-0920-48ff-a599-9629a3581d75
keywords:
- Метод Жетграупбиндекс Direct3D 11
- Метод Жетграупбиндекс Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жетграупбиндекс
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd0f629a60255ed28aa5cc426b99198867e0b23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000467"
---
# <a name="id3dx11effectgetgroupbyindex-method"></a><span data-ttu-id="643c7-106">Метод ID3DX11Effect:: Жетграупбиндекс</span><span class="sxs-lookup"><span data-stu-id="643c7-106">ID3DX11Effect::GetGroupByIndex method</span></span>

<span data-ttu-id="643c7-107">Возвращает группу эффектов по индексу.</span><span class="sxs-lookup"><span data-stu-id="643c7-107">Gets an effect group by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="643c7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="643c7-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="643c7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="643c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="643c7-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="643c7-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="643c7-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="643c7-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="643c7-112">Индекс группы эффектов.</span><span class="sxs-lookup"><span data-stu-id="643c7-112">Index of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="643c7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="643c7-113">Return value</span></span>

<span data-ttu-id="643c7-114">Тип: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="643c7-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="643c7-115">Указатель на интерфейс [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="643c7-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="643c7-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="643c7-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="643c7-117">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="643c7-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="643c7-118">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="643c7-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="643c7-119">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="643c7-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="643c7-120">Требования</span><span class="sxs-lookup"><span data-stu-id="643c7-120">Requirements</span></span>



| <span data-ttu-id="643c7-121">Требование</span><span class="sxs-lookup"><span data-stu-id="643c7-121">Requirement</span></span> | <span data-ttu-id="643c7-122">Значение</span><span class="sxs-lookup"><span data-stu-id="643c7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="643c7-123">Header</span><span class="sxs-lookup"><span data-stu-id="643c7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="643c7-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="643c7-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="643c7-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="643c7-125">Library</span></span><br/> | <dl> <span data-ttu-id="643c7-126"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="643c7-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="643c7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="643c7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643c7-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="643c7-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

