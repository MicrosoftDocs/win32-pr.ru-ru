---
description: Задает толщину линии.
ms.assetid: cedf9217-2b47-40c3-a64c-9872c1083d71
title: 'Метод ID3DXLine:: Сетвидс (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetWidth
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d357d7516233caf6ef9206aa2aecc2a98a435cde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081930"
---
# <a name="id3dxlinesetwidth-method"></a><span data-ttu-id="a4f21-103">Метод ID3DXLine:: Сетвидс</span><span class="sxs-lookup"><span data-stu-id="a4f21-103">ID3DXLine::SetWidth method</span></span>

<span data-ttu-id="a4f21-104">Задает толщину линии.</span><span class="sxs-lookup"><span data-stu-id="a4f21-104">Specifies the thickness of the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f21-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4f21-105">Syntax</span></span>


```C++
HRESULT SetWidth(
  [in] FLOAT fWidth
);
```



## <a name="parameters"></a><span data-ttu-id="a4f21-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4f21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f21-107">*фвидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4f21-107">*fWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f21-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4f21-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4f21-109">Описывает толщину линии.</span><span class="sxs-lookup"><span data-stu-id="a4f21-109">Describes the line width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f21-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4f21-110">Return value</span></span>

<span data-ttu-id="a4f21-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a4f21-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a4f21-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a4f21-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a4f21-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="a4f21-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f21-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a4f21-114">Requirements</span></span>



| <span data-ttu-id="a4f21-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a4f21-115">Requirement</span></span> | <span data-ttu-id="a4f21-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a4f21-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f21-117">Header</span><span class="sxs-lookup"><span data-stu-id="a4f21-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a4f21-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f21-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a4f21-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a4f21-119">Library</span></span><br/> | <dl> <span data-ttu-id="a4f21-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4f21-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4f21-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4f21-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f21-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="a4f21-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
