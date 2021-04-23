---
title: Метод ID3DX11EffectGroup Жетаннотатионбинаме (D3dx11effect. h)
description: Получение заметки по имени. | Метод ID3DX11EffectGroup Жетаннотатионбинаме (D3dx11effect. h)
ms.assetid: c526a249-fb56-47bb-a0c2-b829a1da88e8
keywords:
- Метод Жетаннотатионбинаме Direct3D 11
- Метод Жетаннотатионбинаме Direct3D 11, интерфейс ID3DX11EffectGroup
- Интерфейс ID3DX11EffectGroup Direct3D 11, метод Жетаннотатионбинаме
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1880983785fcfea8a4cda4aa09c8baec2cfebf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998474"
---
# <a name="id3dx11effectgroupgetannotationbyname-method"></a><span data-ttu-id="bc00c-107">Метод ID3DX11EffectGroup:: Жетаннотатионбинаме</span><span class="sxs-lookup"><span data-stu-id="bc00c-107">ID3DX11EffectGroup::GetAnnotationByName method</span></span>

<span data-ttu-id="bc00c-108">Получение заметки по имени.</span><span class="sxs-lookup"><span data-stu-id="bc00c-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc00c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc00c-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="bc00c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc00c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc00c-111">*имя*;</span><span class="sxs-lookup"><span data-stu-id="bc00c-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="bc00c-112">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bc00c-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bc00c-113">Имя заметки.</span><span class="sxs-lookup"><span data-stu-id="bc00c-113">The name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc00c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bc00c-114">Return value</span></span>

<span data-ttu-id="bc00c-115">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc00c-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="bc00c-116">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="bc00c-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="bc00c-117">Обратите внимание, что если заметка не найдена, возвращаемый **ID3DX11EffectVariable** будет пустым.</span><span class="sxs-lookup"><span data-stu-id="bc00c-117">Note that if the annotation is not found the **ID3DX11EffectVariable** returned will be empty.</span></span> <span data-ttu-id="bc00c-118">Чтобы определить, найдена ли заметка, следует вызвать метод [**ID3DX11EffectVariable:: IsValid**](id3dx11effectvariable-isvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="bc00c-118">The [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md) method should be called to determine whether the annotation was found.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc00c-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="bc00c-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bc00c-120">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="bc00c-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bc00c-121">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="bc00c-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bc00c-122">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="bc00c-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bc00c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="bc00c-123">Requirements</span></span>



| <span data-ttu-id="bc00c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="bc00c-124">Requirement</span></span> | <span data-ttu-id="bc00c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="bc00c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc00c-126">Header</span><span class="sxs-lookup"><span data-stu-id="bc00c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="bc00c-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc00c-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bc00c-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bc00c-128">Library</span></span><br/> | <dl> <span data-ttu-id="bc00c-129"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="bc00c-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc00c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc00c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc00c-131">ID3DX11EffectGroup</span><span class="sxs-lookup"><span data-stu-id="bc00c-131">ID3DX11EffectGroup</span></span>](id3dx11effectgroup.md)
</dt> </dl>

 

