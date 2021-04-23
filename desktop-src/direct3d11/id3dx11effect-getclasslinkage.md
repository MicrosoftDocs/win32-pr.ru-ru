---
title: Метод ID3DX11Effect Жеткласслинкаже (D3dx11effect. h)
description: Возвращает интерфейс компоновки класса.
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- Метод Жеткласслинкаже Direct3D 11
- Метод Жеткласслинкаже Direct3D 11, интерфейс ID3DX11Effect
- Интерфейс ID3DX11Effect Direct3D 11, метод Жеткласслинкаже
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b19f14794186f85d0a51f21bc6b2759e512998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000331"
---
# <a name="id3dx11effectgetclasslinkage-method"></a><span data-ttu-id="085bb-106">Метод ID3DX11Effect:: Жеткласслинкаже</span><span class="sxs-lookup"><span data-stu-id="085bb-106">ID3DX11Effect::GetClassLinkage method</span></span>

<span data-ttu-id="085bb-107">Возвращает интерфейс компоновки класса.</span><span class="sxs-lookup"><span data-stu-id="085bb-107">Gets a class linkage interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="085bb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="085bb-108">Syntax</span></span>


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a><span data-ttu-id="085bb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="085bb-109">Parameters</span></span>

<span data-ttu-id="085bb-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="085bb-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="085bb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="085bb-111">Return value</span></span>

<span data-ttu-id="085bb-112">Тип: **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span><span class="sxs-lookup"><span data-stu-id="085bb-112">Type: **[**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span></span>

<span data-ttu-id="085bb-113">Возвращает указатель на интерфейс [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) .</span><span class="sxs-lookup"><span data-stu-id="085bb-113">Returns a pointer to an [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="085bb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="085bb-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="085bb-115">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="085bb-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="085bb-116">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="085bb-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="085bb-117">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="085bb-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="085bb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="085bb-118">Requirements</span></span>



| <span data-ttu-id="085bb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="085bb-119">Requirement</span></span> | <span data-ttu-id="085bb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="085bb-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="085bb-121">Header</span><span class="sxs-lookup"><span data-stu-id="085bb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="085bb-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="085bb-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="085bb-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="085bb-123">Library</span></span><br/> | <dl> <span data-ttu-id="085bb-124"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="085bb-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="085bb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="085bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="085bb-126">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="085bb-126">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





