---
title: Метод ID3DX11EffectVariable-Element (D3dx11effect. h)
description: Получение элемента массива.
ms.assetid: 3edf2084-570a-4423-8205-0b94a2a0cfde
keywords:
- Метод коэлемента Direct3D 11
- Метод коэлемента Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод WebMethod
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetElement
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b887bb9e4c1d40f4d3eb0d36b9a7b4d2698b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986810"
---
# <a name="id3dx11effectvariablegetelement-method"></a><span data-ttu-id="deecc-106">Метод ID3DX11EffectVariable:: WebMethod</span><span class="sxs-lookup"><span data-stu-id="deecc-106">ID3DX11EffectVariable::GetElement method</span></span>

<span data-ttu-id="deecc-107">Получение элемента массива.</span><span class="sxs-lookup"><span data-stu-id="deecc-107">Get an array element.</span></span>

## <a name="syntax"></a><span data-ttu-id="deecc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="deecc-108">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetElement(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="deecc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="deecc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deecc-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="deecc-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="deecc-111">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="deecc-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="deecc-112">Отсчитываемый от нуля индекс; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="deecc-112">A zero-based index; otherwise 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deecc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="deecc-113">Return value</span></span>

<span data-ttu-id="deecc-114">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="deecc-114">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="deecc-115">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="deecc-115">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="deecc-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="deecc-116">Remarks</span></span>

<span data-ttu-id="deecc-117">Если переменная действия является массивом, используйте этот метод, чтобы вернуть один из элементов.</span><span class="sxs-lookup"><span data-stu-id="deecc-117">If the effect variable is an array, use this method to return one of the elements.</span></span>

> [!Note]  
> <span data-ttu-id="deecc-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="deecc-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="deecc-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="deecc-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="deecc-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="deecc-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="deecc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="deecc-121">Requirements</span></span>



| <span data-ttu-id="deecc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="deecc-122">Requirement</span></span> | <span data-ttu-id="deecc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="deecc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deecc-124">Header</span><span class="sxs-lookup"><span data-stu-id="deecc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="deecc-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="deecc-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="deecc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="deecc-126">Library</span></span><br/> | <dl> <span data-ttu-id="deecc-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="deecc-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deecc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="deecc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deecc-129">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="deecc-129">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

