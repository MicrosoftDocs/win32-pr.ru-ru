---
description: Связывает объект ID3DXTextureGutterHelper с объектом ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'Метод ID3DXPRTBuffer:: Аттачгх (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703870"
---
# <a name="id3dxprtbufferattachgh-method"></a><span data-ttu-id="2136b-103">Метод ID3DXPRTBuffer:: Аттачгх</span><span class="sxs-lookup"><span data-stu-id="2136b-103">ID3DXPRTBuffer::AttachGH method</span></span>

<span data-ttu-id="2136b-104">Связывает объект [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) с объектом [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="2136b-104">Associates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2136b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2136b-105">Syntax</span></span>


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a><span data-ttu-id="2136b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2136b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2136b-107">*ПГХ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2136b-107">*pGH* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2136b-108">Тип: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span><span class="sxs-lookup"><span data-stu-id="2136b-108">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**</span></span>

<span data-ttu-id="2136b-109">Указатель на интерфейс [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) объекта, который содержит данные для переплета текстуры.</span><span class="sxs-lookup"><span data-stu-id="2136b-109">Pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface of an object that contains texture gutter data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2136b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2136b-110">Return value</span></span>

<span data-ttu-id="2136b-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2136b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2136b-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="2136b-112">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2136b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2136b-113">Remarks</span></span>

<span data-ttu-id="2136b-114">Число ссылок объекта [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) будет автоматически увеличиваться на единицу.</span><span class="sxs-lookup"><span data-stu-id="2136b-114">The reference count of the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object will automatically be incremented by one.</span></span> <span data-ttu-id="2136b-115">Все существующие указатели **ID3DXTextureGutterHelper** будут освобождены.</span><span class="sxs-lookup"><span data-stu-id="2136b-115">Any existing **ID3DXTextureGutterHelper** pointers will be released.</span></span>

<span data-ttu-id="2136b-116">Необходимо убедиться, что число вызовов **ID3DXPRTBuffer:: аттачгх** соответствует числу вызовов [**ID3DXPRTBuffer:: релеасегх**](id3dxprtbuffer--releasegh.md) .</span><span class="sxs-lookup"><span data-stu-id="2136b-116">You must ensure that the number of **ID3DXPRTBuffer::AttachGH** calls matches the number of [**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md) calls.</span></span> <span data-ttu-id="2136b-117">После вызова **ID3DXPRTBuffer:: релеасегх** указатель ПГХ, возвращенный **ID3DXPRTBuffer:: аттачгх** , больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="2136b-117">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2136b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2136b-118">Requirements</span></span>



| <span data-ttu-id="2136b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2136b-119">Requirement</span></span> | <span data-ttu-id="2136b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2136b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2136b-121">Header</span><span class="sxs-lookup"><span data-stu-id="2136b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2136b-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2136b-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2136b-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2136b-123">Library</span></span><br/> | <dl> <span data-ttu-id="2136b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2136b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2136b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2136b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2136b-126">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="2136b-126">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="2136b-127">**ID3DXPRTBuffer:: Релеасегх**</span><span class="sxs-lookup"><span data-stu-id="2136b-127">**ID3DXPRTBuffer::ReleaseGH**</span></span>](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




