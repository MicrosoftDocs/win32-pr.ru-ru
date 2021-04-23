---
title: Метод ID3DX11EffectTechnique Жетпассбинаме (D3dx11effect. h)
description: Получение передачи по имени.
ms.assetid: 07c7502e-2af9-4898-8cd4-106d6814fb85
keywords:
- Метод Жетпассбинаме Direct3D 11
- Метод Жетпассбинаме Direct3D 11, интерфейс ID3DX11EffectTechnique
- Интерфейс ID3DX11EffectTechnique Direct3D 11, метод Жетпассбинаме
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetPassByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84bbe9b954efff12e458ee6172665118a7b8ede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998486"
---
# <a name="id3dx11effecttechniquegetpassbyname-method"></a><span data-ttu-id="bf8bc-106">Метод ID3DX11EffectTechnique:: Жетпассбинаме</span><span class="sxs-lookup"><span data-stu-id="bf8bc-106">ID3DX11EffectTechnique::GetPassByName method</span></span>

<span data-ttu-id="bf8bc-107">Получение передачи по имени.</span><span class="sxs-lookup"><span data-stu-id="bf8bc-107">Get a pass by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf8bc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf8bc-108">Syntax</span></span>


```C++
ID3DX11EffectPass* GetPassByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="bf8bc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf8bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf8bc-110">*имя*;</span><span class="sxs-lookup"><span data-stu-id="bf8bc-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="bf8bc-111">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bf8bc-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bf8bc-112">Имя прохода.</span><span class="sxs-lookup"><span data-stu-id="bf8bc-112">The name of the pass.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf8bc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf8bc-113">Return value</span></span>

<span data-ttu-id="bf8bc-114">Тип: **[ **ID3DX11EffectPass**](id3dx11effectpass.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf8bc-114">Type: **[**ID3DX11EffectPass**](id3dx11effectpass.md)\***</span></span>

<span data-ttu-id="bf8bc-115">Указатель на [**ID3DX11EffectPass**](id3dx11effectpass.md).</span><span class="sxs-lookup"><span data-stu-id="bf8bc-115">A pointer to an [**ID3DX11EffectPass**](id3dx11effectpass.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf8bc-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf8bc-116">Remarks</span></span>

<span data-ttu-id="bf8bc-117">Метод содержит один или несколько проходов; Получите проход, используя имя или индекс.</span><span class="sxs-lookup"><span data-stu-id="bf8bc-117">A technique contains one or more passes; get a pass using a name or an index.</span></span>

> [!Note]  
> <span data-ttu-id="bf8bc-118">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="bf8bc-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bf8bc-119">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="bf8bc-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bf8bc-120">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bf8bc-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf8bc-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bf8bc-121">Requirements</span></span>



| <span data-ttu-id="bf8bc-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bf8bc-122">Requirement</span></span> | <span data-ttu-id="bf8bc-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bf8bc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf8bc-124">Header</span><span class="sxs-lookup"><span data-stu-id="bf8bc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bf8bc-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf8bc-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bf8bc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf8bc-126">Library</span></span><br/> | <dl> <span data-ttu-id="bf8bc-127"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="bf8bc-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf8bc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf8bc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf8bc-129">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="bf8bc-129">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

