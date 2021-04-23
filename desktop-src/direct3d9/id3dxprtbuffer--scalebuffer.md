---
description: Умножает каждое значение в буфере на постоянное значение.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'Метод ID3DXPRTBuffer:: Скалебуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05bdd066f4b7c33ad06f089551f16f0489608c83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694335"
---
# <a name="id3dxprtbufferscalebuffer-method"></a><span data-ttu-id="22688-103">Метод ID3DXPRTBuffer:: Скалебуффер</span><span class="sxs-lookup"><span data-stu-id="22688-103">ID3DXPRTBuffer::ScaleBuffer method</span></span>

<span data-ttu-id="22688-104">Умножает каждое значение в буфере на постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="22688-104">Multiplies every value in the buffer by a constant value.</span></span>

## <a name="syntax"></a><span data-ttu-id="22688-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22688-105">Syntax</span></span>


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="22688-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="22688-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22688-107">*Масштаб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22688-107">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22688-108">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22688-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22688-109">Постоянное значение, используемое для масштабирования буфера.</span><span class="sxs-lookup"><span data-stu-id="22688-109">Constant value used to scale the buffer.</span></span> <span data-ttu-id="22688-110">Каждое значение в буфере заменяется произведением этого значения и исходного значения буфера.</span><span class="sxs-lookup"><span data-stu-id="22688-110">Every value in the buffer is replaced by the product of this value and the original buffer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22688-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22688-111">Return value</span></span>

<span data-ttu-id="22688-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22688-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22688-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="22688-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="22688-114">Если метод завершается с ошибкой, будет возвращено следующее значение.</span><span class="sxs-lookup"><span data-stu-id="22688-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="22688-115">Требования</span><span class="sxs-lookup"><span data-stu-id="22688-115">Requirements</span></span>



| <span data-ttu-id="22688-116">Требование</span><span class="sxs-lookup"><span data-stu-id="22688-116">Requirement</span></span> | <span data-ttu-id="22688-117">Значение</span><span class="sxs-lookup"><span data-stu-id="22688-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22688-118">Header</span><span class="sxs-lookup"><span data-stu-id="22688-118">Header</span></span><br/>  | <dl> <span data-ttu-id="22688-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="22688-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="22688-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="22688-120">Library</span></span><br/> | <dl> <span data-ttu-id="22688-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22688-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22688-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22688-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22688-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="22688-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
