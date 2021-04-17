---
description: Задает координаты текстуры (u, v) каждого шаг текселя.
ms.assetid: b1f8f5d6-568f-4868-87c9-9d6b1034d898
title: 'Метод ID3DXTextureGutterHelper:: Сеттекселмап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ee00394e81dadf147d54dffe0dc02199b2274e9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703940"
---
# <a name="id3dxtexturegutterhelpersettexelmap-method"></a><span data-ttu-id="64881-103">Метод ID3DXTextureGutterHelper:: Сеттекселмап</span><span class="sxs-lookup"><span data-stu-id="64881-103">ID3DXTextureGutterHelper::SetTexelMap method</span></span>

<span data-ttu-id="64881-104">Задает координаты текстуры (u, v) каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="64881-104">Sets the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="64881-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64881-105">Syntax</span></span>


```C++
HRESULT SetTexelMap(
  [in] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="64881-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="64881-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64881-107">*птекселдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="64881-107">*pTexelData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64881-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="64881-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="64881-109">Указатель на расположение в координатах текстуры (u, v), где размещается каждая шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="64881-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64881-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64881-110">Return value</span></span>

<span data-ttu-id="64881-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64881-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64881-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="64881-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="64881-113">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="64881-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="64881-114">Требования</span><span class="sxs-lookup"><span data-stu-id="64881-114">Requirements</span></span>



| <span data-ttu-id="64881-115">Требование</span><span class="sxs-lookup"><span data-stu-id="64881-115">Requirement</span></span> | <span data-ttu-id="64881-116">Значение</span><span class="sxs-lookup"><span data-stu-id="64881-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64881-117">Header</span><span class="sxs-lookup"><span data-stu-id="64881-117">Header</span></span><br/>  | <dl> <span data-ttu-id="64881-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="64881-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="64881-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="64881-119">Library</span></span><br/> | <dl> <span data-ttu-id="64881-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64881-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64881-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64881-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64881-122">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="64881-122">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




