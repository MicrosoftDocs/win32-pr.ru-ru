---
description: Сопоставляет индексы в диапазоне от 0 до 255 с соответствующими состояниями преобразования.
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: Макрос D3DTS_WORLDMATRIX (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547858"
---
# <a name="d3dts_worldmatrix-macro"></a><span data-ttu-id="df6de-103">\_Макрос D3DTS ворлдматрикс</span><span class="sxs-lookup"><span data-stu-id="df6de-103">D3DTS\_WORLDMATRIX macro</span></span>

<span data-ttu-id="df6de-104">Сопоставляет индексы в диапазоне от 0 до 255 с соответствующими состояниями преобразования.</span><span class="sxs-lookup"><span data-stu-id="df6de-104">Maps indices in the range 0 through 255 to the corresponding transform states.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df6de-105">Syntax</span></span>


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a><span data-ttu-id="df6de-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df6de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6de-107">*index*</span><span class="sxs-lookup"><span data-stu-id="df6de-107">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="df6de-108">Значение индекса в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="df6de-108">An index value in the range 0 through 255.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6de-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df6de-109">Return value</span></span>

<span data-ttu-id="df6de-110">Объект [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) , сопоставляемый с данным *индексом*.</span><span class="sxs-lookup"><span data-stu-id="df6de-110">The [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) that maps to the given *index*.</span></span>

## <a name="remarks"></a><span data-ttu-id="df6de-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df6de-111">Remarks</span></span>

<span data-ttu-id="df6de-112">Состояния преобразования в диапазоне от 256 до 511 зарезервированы для хранения до 256 матриц, которые можно индексировать с помощью 8-разрядных индексов.</span><span class="sxs-lookup"><span data-stu-id="df6de-112">Transform states in the range 256 through 511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span>

## <a name="requirements"></a><span data-ttu-id="df6de-113">Требования</span><span class="sxs-lookup"><span data-stu-id="df6de-113">Requirements</span></span>



| <span data-ttu-id="df6de-114">Требование</span><span class="sxs-lookup"><span data-stu-id="df6de-114">Requirement</span></span> | <span data-ttu-id="df6de-115">Значение</span><span class="sxs-lookup"><span data-stu-id="df6de-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df6de-116">Header</span><span class="sxs-lookup"><span data-stu-id="df6de-116">Header</span></span><br/> | <dl> <span data-ttu-id="df6de-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="df6de-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df6de-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df6de-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6de-119">Макросы</span><span class="sxs-lookup"><span data-stu-id="df6de-119">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[<span data-ttu-id="df6de-120">**сеттрансформ**</span><span class="sxs-lookup"><span data-stu-id="df6de-120">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
