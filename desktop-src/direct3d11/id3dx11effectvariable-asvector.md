---
title: Метод ID3DX11EffectVariable Асвектор (D3dx11effect. h)
description: Получение переменной Vector.
ms.assetid: 995bd9f3-1417-4048-9a23-4dcb3864c77d
keywords:
- Метод Асвектор Direct3D 11
- Метод Асвектор Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асвектор
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df994536c818461b0307cdee726e704aaaf8a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998714"
---
# <a name="id3dx11effectvariableasvector-method"></a><span data-ttu-id="57ac5-106">Метод ID3DX11EffectVariable:: Асвектор</span><span class="sxs-lookup"><span data-stu-id="57ac5-106">ID3DX11EffectVariable::AsVector method</span></span>

<span data-ttu-id="57ac5-107">Получение переменной Vector.</span><span class="sxs-lookup"><span data-stu-id="57ac5-107">Get a vector variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ac5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57ac5-108">Syntax</span></span>


```C++
ID3DX11EffectVectorVariable* AsVector();
```



## <a name="parameters"></a><span data-ttu-id="57ac5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="57ac5-109">Parameters</span></span>

<span data-ttu-id="57ac5-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="57ac5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="57ac5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57ac5-111">Return value</span></span>

<span data-ttu-id="57ac5-112">Тип: **[ **ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="57ac5-112">Type: **[**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md)\***</span></span>

<span data-ttu-id="57ac5-113">Указатель на переменную Vector.</span><span class="sxs-lookup"><span data-stu-id="57ac5-113">A pointer to a vector variable.</span></span> <span data-ttu-id="57ac5-114">См. [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).</span><span class="sxs-lookup"><span data-stu-id="57ac5-114">See [**ID3DX11EffectVectorVariable**](id3dx11effectvectorvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="57ac5-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="57ac5-115">Remarks</span></span>

<span data-ttu-id="57ac5-116">Асвектор Возвращает версию переменной Effect, которая была специализированной для векторной переменной.</span><span class="sxs-lookup"><span data-stu-id="57ac5-116">AsVector returns a version of the effect variable that has been specialized to a vector variable.</span></span> <span data-ttu-id="57ac5-117">Как и в приведении, эта специализация вернет недопустимый объект, если переменная действия не содержит векторных данных.</span><span class="sxs-lookup"><span data-stu-id="57ac5-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain vector data.</span></span>

<span data-ttu-id="57ac5-118">Приложения могут проверить возвращаемый объект на допустимость, вызвав [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="57ac5-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="57ac5-119">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="57ac5-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="57ac5-120">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="57ac5-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="57ac5-121">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="57ac5-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="57ac5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="57ac5-122">Requirements</span></span>



| <span data-ttu-id="57ac5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="57ac5-123">Requirement</span></span> | <span data-ttu-id="57ac5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="57ac5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ac5-125">Header</span><span class="sxs-lookup"><span data-stu-id="57ac5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="57ac5-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="57ac5-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="57ac5-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="57ac5-127">Library</span></span><br/> | <dl> <span data-ttu-id="57ac5-128"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="57ac5-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ac5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57ac5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ac5-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="57ac5-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





