---
description: Отменяет связь присоединенного объекта ID3DXTextureGutterHelper с объектом ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'Метод ID3DXPRTBuffer:: Релеасегх (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424526"
---
# <a name="id3dxprtbufferreleasegh-method"></a><span data-ttu-id="577d7-103">Метод ID3DXPRTBuffer:: Релеасегх</span><span class="sxs-lookup"><span data-stu-id="577d7-103">ID3DXPRTBuffer::ReleaseGH method</span></span>

<span data-ttu-id="577d7-104">Отменяет связь присоединенного объекта [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) с объектом [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="577d7-104">Unassociates an attached [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object with the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="577d7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="577d7-105">Syntax</span></span>


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a><span data-ttu-id="577d7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="577d7-106">Parameters</span></span>

<span data-ttu-id="577d7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="577d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="577d7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="577d7-108">Return value</span></span>

<span data-ttu-id="577d7-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="577d7-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="577d7-110">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="577d7-110">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="577d7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="577d7-111">Remarks</span></span>

<span data-ttu-id="577d7-112">Этот метод освобождает указатель на интерфейс [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .</span><span class="sxs-lookup"><span data-stu-id="577d7-112">This method releases the pointer to the [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) interface.</span></span>

<span data-ttu-id="577d7-113">Необходимо убедиться, что число вызовов [**ID3DXPRTBuffer:: аттачгх**](id3dxprtbuffer--attachgh.md) соответствует числу вызовов **ID3DXPRTBuffer:: релеасегх** .</span><span class="sxs-lookup"><span data-stu-id="577d7-113">You must ensure that the number of [**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md) calls matches the number of **ID3DXPRTBuffer::ReleaseGH** calls.</span></span> <span data-ttu-id="577d7-114">После вызова **ID3DXPRTBuffer:: релеасегх** указатель ПГХ, возвращенный **ID3DXPRTBuffer:: аттачгх** , больше не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="577d7-114">After calling **ID3DXPRTBuffer::ReleaseGH**, the pGH pointer returned by **ID3DXPRTBuffer::AttachGH** should no longer be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="577d7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="577d7-115">Requirements</span></span>



| <span data-ttu-id="577d7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="577d7-116">Requirement</span></span> | <span data-ttu-id="577d7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="577d7-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="577d7-118">Header</span><span class="sxs-lookup"><span data-stu-id="577d7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="577d7-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="577d7-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="577d7-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="577d7-120">Library</span></span><br/> | <dl> <span data-ttu-id="577d7-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="577d7-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="577d7-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="577d7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577d7-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="577d7-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="577d7-124">**ID3DXPRTBuffer:: Аттачгх**</span><span class="sxs-lookup"><span data-stu-id="577d7-124">**ID3DXPRTBuffer::AttachGH**</span></span>](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




