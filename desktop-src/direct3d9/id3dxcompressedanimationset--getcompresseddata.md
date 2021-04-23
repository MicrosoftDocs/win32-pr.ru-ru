---
description: Возвращает буфер данных, в котором хранятся сжатые данные анимации с помощью ключевых кадров.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: 'Метод ID3DXCompressedAnimationSet:: Жеткомпресседдата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7907daf5db2d03afca310a630f6aeb2dc16c4f22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674706"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a><span data-ttu-id="737ea-103">Метод ID3DXCompressedAnimationSet:: Жеткомпресседдата</span><span class="sxs-lookup"><span data-stu-id="737ea-103">ID3DXCompressedAnimationSet::GetCompressedData method</span></span>

<span data-ttu-id="737ea-104">Возвращает буфер данных, в котором хранятся сжатые данные анимации с помощью ключевых кадров.</span><span class="sxs-lookup"><span data-stu-id="737ea-104">Gets the data buffer that stores compressed key frame animation data.</span></span>

## <a name="syntax"></a><span data-ttu-id="737ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="737ea-105">Syntax</span></span>


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="737ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="737ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="737ea-107">*ппкомпресседдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="737ea-107">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="737ea-108">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="737ea-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="737ea-109">Адрес указателя на буфер данных [**ID3DXBuffer**](id3dxbuffer.md) , который получает сжатые данные анимации по ключевым кадрам.</span><span class="sxs-lookup"><span data-stu-id="737ea-109">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) data buffer that receives compressed key frame animation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="737ea-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="737ea-110">Return value</span></span>

<span data-ttu-id="737ea-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="737ea-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="737ea-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="737ea-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="737ea-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="737ea-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="737ea-114">Требования</span><span class="sxs-lookup"><span data-stu-id="737ea-114">Requirements</span></span>



| <span data-ttu-id="737ea-115">Требование</span><span class="sxs-lookup"><span data-stu-id="737ea-115">Requirement</span></span> | <span data-ttu-id="737ea-116">Значение</span><span class="sxs-lookup"><span data-stu-id="737ea-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="737ea-117">Header</span><span class="sxs-lookup"><span data-stu-id="737ea-117">Header</span></span><br/>  | <dl> <span data-ttu-id="737ea-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="737ea-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="737ea-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="737ea-119">Library</span></span><br/> | <dl> <span data-ttu-id="737ea-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="737ea-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="737ea-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="737ea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737ea-122">ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="737ea-122">ID3DXCompressedAnimationSet</span></span>](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




