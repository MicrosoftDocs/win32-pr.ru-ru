---
description: Извлекает средние и абстрактные векторы для заданного кластера из сжатого буфера данных ID3DXPRTCompBuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'Метод ID3DXPRTCompBuffer:: Екстрактбасис (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713797"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a><span data-ttu-id="31392-103">Метод ID3DXPRTCompBuffer:: Екстрактбасис</span><span class="sxs-lookup"><span data-stu-id="31392-103">ID3DXPRTCompBuffer::ExtractBasis method</span></span>

<span data-ttu-id="31392-104">Извлекает средние и абстрактные векторы для заданного кластера из сжатого буфера данных [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="31392-104">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="31392-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31392-105">Syntax</span></span>


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a><span data-ttu-id="31392-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31392-107">*Кластер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="31392-107">*Cluster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31392-108">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31392-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31392-109">Кластер, для которого будет извлечена эта базисная единица.</span><span class="sxs-lookup"><span data-stu-id="31392-109">Cluster for which the basis will be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="31392-110">*пклустербасис* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="31392-110">*pClusterBasis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="31392-111">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31392-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31392-112">Указатель на массив базисных данных вектора для кластера.</span><span class="sxs-lookup"><span data-stu-id="31392-112">Pointer to an array of basis vector data for Cluster.</span></span> <span data-ttu-id="31392-113">Размер хранимых данных с плавающей запятой будет следующим: (1 + число векторов PCA на кластер) \* (количество коэффициентов) (количество \* цветовых каналов)</span><span class="sxs-lookup"><span data-stu-id="31392-113">The size of the FLOAT data stored will be: (1 + Number of PCA vectors per cluster) \* (Number of coefficients) \* (Number of color channels)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31392-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31392-114">Return value</span></span>

<span data-ttu-id="31392-115">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31392-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31392-116">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="31392-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="31392-117">Если метод завершается с ошибкой, будет возвращено следующее значение.</span><span class="sxs-lookup"><span data-stu-id="31392-117">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="31392-118">Требования</span><span class="sxs-lookup"><span data-stu-id="31392-118">Requirements</span></span>



| <span data-ttu-id="31392-119">Требование</span><span class="sxs-lookup"><span data-stu-id="31392-119">Requirement</span></span> | <span data-ttu-id="31392-120">Значение</span><span class="sxs-lookup"><span data-stu-id="31392-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31392-121">Header</span><span class="sxs-lookup"><span data-stu-id="31392-121">Header</span></span><br/>  | <dl> <span data-ttu-id="31392-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="31392-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="31392-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="31392-123">Library</span></span><br/> | <dl> <span data-ttu-id="31392-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31392-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31392-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31392-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31392-126">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="31392-126">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
