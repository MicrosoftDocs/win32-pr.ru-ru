---
description: Создание загрузчика с асинхронной памятью.
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: Функция D3DX10CreateAsyncMemoryLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0219026eabfcff6dfcec0df4721716302f09f5e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713759"
---
# <a name="d3dx10createasyncmemoryloader-function"></a><span data-ttu-id="9dd4d-103">Функция D3DX10CreateAsyncMemoryLoader</span><span class="sxs-lookup"><span data-stu-id="9dd4d-103">D3DX10CreateAsyncMemoryLoader function</span></span>

<span data-ttu-id="9dd4d-104">Создание загрузчика с асинхронной памятью.</span><span class="sxs-lookup"><span data-stu-id="9dd4d-104">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd4d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9dd4d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="9dd4d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9dd4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd4d-107">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9dd4d-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd4d-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9dd4d-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9dd4d-109">Указатель на данные.</span><span class="sxs-lookup"><span data-stu-id="9dd4d-109">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="9dd4d-110">*cbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9dd4d-110">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd4d-111">Type: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9dd4d-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9dd4d-112">Размер данных.</span><span class="sxs-lookup"><span data-stu-id="9dd4d-112">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="9dd4d-113">*ппдаталоадер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9dd4d-113">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd4d-114">Тип: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9dd4d-114">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="9dd4d-115">Адрес указателя на обработчик асинхронных данных (см. [**интерфейс ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="9dd4d-115">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd4d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9dd4d-116">Return value</span></span>

<span data-ttu-id="9dd4d-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9dd4d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9dd4d-118">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9dd4d-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd4d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="9dd4d-119">Requirements</span></span>



| <span data-ttu-id="9dd4d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="9dd4d-120">Requirement</span></span> | <span data-ttu-id="9dd4d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="9dd4d-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd4d-122">Header</span><span class="sxs-lookup"><span data-stu-id="9dd4d-122">Header</span></span><br/> | <dl> <span data-ttu-id="9dd4d-123"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd4d-123"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dd4d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9dd4d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd4d-125">Функции общего назначения</span><span class="sxs-lookup"><span data-stu-id="9dd4d-125">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
