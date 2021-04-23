---
title: Метод ID3DX11Effect Жеттечникуебиндекс (D3dx11effect. h)
description: Получение методики по индексу. | Метод ID3DX11Effect Жеттечникуебиндекс (D3dx11effect. h)
ms.assetid: ee9c0cc3-0ca1-42e8-bd37-5878fd56cff1
keywords:
- Метод Жеттечникуебиндекс Direct3D 11
- Метод Жеттечникуебиндекс Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жеттечникуебиндекс
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetTechniqueByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81d3be5ec403fb25ab3a49792ed77fd4d96bf571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000466"
---
# <a name="id3dx11effectgettechniquebyindex-method"></a><span data-ttu-id="96e32-107">Метод ID3DX11Effect:: Жеттечникуебиндекс</span><span class="sxs-lookup"><span data-stu-id="96e32-107">ID3DX11Effect::GetTechniqueByIndex method</span></span>

<span data-ttu-id="96e32-108">Получение методики по индексу.</span><span class="sxs-lookup"><span data-stu-id="96e32-108">Get a technique by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="96e32-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96e32-109">Syntax</span></span>


```C++
ID3DX11EffectTechnique* GetTechniqueByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="96e32-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="96e32-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96e32-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="96e32-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="96e32-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="96e32-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="96e32-113">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="96e32-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96e32-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96e32-114">Return value</span></span>

<span data-ttu-id="96e32-115">Тип: **[ **ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span><span class="sxs-lookup"><span data-stu-id="96e32-115">Type: **[**ID3DX11EffectTechnique**](id3dx11effecttechnique.md)\***</span></span>

<span data-ttu-id="96e32-116">Указатель на [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span><span class="sxs-lookup"><span data-stu-id="96e32-116">A pointer to an [**ID3DX11EffectTechnique**](id3dx11effecttechnique.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="96e32-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="96e32-117">Remarks</span></span>

<span data-ttu-id="96e32-118">Результат содержит один или несколько методов. Каждый прием содержит один или несколько проходов.</span><span class="sxs-lookup"><span data-stu-id="96e32-118">An effect contains one or more techniques; each technique contains one or more passes.</span></span> <span data-ttu-id="96e32-119">Можно получить доступ к методу, используя его имя или индекс.</span><span class="sxs-lookup"><span data-stu-id="96e32-119">You can access a technique using its name or with an index.</span></span>

> [!Note]  
> <span data-ttu-id="96e32-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="96e32-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="96e32-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="96e32-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="96e32-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="96e32-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96e32-123">Требования</span><span class="sxs-lookup"><span data-stu-id="96e32-123">Requirements</span></span>



| <span data-ttu-id="96e32-124">Требование</span><span class="sxs-lookup"><span data-stu-id="96e32-124">Requirement</span></span> | <span data-ttu-id="96e32-125">Значение</span><span class="sxs-lookup"><span data-stu-id="96e32-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96e32-126">Header</span><span class="sxs-lookup"><span data-stu-id="96e32-126">Header</span></span><br/>  | <dl> <span data-ttu-id="96e32-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="96e32-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="96e32-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96e32-128">Library</span></span><br/> | <dl> <span data-ttu-id="96e32-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="96e32-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e32-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96e32-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e32-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="96e32-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

