---
description: Переключает режим для отображения линий в стиле OpenGL.
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'Метод ID3DXLine:: Сетгллинес (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 131c472ef4a2254880ef560edccb9c0cf1c8774b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914823"
---
# <a name="id3dxlinesetgllines-method"></a><span data-ttu-id="9129e-103">Метод ID3DXLine:: Сетгллинес</span><span class="sxs-lookup"><span data-stu-id="9129e-103">ID3DXLine::SetGLLines method</span></span>

<span data-ttu-id="9129e-104">Переключает режим для отображения линий в стиле OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9129e-104">Toggles the mode to draw OpenGL-style lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="9129e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9129e-105">Syntax</span></span>


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a><span data-ttu-id="9129e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9129e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9129e-107">*бгллинес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9129e-107">*bGLLines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9129e-108">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9129e-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9129e-109">Переключает рисование линий в стиле OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9129e-109">Toggles OpenGL-style line drawing.</span></span> <span data-ttu-id="9129e-110">**True** включает линии в стиле OpenGL и **false** включает линии в стиле Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9129e-110">**TRUE** enables OpenGL-style lines, and **FALSE** enables Direct3D-style lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9129e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9129e-111">Return value</span></span>

<span data-ttu-id="9129e-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9129e-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9129e-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="9129e-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9129e-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="9129e-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="9129e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9129e-115">Requirements</span></span>



| <span data-ttu-id="9129e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9129e-116">Requirement</span></span> | <span data-ttu-id="9129e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9129e-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9129e-118">Header</span><span class="sxs-lookup"><span data-stu-id="9129e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9129e-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9129e-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9129e-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9129e-120">Library</span></span><br/> | <dl> <span data-ttu-id="9129e-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9129e-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9129e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9129e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9129e-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="9129e-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
