---
title: Метод ID3DX11EffectVariable Асунордередакцессвиев (D3dx11effect. h)
description: Возвращает неупорядоченную переменную с доступом к представлениям.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Метод Асунордередакцессвиев Direct3D 11
- Метод Асунордередакцессвиев Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асунордередакцессвиев
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b9ce7dbbc99ef16ef3290ec1ba3135a8d2cb05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821540"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a><span data-ttu-id="72f50-106">Метод ID3DX11EffectVariable:: Асунордередакцессвиев</span><span class="sxs-lookup"><span data-stu-id="72f50-106">ID3DX11EffectVariable::AsUnorderedAccessView method</span></span>

<span data-ttu-id="72f50-107">Возвращает неупорядоченную переменную с доступом к представлениям.</span><span class="sxs-lookup"><span data-stu-id="72f50-107">Get an unordered-access-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f50-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72f50-108">Syntax</span></span>


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a><span data-ttu-id="72f50-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="72f50-109">Parameters</span></span>

<span data-ttu-id="72f50-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="72f50-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72f50-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72f50-111">Return value</span></span>

<span data-ttu-id="72f50-112">Тип: **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="72f50-112">Type: **[**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span></span>

<span data-ttu-id="72f50-113">Указатель на переменную неупорядоченного представления доступа.</span><span class="sxs-lookup"><span data-stu-id="72f50-113">A pointer to an unordered-access-view variable.</span></span> <span data-ttu-id="72f50-114">См. [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="72f50-114">See [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="72f50-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="72f50-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="72f50-116">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="72f50-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="72f50-117">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="72f50-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="72f50-118">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="72f50-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72f50-119">Требования</span><span class="sxs-lookup"><span data-stu-id="72f50-119">Requirements</span></span>



| <span data-ttu-id="72f50-120">Требование</span><span class="sxs-lookup"><span data-stu-id="72f50-120">Requirement</span></span> | <span data-ttu-id="72f50-121">Значение</span><span class="sxs-lookup"><span data-stu-id="72f50-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f50-122">Header</span><span class="sxs-lookup"><span data-stu-id="72f50-122">Header</span></span><br/>  | <dl> <span data-ttu-id="72f50-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="72f50-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="72f50-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72f50-124">Library</span></span><br/> | <dl> <span data-ttu-id="72f50-125"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="72f50-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72f50-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72f50-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f50-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="72f50-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





