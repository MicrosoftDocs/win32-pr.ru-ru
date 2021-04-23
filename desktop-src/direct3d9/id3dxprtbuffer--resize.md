---
description: Изменяет число выборок, содержащихся в буфере.
ms.assetid: c3cceba8-0bbc-46e5-95d9-cdf58d8a2510
title: 'Метод ID3DXPRTBuffer:: resize (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.Resize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c54044ffc9e166131faa16c9b438b497c658ef25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694216"
---
# <a name="id3dxprtbufferresize-method"></a><span data-ttu-id="6ee09-103">Метод ID3DXPRTBuffer:: resize</span><span class="sxs-lookup"><span data-stu-id="6ee09-103">ID3DXPRTBuffer::Resize method</span></span>

<span data-ttu-id="6ee09-104">Изменяет число выборок, содержащихся в буфере.</span><span class="sxs-lookup"><span data-stu-id="6ee09-104">Changes the number of samples contained in the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee09-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ee09-105">Syntax</span></span>


```C++
HRESULT Resize(
  [in] UINT NewSize
);
```



## <a name="parameters"></a><span data-ttu-id="6ee09-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ee09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee09-107">*NewSize* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6ee09-107">*NewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee09-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6ee09-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6ee09-109">Число выборок, которые должны содержаться в буфере.</span><span class="sxs-lookup"><span data-stu-id="6ee09-109">Number of samples to be contained in the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee09-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6ee09-110">Return value</span></span>

<span data-ttu-id="6ee09-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6ee09-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6ee09-112">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6ee09-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6ee09-113">Если метод завершается с ошибкой, будет возвращено следующее значение: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="6ee09-113">If the method fails, the following value will be returned, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ee09-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6ee09-114">Requirements</span></span>



| <span data-ttu-id="6ee09-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6ee09-115">Requirement</span></span> | <span data-ttu-id="6ee09-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6ee09-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee09-117">Header</span><span class="sxs-lookup"><span data-stu-id="6ee09-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6ee09-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ee09-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6ee09-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6ee09-119">Library</span></span><br/> | <dl> <span data-ttu-id="6ee09-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ee09-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6ee09-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ee09-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee09-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="6ee09-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
