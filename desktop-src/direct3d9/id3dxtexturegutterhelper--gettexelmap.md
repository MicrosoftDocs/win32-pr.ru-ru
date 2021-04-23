---
description: Извлекает координаты текстуры (u, v) каждого шаг текселя.
ms.assetid: 7d8eecf8-6344-4a48-8338-b92ebb0ab2ef
title: 'Метод ID3DXTextureGutterHelper:: Жеттекселмап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af401eaa98ac4255b15961477b1ba2316e29edf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355000"
---
# <a name="id3dxtexturegutterhelpergettexelmap-method"></a><span data-ttu-id="be075-103">Метод ID3DXTextureGutterHelper:: Жеттекселмап</span><span class="sxs-lookup"><span data-stu-id="be075-103">ID3DXTextureGutterHelper::GetTexelMap method</span></span>

<span data-ttu-id="be075-104">Извлекает координаты текстуры (u, v) каждого шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="be075-104">Retrieves the (u, v) texture coordinates of each texel.</span></span>

## <a name="syntax"></a><span data-ttu-id="be075-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be075-105">Syntax</span></span>


```C++
HRESULT GetTexelMap(
  [out] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a><span data-ttu-id="be075-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be075-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be075-107">*птекселдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="be075-107">*pTexelData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be075-108">Тип: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="be075-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="be075-109">Указатель на расположение в координатах текстуры (u, v), где размещается каждая шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="be075-109">Pointer to the location in pixel (u, v) texture coordinates where each texel is located.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be075-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be075-110">Return value</span></span>

<span data-ttu-id="be075-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be075-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be075-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="be075-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="be075-113">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="be075-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="be075-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be075-114">Remarks</span></span>

<span data-ttu-id="be075-115">Для [**классов 2 и 4 пикселей текстуры**](id3dxtexturegutterhelper.md)возвращенные координаты текстуры (u, v) соответствуют ближайшей точке ближайшего треугольника.</span><span class="sxs-lookup"><span data-stu-id="be075-115">For [**class 2 and 4 texels**](id3dxtexturegutterhelper.md), the returned (u, v) texture coordinates correspond to the closest point on the closest triangle.</span></span>

<span data-ttu-id="be075-116">Приложение должно выделить Птекселдата и управлять им.</span><span class="sxs-lookup"><span data-stu-id="be075-116">The application must allocate and manage pTexelData.</span></span>

## <a name="requirements"></a><span data-ttu-id="be075-117">Требования</span><span class="sxs-lookup"><span data-stu-id="be075-117">Requirements</span></span>



| <span data-ttu-id="be075-118">Требование</span><span class="sxs-lookup"><span data-stu-id="be075-118">Requirement</span></span> | <span data-ttu-id="be075-119">Значение</span><span class="sxs-lookup"><span data-stu-id="be075-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="be075-120">Header</span><span class="sxs-lookup"><span data-stu-id="be075-120">Header</span></span><br/>  | <dl> <span data-ttu-id="be075-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="be075-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="be075-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be075-122">Library</span></span><br/> | <dl> <span data-ttu-id="be075-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be075-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="be075-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be075-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be075-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="be075-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




