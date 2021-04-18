---
description: Применяет сохраненные данные для переплета текстуры в буфер текстуры ID3DXPRTBuffer.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'Метод ID3DXPRTBuffer:: Евалгх (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704024"
---
# <a name="id3dxprtbufferevalgh-method"></a><span data-ttu-id="02f9c-103">Метод ID3DXPRTBuffer:: Евалгх</span><span class="sxs-lookup"><span data-stu-id="02f9c-103">ID3DXPRTBuffer::EvalGH method</span></span>

<span data-ttu-id="02f9c-104">Применяет сохраненные данные для переплета текстуры в буфер текстуры [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="02f9c-104">Applies stored texture gutter data to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f9c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02f9c-105">Syntax</span></span>


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a><span data-ttu-id="02f9c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="02f9c-106">Parameters</span></span>

<span data-ttu-id="02f9c-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="02f9c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02f9c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02f9c-108">Return value</span></span>

<span data-ttu-id="02f9c-109">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02f9c-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02f9c-110">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="02f9c-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="02f9c-111">Если метод завершается с ошибкой, будет возвращено следующее значение.</span><span class="sxs-lookup"><span data-stu-id="02f9c-111">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="02f9c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02f9c-112">Remarks</span></span>

<span data-ttu-id="02f9c-113">Этот метод выполняет внутренний вызов [**ID3DXTextureGutterHelper:: апплигуттерсфлоат**](id3dxtexturegutterhelper--applyguttersfloat.md) для получения и применения данных для переплета текстуры.</span><span class="sxs-lookup"><span data-stu-id="02f9c-113">This method makes an internal call to [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) to retrieve and apply texture gutter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f9c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="02f9c-114">Requirements</span></span>



| <span data-ttu-id="02f9c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="02f9c-115">Requirement</span></span> | <span data-ttu-id="02f9c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="02f9c-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02f9c-117">Header</span><span class="sxs-lookup"><span data-stu-id="02f9c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="02f9c-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="02f9c-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="02f9c-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="02f9c-119">Library</span></span><br/> | <dl> <span data-ttu-id="02f9c-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02f9c-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02f9c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02f9c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f9c-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="02f9c-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




