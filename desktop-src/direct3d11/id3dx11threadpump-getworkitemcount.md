---
title: Метод ID3DX11ThreadPump Жетворкитемкаунт (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Возвращает количество рабочих элементов в конвейере потока.
ms.assetid: 04883b25-64dc-41a3-849f-710a59e9d3da
keywords:
- Метод Жетворкитемкаунт Direct3D 11
- Метод Жетворкитемкаунт Direct3D 11, интерфейс ID3DX11ThreadPump
- Интерфейс ID3DX11ThreadPump Direct3D 11, метод Жетворкитемкаунт
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetWorkItemCount
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29668e66dd3d8c6d29cbfc69a4ef12a2fdfd18b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986903"
---
# <a name="id3dx11threadpumpgetworkitemcount-method"></a><span data-ttu-id="44b21-107">Метод ID3DX11ThreadPump:: Жетворкитемкаунт</span><span class="sxs-lookup"><span data-stu-id="44b21-107">ID3DX11ThreadPump::GetWorkItemCount method</span></span>

> [!Note]  
> <span data-ttu-id="44b21-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="44b21-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="44b21-109">Возвращает количество рабочих элементов в конвейере потока.</span><span class="sxs-lookup"><span data-stu-id="44b21-109">Gets the number of work items in the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="44b21-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44b21-110">Syntax</span></span>


```C++
UINT GetWorkItemCount();
```



## <a name="parameters"></a><span data-ttu-id="44b21-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="44b21-111">Parameters</span></span>

<span data-ttu-id="44b21-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="44b21-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44b21-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44b21-113">Return value</span></span>

<span data-ttu-id="44b21-114">Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="44b21-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="44b21-115">Количество рабочих элементов, поставленных в конвейер потоков.</span><span class="sxs-lookup"><span data-stu-id="44b21-115">The number of work items queued in the thread pump.</span></span>

## <a name="requirements"></a><span data-ttu-id="44b21-116">Требования</span><span class="sxs-lookup"><span data-stu-id="44b21-116">Requirements</span></span>



| <span data-ttu-id="44b21-117">Требование</span><span class="sxs-lookup"><span data-stu-id="44b21-117">Requirement</span></span> | <span data-ttu-id="44b21-118">Значение</span><span class="sxs-lookup"><span data-stu-id="44b21-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44b21-119">Header</span><span class="sxs-lookup"><span data-stu-id="44b21-119">Header</span></span><br/>  | <dl> <span data-ttu-id="44b21-120"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="44b21-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="44b21-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44b21-121">Library</span></span><br/> | <dl> <span data-ttu-id="44b21-122"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44b21-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="44b21-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44b21-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b21-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="44b21-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="44b21-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="44b21-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

