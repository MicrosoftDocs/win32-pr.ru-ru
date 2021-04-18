---
description: Переключает Сглаживание линии.
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'Метод ID3DXLine:: Сетантиалиас (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893e2061beedb6d45dc86e87903613984e3d1785
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694344"
---
# <a name="id3dxlinesetantialias-method"></a><span data-ttu-id="81b7d-103">Метод ID3DXLine:: Сетантиалиас</span><span class="sxs-lookup"><span data-stu-id="81b7d-103">ID3DXLine::SetAntialias method</span></span>

<span data-ttu-id="81b7d-104">Переключает Сглаживание линии.</span><span class="sxs-lookup"><span data-stu-id="81b7d-104">Toggles line antialiasing.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81b7d-105">Syntax</span></span>


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a><span data-ttu-id="81b7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="81b7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81b7d-107">*бантиалиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81b7d-107">*bAntiAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81b7d-108">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81b7d-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81b7d-109">Включает и выключает сглаживание.</span><span class="sxs-lookup"><span data-stu-id="81b7d-109">Toggles antialiasing on and off.</span></span> <span data-ttu-id="81b7d-110">**True** включает сглаживание, а **значение false** отключает сглаживание.</span><span class="sxs-lookup"><span data-stu-id="81b7d-110">**TRUE** turns antialiasing on, and **FALSE** turns antialiasing off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81b7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81b7d-111">Return value</span></span>

<span data-ttu-id="81b7d-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81b7d-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81b7d-113">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="81b7d-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="81b7d-114">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="81b7d-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="81b7d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="81b7d-115">Requirements</span></span>



| <span data-ttu-id="81b7d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="81b7d-116">Requirement</span></span> | <span data-ttu-id="81b7d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="81b7d-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81b7d-118">Header</span><span class="sxs-lookup"><span data-stu-id="81b7d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="81b7d-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="81b7d-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="81b7d-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81b7d-120">Library</span></span><br/> | <dl> <span data-ttu-id="81b7d-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81b7d-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="81b7d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81b7d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b7d-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="81b7d-123">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="81b7d-124">**ID3DXLine:: Жетантиалиас**</span><span class="sxs-lookup"><span data-stu-id="81b7d-124">**ID3DXLine::GetAntialias**</span></span>](id3dxline--getantialias.md)
</dt> </dl>

 

 
