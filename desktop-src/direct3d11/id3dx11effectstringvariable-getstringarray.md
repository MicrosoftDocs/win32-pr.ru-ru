---
title: Метод ID3DX11EffectStringVariable Жетстрингаррай (D3dx11effect. h)
description: Получение массива строк.
ms.assetid: 2cc45b2f-1851-49d2-8844-3e249c48f327
keywords:
- Метод Жетстрингаррай Direct3D 11
- Метод Жетстрингаррай Direct3D 11, интерфейс ID3DX11EffectStringVariable
- Интерфейс ID3DX11EffectStringVariable Direct3D 11, метод Жетстрингаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetStringArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2050ebd7c9ae3735385a379e6ef7bdff0e1cfd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986813"
---
# <a name="id3dx11effectstringvariablegetstringarray-method"></a><span data-ttu-id="3b9da-106">Метод ID3DX11EffectStringVariable:: Жетстрингаррай</span><span class="sxs-lookup"><span data-stu-id="3b9da-106">ID3DX11EffectStringVariable::GetStringArray method</span></span>

<span data-ttu-id="3b9da-107">Получение массива строк.</span><span class="sxs-lookup"><span data-stu-id="3b9da-107">Get an array of strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9da-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b9da-108">Syntax</span></span>


```C++
HRESULT GetStringArray(
   LPCSTR *ppStrings,
   UINT   Offset,
   UINT   Count
);
```



## <a name="parameters"></a><span data-ttu-id="3b9da-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b9da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b9da-110">*ппстрингс*</span><span class="sxs-lookup"><span data-stu-id="3b9da-110">*ppStrings*</span></span> 
</dt> <dd>

<span data-ttu-id="3b9da-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="3b9da-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="3b9da-112">Указатель на первую строку в массиве.</span><span class="sxs-lookup"><span data-stu-id="3b9da-112">A pointer to the first string in the array.</span></span>

</dd> <dt>

<span data-ttu-id="3b9da-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3b9da-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3b9da-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3b9da-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3b9da-115">Смещение (в количестве строк) между началом массива и первой строкой, которую необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="3b9da-115">The offset (in number of strings) between the start of the array and the first string to get.</span></span>

</dd> <dt>

<span data-ttu-id="3b9da-116">*Количество*</span><span class="sxs-lookup"><span data-stu-id="3b9da-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3b9da-117">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3b9da-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3b9da-118">Количество строк в возвращаемом массиве.</span><span class="sxs-lookup"><span data-stu-id="3b9da-118">The number of strings in the returned array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b9da-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b9da-119">Return value</span></span>

<span data-ttu-id="3b9da-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b9da-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b9da-121">Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3b9da-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3b9da-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="3b9da-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3b9da-123">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="3b9da-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3b9da-124">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="3b9da-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3b9da-125">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3b9da-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3b9da-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3b9da-126">Requirements</span></span>



| <span data-ttu-id="3b9da-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3b9da-127">Requirement</span></span> | <span data-ttu-id="3b9da-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3b9da-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9da-129">Header</span><span class="sxs-lookup"><span data-stu-id="3b9da-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3b9da-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b9da-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3b9da-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3b9da-131">Library</span></span><br/> | <dl> <span data-ttu-id="3b9da-132"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="3b9da-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9da-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b9da-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9da-134">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="3b9da-134">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

