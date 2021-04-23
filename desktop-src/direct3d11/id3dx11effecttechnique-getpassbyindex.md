---
title: Метод ID3DX11EffectTechnique Жетпассбиндекс (D3dx11effect. h)
description: Получение передаваемого по индексу.
ms.assetid: 3c9452f5-c94a-4951-bdd2-e8891b7ceb34
keywords:
- Метод Жетпассбиндекс Direct3D 11
- Метод Жетпассбиндекс Direct3D 11, интерфейс ID3DX11EffectTechnique
- Интерфейс ID3DX11EffectTechnique Direct3D 11, метод Жетпассбиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6af222298cc3d00ad87e5037f9de20139e4fc40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000479"
---
# <a name="id3dx11effecttechniquegetpassbyindex-method"></a><span data-ttu-id="1d420-106">Метод ID3DX11EffectTechnique:: Жетпассбиндекс</span><span class="sxs-lookup"><span data-stu-id="1d420-106">ID3DX11EffectTechnique::GetPassByIndex method</span></span>

<span data-ttu-id="1d420-107">Получение передаваемого по индексу.</span><span class="sxs-lookup"><span data-stu-id="1d420-107">Get a pass by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d420-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d420-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="1d420-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d420-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d420-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="1d420-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="1d420-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1d420-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1d420-112">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="1d420-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d420-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d420-113">Return value</span></span>

<span data-ttu-id="1d420-114">Тип: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d420-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="1d420-115">Указатель на [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="1d420-115">A pointer to a [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1d420-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="1d420-116">Remarks</span></span>

<span data-ttu-id="1d420-117">Метод содержит один или несколько проходов; Получите проход, используя имя или индекс.</span><span class="sxs-lookup"><span data-stu-id="1d420-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="1d420-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="1d420-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1d420-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="1d420-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1d420-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1d420-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d420-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1d420-121">Requirements</span></span>



| <span data-ttu-id="1d420-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1d420-122">Requirement</span></span> | <span data-ttu-id="1d420-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1d420-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d420-124">Header</span><span class="sxs-lookup"><span data-stu-id="1d420-124">Header</span></span><br/>  | <dl> <span data-ttu-id="1d420-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d420-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1d420-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d420-126">Library</span></span><br/> | <dl> <span data-ttu-id="1d420-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="1d420-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d420-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d420-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d420-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="1d420-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

