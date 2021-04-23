---
description: Получение количества рабочих элементов, находящихся в настоящий момент в конвейере потоков.
ms.assetid: 0a3d5a7e-6fa5-4580-8912-c142eb99cef5
title: 'Метод ID3DX10ThreadPump:: Жетворкитемкаунт (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.GetWorkItemCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 71c7bf8f73b79982b933ee5fa0481dc361685682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273971"
---
# <a name="id3dx10threadpumpgetworkitemcount-method"></a><span data-ttu-id="80221-103">Метод ID3DX10ThreadPump:: Жетворкитемкаунт</span><span class="sxs-lookup"><span data-stu-id="80221-103">ID3DX10ThreadPump::GetWorkItemCount method</span></span>

<span data-ttu-id="80221-104">Получение количества рабочих элементов, находящихся в настоящий момент в конвейере потоков.</span><span class="sxs-lookup"><span data-stu-id="80221-104">Get the number of work items currently in the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="80221-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80221-105">Syntax</span></span>


```C++
UINT GetWorkItemCount();
```



## <a name="parameters"></a><span data-ttu-id="80221-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80221-106">Parameters</span></span>

<span data-ttu-id="80221-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="80221-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="80221-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80221-108">Return value</span></span>

<span data-ttu-id="80221-109">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80221-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80221-110">Количество рабочих элементов, которые в настоящий момент находятся в очереди в конвейере потоков.</span><span class="sxs-lookup"><span data-stu-id="80221-110">The number of work items currently queued in the thread pump.</span></span>

## <a name="requirements"></a><span data-ttu-id="80221-111">Требования</span><span class="sxs-lookup"><span data-stu-id="80221-111">Requirements</span></span>



| <span data-ttu-id="80221-112">Требование</span><span class="sxs-lookup"><span data-stu-id="80221-112">Requirement</span></span> | <span data-ttu-id="80221-113">Значение</span><span class="sxs-lookup"><span data-stu-id="80221-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80221-114">Header</span><span class="sxs-lookup"><span data-stu-id="80221-114">Header</span></span><br/>  | <dl> <span data-ttu-id="80221-115"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="80221-115"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="80221-116">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80221-116">Library</span></span><br/> | <dl> <span data-ttu-id="80221-117"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80221-117"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80221-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80221-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80221-119">ID3DX10ThreadPump</span><span class="sxs-lookup"><span data-stu-id="80221-119">ID3DX10ThreadPump</span></span>](id3dx10threadpump.md)
</dt> <dt>

[<span data-ttu-id="80221-120">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="80221-120">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
