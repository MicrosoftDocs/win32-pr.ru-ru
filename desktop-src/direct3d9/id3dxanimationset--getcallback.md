---
description: Возвращает сведения о конкретном обратном вызове в наборе анимации.
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'Метод ID3DXAnimationSet:: callback (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4cde6c9d51fd29c0412f33b34ca7bea8260dfea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273963"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="46efe-103">Метод ID3DXAnimationSet:: callback</span><span class="sxs-lookup"><span data-stu-id="46efe-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="46efe-104">Возвращает сведения о конкретном обратном вызове в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="46efe-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="46efe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46efe-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="46efe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="46efe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46efe-107">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46efe-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46efe-108">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46efe-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46efe-109">Расположение для поиска обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="46efe-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="46efe-110">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46efe-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46efe-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46efe-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46efe-112">Флаги поиска обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="46efe-112">Callback search flags.</span></span> <span data-ttu-id="46efe-113">Этому параметру можно присвоить сочетание из одного или нескольких флагов [**из \_ \_ флагов поиска D3DXCALLBACK**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="46efe-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="46efe-114">*пкаллбаккпоситион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46efe-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46efe-115">Тип: **[ **Double**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="46efe-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46efe-116">Указатель на расположение обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="46efe-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="46efe-117">*ппкаллбаккдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46efe-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46efe-118">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="46efe-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="46efe-119">Адрес указателя данных обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="46efe-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46efe-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46efe-120">Return value</span></span>

<span data-ttu-id="46efe-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46efe-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46efe-122">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="46efe-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="46efe-123">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="46efe-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="46efe-124">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке из [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="46efe-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46efe-125">Требования</span><span class="sxs-lookup"><span data-stu-id="46efe-125">Requirements</span></span>



| <span data-ttu-id="46efe-126">Требование</span><span class="sxs-lookup"><span data-stu-id="46efe-126">Requirement</span></span> | <span data-ttu-id="46efe-127">Значение</span><span class="sxs-lookup"><span data-stu-id="46efe-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46efe-128">Header</span><span class="sxs-lookup"><span data-stu-id="46efe-128">Header</span></span><br/>  | <dl> <span data-ttu-id="46efe-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="46efe-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="46efe-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46efe-130">Library</span></span><br/> | <dl> <span data-ttu-id="46efe-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46efe-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46efe-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46efe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46efe-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="46efe-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
