---
description: Возвращает количество элементов в каждой из трех очередей в конвейере потока.
ms.assetid: b5b829a5-5ef7-4ef5-afb4-efe1bb22ae70
title: 'Метод ID3DX10ThreadPump:: Жеткуеуестатус (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetQueueStatus
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4cf3b5879da0346cefbb5b8835d6922dd736cfd3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704014"
---
# <a name="id3dx10threadpumpgetqueuestatus-method"></a><span data-ttu-id="152f5-103">Метод ID3DX10ThreadPump:: Жеткуеуестатус</span><span class="sxs-lookup"><span data-stu-id="152f5-103">ID3DX10ThreadPump::GetQueueStatus method</span></span>

<span data-ttu-id="152f5-104">Возвращает количество элементов в каждой из трех очередей в конвейере потока.</span><span class="sxs-lookup"><span data-stu-id="152f5-104">Get the number of items in each of the three queues inside the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="152f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="152f5-105">Syntax</span></span>


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a><span data-ttu-id="152f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="152f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="152f5-107">*пиокуеуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="152f5-107">*pIoQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="152f5-108">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="152f5-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="152f5-109">Число элементов в очереди ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="152f5-109">Number of items in the I/O queue.</span></span>

</dd> <dt>

<span data-ttu-id="152f5-110">*ппроцесскуеуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="152f5-110">*pProcessQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="152f5-111">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="152f5-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="152f5-112">Число элементов в очереди процессов.</span><span class="sxs-lookup"><span data-stu-id="152f5-112">Number of items in the process queue.</span></span>

</dd> <dt>

<span data-ttu-id="152f5-113">*пдевицекуеуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="152f5-113">*pDeviceQueue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="152f5-114">Тип: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="152f5-114">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="152f5-115">Число элементов в очереди устройства.</span><span class="sxs-lookup"><span data-stu-id="152f5-115">Number of items in the device queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="152f5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="152f5-116">Return value</span></span>

<span data-ttu-id="152f5-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="152f5-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="152f5-118">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="152f5-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="152f5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="152f5-119">Requirements</span></span>



| <span data-ttu-id="152f5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="152f5-120">Requirement</span></span> | <span data-ttu-id="152f5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="152f5-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="152f5-122">Header</span><span class="sxs-lookup"><span data-stu-id="152f5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="152f5-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="152f5-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="152f5-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="152f5-124">Library</span></span><br/> | <dl> <span data-ttu-id="152f5-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="152f5-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152f5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="152f5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152f5-127">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="152f5-127">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="152f5-128">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="152f5-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
