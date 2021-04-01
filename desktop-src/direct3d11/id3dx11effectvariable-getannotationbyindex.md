---
title: Метод ID3DX11EffectVariable Жетаннотатионбиндекс (D3dx11effect. h)
description: Получение заметки по индексу. | Метод ID3DX11EffectVariable Жетаннотатионбиндекс (D3dx11effect. h)
ms.assetid: fc130098-0269-4c78-bc45-284aa0b77865
keywords:
- Метод Жетаннотатионбиндекс Direct3D 11
- Метод Жетаннотатионбиндекс Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Жетаннотатионбиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e13cfcb27e94c64af132e5eec600941d0b41cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157139"
---
# <a name="id3dx11effectvariablegetannotationbyindex-method"></a><span data-ttu-id="8ed92-107">Метод ID3DX11EffectVariable:: Жетаннотатионбиндекс</span><span class="sxs-lookup"><span data-stu-id="8ed92-107">ID3DX11EffectVariable::GetAnnotationByIndex method</span></span>

<span data-ttu-id="8ed92-108">Получение заметки по индексу.</span><span class="sxs-lookup"><span data-stu-id="8ed92-108">Get an annotation by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed92-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ed92-109">Syntax</span></span>


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="8ed92-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ed92-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ed92-111">*Index*</span><span class="sxs-lookup"><span data-stu-id="8ed92-111">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="8ed92-112">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8ed92-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8ed92-113">Отсчитываемый с нуля индекс.</span><span class="sxs-lookup"><span data-stu-id="8ed92-113">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ed92-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ed92-114">Return value</span></span>

<span data-ttu-id="8ed92-115">Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ed92-115">Type: **[**ID3DX11EffectVariable**](id3dx11effectvariable.md)\***</span></span>

<span data-ttu-id="8ed92-116">Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="8ed92-116">A pointer to an [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed92-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ed92-117">Remarks</span></span>

<span data-ttu-id="8ed92-118">Аннонатионс можно подключить к методу, к Pass или к глобальной переменной.</span><span class="sxs-lookup"><span data-stu-id="8ed92-118">Annonations can be attached to a technique, a pass, or a global variable.</span></span>

> [!Note]  
> <span data-ttu-id="8ed92-119">Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов.</span><span class="sxs-lookup"><span data-stu-id="8ed92-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8ed92-120">Для создания приложения типа Effects необходимо использовать исходный текст Effects 11.</span><span class="sxs-lookup"><span data-stu-id="8ed92-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8ed92-121">Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8ed92-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ed92-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8ed92-122">Requirements</span></span>



| <span data-ttu-id="8ed92-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8ed92-123">Requirement</span></span> | <span data-ttu-id="8ed92-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8ed92-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed92-125">Header</span><span class="sxs-lookup"><span data-stu-id="8ed92-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8ed92-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ed92-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8ed92-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8ed92-127">Library</span></span><br/> | <dl> <span data-ttu-id="8ed92-128"><dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt></span><span class="sxs-lookup"><span data-stu-id="8ed92-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ed92-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ed92-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed92-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="8ed92-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

