---
description: 'Метод ID3DXAnimationSet:: callback — получает сведения о конкретном обратном вызове в наборе анимации.'
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
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097542"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="f8275-103">Метод ID3DXAnimationSet:: callback</span><span class="sxs-lookup"><span data-stu-id="f8275-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="f8275-104">Возвращает сведения о конкретном обратном вызове в наборе анимации.</span><span class="sxs-lookup"><span data-stu-id="f8275-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8275-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8275-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="f8275-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8275-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8275-107">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8275-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8275-108">Тип: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8275-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8275-109">Расположение для поиска обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="f8275-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="f8275-110">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8275-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8275-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8275-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8275-112">Флаги поиска обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f8275-112">Callback search flags.</span></span> <span data-ttu-id="f8275-113">Этому параметру можно присвоить сочетание из одного или нескольких флагов [**из \_ \_ флагов поиска D3DXCALLBACK**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f8275-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8275-114">*пкаллбаккпоситион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f8275-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8275-115">Тип: **[ **Double**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8275-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8275-116">Указатель на расположение обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f8275-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="f8275-117">*ппкаллбаккдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f8275-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8275-118">Тип: **[ **лпвоид**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8275-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8275-119">Адрес указателя данных обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f8275-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8275-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8275-120">Return value</span></span>

<span data-ttu-id="f8275-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8275-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8275-122">Возвращаемые значения этого метода реализуются программистом приложения.</span><span class="sxs-lookup"><span data-stu-id="f8275-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="f8275-123">Как правило, если ошибка не возникает, программа возвращает метод, возвращающий D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="f8275-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="f8275-124">В противном случае программа возвращает метод, возвращающий соответствующее сообщение об ошибке из [D3DERR](d3derr.md) или [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="f8275-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8275-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f8275-125">Requirements</span></span>



| <span data-ttu-id="f8275-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f8275-126">Requirement</span></span> | <span data-ttu-id="f8275-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f8275-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8275-128">Header</span><span class="sxs-lookup"><span data-stu-id="f8275-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f8275-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8275-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f8275-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8275-130">Library</span></span><br/> | <dl> <span data-ttu-id="f8275-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8275-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8275-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f8275-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8275-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="f8275-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
