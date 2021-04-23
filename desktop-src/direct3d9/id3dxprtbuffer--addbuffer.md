---
description: Добавляет еще один буфер в ID3DXPRTBuffer и сохраняет результаты в ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'Метод ID3DXPRTBuffer:: Аддбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 90b86ad3d5d9fe5aa65db722757bdb34574a1006
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704025"
---
# <a name="id3dxprtbufferaddbuffer-method"></a><span data-ttu-id="869f0-103">Метод ID3DXPRTBuffer:: Аддбуффер</span><span class="sxs-lookup"><span data-stu-id="869f0-103">ID3DXPRTBuffer::AddBuffer method</span></span>

<span data-ttu-id="869f0-104">Добавляет еще один буфер в [**ID3DXPRTBuffer**](id3dxprtbuffer.md) и сохраняет результаты в **ID3DXPRTBuffer**.</span><span class="sxs-lookup"><span data-stu-id="869f0-104">Adds another buffer to the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and stores the results in **ID3DXPRTBuffer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="869f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="869f0-105">Syntax</span></span>


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="869f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="869f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="869f0-107">*pBuffer* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="869f0-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="869f0-108">Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="869f0-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="869f0-109">Указатель на буфер, содержащий элементы, добавляемые в соответствующие элементы буфера [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="869f0-109">Pointer to a buffer that contains members to be added to the respective members of the [**ID3DXPRTBuffer**](id3dxprtbuffer.md) buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="869f0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="869f0-110">Return value</span></span>

<span data-ttu-id="869f0-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="869f0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="869f0-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="869f0-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="869f0-113">Если метод завершается с ошибкой, будет возвращено следующее значение.</span><span class="sxs-lookup"><span data-stu-id="869f0-113">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="869f0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="869f0-114">Remarks</span></span>

<span data-ttu-id="869f0-115">pBuffer и [**ID3DXPRTBuffer**](id3dxprtbuffer.md) должны иметь одинаковое число выборок, коэффициентов и цветовых каналов. в противном случае метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="869f0-115">pBuffer and [**ID3DXPRTBuffer**](id3dxprtbuffer.md) must have the same number of samples, coefficients, and color channels; the method will fail otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="869f0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="869f0-116">Requirements</span></span>



| <span data-ttu-id="869f0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="869f0-117">Requirement</span></span> | <span data-ttu-id="869f0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="869f0-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="869f0-119">Header</span><span class="sxs-lookup"><span data-stu-id="869f0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="869f0-120"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="869f0-120"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="869f0-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="869f0-121">Library</span></span><br/> | <dl> <span data-ttu-id="869f0-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="869f0-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="869f0-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="869f0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="869f0-124">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="869f0-124">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




