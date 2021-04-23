---
title: Метод ID3DX11EffectTechnique Жетаннотатионбинаме (D3dx11effect. h)
description: Получение заметки по имени. | Метод ID3DX11EffectTechnique Жетаннотатионбинаме (D3dx11effect. h)
ms.assetid: 3a9e1fa7-4586-42d6-a723-3140f29a01b4
keywords:
- Метод Жетаннотатионбинаме Direct3D 11
- Метод Жетаннотатионбинаме Direct3D 11, интерфейс ID3DX11EffectTechnique
- Интерфейс ID3DX11EffectTechnique Direct3D 11, метод Жетаннотатионбинаме
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.GetAnnotationByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae5a7c24d392bd034dfcd69fb67723c9492f982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355123"
---
# <a name="id3dx11effecttechniquegetannotationbyname-method"></a><span data-ttu-id="ce342-107">Метод ID3DX11EffectTechnique:: Жетаннотатионбинаме</span><span class="sxs-lookup"><span data-stu-id="ce342-107">ID3DX11EffectTechnique::GetAnnotationByName method</span></span>

<span data-ttu-id="ce342-108">Получение заметки по имени.</span><span class="sxs-lookup"><span data-stu-id="ce342-108">Get an annotation by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce342-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce342-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="ce342-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce342-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce342-111">*имя*;</span><span class="sxs-lookup"><span data-stu-id="ce342-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="ce342-112">Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce342-112">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ce342-113">Имя заметки.</span><span class="sxs-lookup"><span data-stu-id="ce342-113">Name of the annotation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce342-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce342-114">Return value</span></span>

<span data-ttu-id="ce342-115">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="ce342-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="ce342-116">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="ce342-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce342-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce342-117">Remarks</span></span>

<span data-ttu-id="ce342-118">Используйте заметку, чтобы присоединить часть метаданных к приему.</span><span class="sxs-lookup"><span data-stu-id="ce342-118">Use an annotation to attach a piece of metadata to a technique.</span></span>

> [!Note]  
> <span data-ttu-id="ce342-119">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="ce342-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ce342-120">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="ce342-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ce342-121">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ce342-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce342-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ce342-122">Requirements</span></span>



| <span data-ttu-id="ce342-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ce342-123">Requirement</span></span> | <span data-ttu-id="ce342-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ce342-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce342-125">Header</span><span class="sxs-lookup"><span data-stu-id="ce342-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ce342-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce342-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ce342-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ce342-127">Library</span></span><br/> | <dl> <span data-ttu-id="ce342-128"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="ce342-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce342-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce342-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce342-130">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="ce342-130">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

