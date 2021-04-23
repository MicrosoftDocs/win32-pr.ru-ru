---
description: Нормализует все весовые коэффициенты для анализа основных компонентов (PCA), чтобы они были в диапазоне от-1 до 1. Векторы базиса изменяются для отражения этой нормализации.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: 'Метод ID3DXPRTCompBuffer:: Нормализедата (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a69dacb25d04b56a14e27a43487911e56a038ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713933"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a><span data-ttu-id="d22e7-104">Метод ID3DXPRTCompBuffer:: Нормализедата</span><span class="sxs-lookup"><span data-stu-id="d22e7-104">ID3DXPRTCompBuffer::NormalizeData method</span></span>

<span data-ttu-id="d22e7-105">Нормализует все весовые коэффициенты для анализа основных компонентов (PCA), чтобы они были в диапазоне от-1 до 1.</span><span class="sxs-lookup"><span data-stu-id="d22e7-105">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="d22e7-106">Векторы базиса изменяются для отражения этой нормализации.</span><span class="sxs-lookup"><span data-stu-id="d22e7-106">Basis vectors are modified to reflect this normalization.</span></span>

## <a name="syntax"></a><span data-ttu-id="d22e7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d22e7-107">Syntax</span></span>


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a><span data-ttu-id="d22e7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d22e7-108">Parameters</span></span>

<span data-ttu-id="d22e7-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d22e7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d22e7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d22e7-110">Return value</span></span>

<span data-ttu-id="d22e7-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d22e7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d22e7-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="d22e7-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d22e7-113">Если метод завершается с ошибкой, будет возвращено следующее значение.</span><span class="sxs-lookup"><span data-stu-id="d22e7-113">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d22e7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d22e7-114">Requirements</span></span>



| <span data-ttu-id="d22e7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d22e7-115">Requirement</span></span> | <span data-ttu-id="d22e7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d22e7-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d22e7-117">Header</span><span class="sxs-lookup"><span data-stu-id="d22e7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d22e7-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d22e7-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d22e7-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d22e7-119">Library</span></span><br/> | <dl> <span data-ttu-id="d22e7-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d22e7-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d22e7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d22e7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22e7-122">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="d22e7-122">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




