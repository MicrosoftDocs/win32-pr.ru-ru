---
description: Извлекает идентификаторы кластеров по образцу из сжатого буфера данных ID3DXPRTCompBuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'Метод ID3DXPRTCompBuffer:: Екстрактклустеридс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714033"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a><span data-ttu-id="1388c-103">Метод ID3DXPRTCompBuffer:: Екстрактклустеридс</span><span class="sxs-lookup"><span data-stu-id="1388c-103">ID3DXPRTCompBuffer::ExtractClusterIDs method</span></span>

<span data-ttu-id="1388c-104">Извлекает идентификаторы кластеров по образцу из сжатого буфера данных [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1388c-104">Extracts the per-sample cluster IDs from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1388c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1388c-105">Syntax</span></span>


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a><span data-ttu-id="1388c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1388c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1388c-107">*пклустеридс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="1388c-107">*pClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1388c-108">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1388c-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1388c-109">Указатель на расположение в памяти, где записываются идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="1388c-109">Pointer to the location in memory where IDs are written.</span></span> <span data-ttu-id="1388c-110">Требуемая длина памяти — это значение, возвращаемое функцией [**ID3DXPRTCompBuffer:: жетнумсамплес**](id3dxprtcompbuffer--getnumsamples.md).</span><span class="sxs-lookup"><span data-stu-id="1388c-110">The length of memory required is the value returned by [**ID3DXPRTCompBuffer::GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1388c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1388c-111">Return value</span></span>

<span data-ttu-id="1388c-112">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1388c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1388c-113">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="1388c-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1388c-114">Если метод завершается с ошибкой, будет возвращено следующее значение.</span><span class="sxs-lookup"><span data-stu-id="1388c-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="1388c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1388c-115">Requirements</span></span>



| <span data-ttu-id="1388c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1388c-116">Requirement</span></span> | <span data-ttu-id="1388c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1388c-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1388c-118">Header</span><span class="sxs-lookup"><span data-stu-id="1388c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1388c-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1388c-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1388c-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1388c-120">Library</span></span><br/> | <dl> <span data-ttu-id="1388c-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1388c-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1388c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1388c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1388c-123">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="1388c-123">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
