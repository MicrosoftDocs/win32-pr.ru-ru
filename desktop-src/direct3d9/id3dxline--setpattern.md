---
description: Применяет к строке шаблон стиппле.
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'Метод ID3DXLine:: Сетпаттерн (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80a0485991bc06bdb9fcd3280017d4cc60b492ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157235"
---
# <a name="id3dxlinesetpattern-method"></a><span data-ttu-id="5e7bb-103">Метод ID3DXLine:: Сетпаттерн</span><span class="sxs-lookup"><span data-stu-id="5e7bb-103">ID3DXLine::SetPattern method</span></span>

<span data-ttu-id="5e7bb-104">Применяет к строке шаблон стиппле.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-104">Applies a stipple pattern to the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e7bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e7bb-105">Syntax</span></span>


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a><span data-ttu-id="5e7bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e7bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e7bb-107">*двпаттерн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e7bb-107">*dwPattern* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e7bb-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e7bb-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e7bb-109">Описывает шаблон стиппле: 1 является непрозрачным, 0 является прозрачным.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-109">Describes the stipple pattern: 1 is opaque, 0 is transparent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e7bb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e7bb-110">Return value</span></span>

<span data-ttu-id="5e7bb-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e7bb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e7bb-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5e7bb-113">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="5e7bb-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e7bb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5e7bb-114">Requirements</span></span>



| <span data-ttu-id="5e7bb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5e7bb-115">Requirement</span></span> | <span data-ttu-id="5e7bb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5e7bb-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e7bb-117">Header</span><span class="sxs-lookup"><span data-stu-id="5e7bb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5e7bb-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e7bb-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="5e7bb-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e7bb-119">Library</span></span><br/> | <dl> <span data-ttu-id="5e7bb-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e7bb-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e7bb-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e7bb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e7bb-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="5e7bb-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
