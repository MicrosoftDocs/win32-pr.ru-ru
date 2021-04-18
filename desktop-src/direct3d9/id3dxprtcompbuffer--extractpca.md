---
description: Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'Метод ID3DXPRTCompBuffer:: Екстрактпка (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713547"
---
# <a name="id3dxprtcompbufferextractpca-method"></a><span data-ttu-id="b1837-103">Метод ID3DXPRTCompBuffer:: Екстрактпка</span><span class="sxs-lookup"><span data-stu-id="b1837-103">ID3DXPRTCompBuffer::ExtractPCA method</span></span>

<span data-ttu-id="b1837-104">Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b1837-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1837-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1837-105">Syntax</span></span>


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a><span data-ttu-id="b1837-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1837-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1837-107">*Стартпка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1837-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1837-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1837-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1837-109">Начальный индекс для коэффициентов проекции PCA для извлечения из буфера.</span><span class="sxs-lookup"><span data-stu-id="b1837-109">Starting index for PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b1837-110">*Нумекстракт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1837-110">*NumExtract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1837-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1837-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1837-112">Число коэффициентов проекции PCA, извлекаемых из буфера.</span><span class="sxs-lookup"><span data-stu-id="b1837-112">Number of PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b1837-113">*ппкакоеффиЦиентс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1837-113">*pPCACoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1837-114">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1837-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b1837-115">Указатель на расположение, в котором написаны коэффициенты для анализа кластеризованных основных компонентов (КПКА).</span><span class="sxs-lookup"><span data-stu-id="b1837-115">Pointer to the location where clustered principal component analysis (CPCA) coefficients are written.</span></span> <span data-ttu-id="b1837-116">Размер записываемых данных — (число выборок) (число образцов) \* (количество коэффициентов PCA).</span><span class="sxs-lookup"><span data-stu-id="b1837-116">The size of the data written is (Number of Samples) \* (Number of PCA Coefficients).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1837-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1837-117">Return value</span></span>

<span data-ttu-id="b1837-118">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1837-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1837-119">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="b1837-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b1837-120">Если метод завершается с ошибкой, будет возвращено следующее значение.</span><span class="sxs-lookup"><span data-stu-id="b1837-120">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1837-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b1837-121">Requirements</span></span>



| <span data-ttu-id="b1837-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b1837-122">Requirement</span></span> | <span data-ttu-id="b1837-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b1837-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1837-124">Header</span><span class="sxs-lookup"><span data-stu-id="b1837-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b1837-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1837-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b1837-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b1837-126">Library</span></span><br/> | <dl> <span data-ttu-id="b1837-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1837-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1837-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1837-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1837-129">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="b1837-129">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
