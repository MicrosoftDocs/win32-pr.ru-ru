---
title: Метод ID3DX11ThreadPump Пуржеаллитемс (D3DX11core. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Удаляет все рабочие элементы из конвейера потоков.
ms.assetid: 41a102af-bb9e-4a5a-a351-de0725e592c4
keywords:
- Метод Пуржеаллитемс Direct3D 11
- Метод Пуржеаллитемс Direct3D 11, интерфейс ID3DX11ThreadPump
- Интерфейс ID3DX11ThreadPump Direct3D 11, метод Пуржеаллитемс
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.PurgeAllItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea889f8dd919235adbd9c31fbfb9b269f89ed888
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998453"
---
# <a name="id3dx11threadpumppurgeallitems-method"></a><span data-ttu-id="ebec0-107">ID3DX11ThreadPump: метод:P Уржеаллитемс</span><span class="sxs-lookup"><span data-stu-id="ebec0-107">ID3DX11ThreadPump::PurgeAllItems method</span></span>

> [!Note]  
> <span data-ttu-id="ebec0-108">Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="ebec0-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="ebec0-109">Удаляет все рабочие элементы из конвейера потоков.</span><span class="sxs-lookup"><span data-stu-id="ebec0-109">Clears all work items from the thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebec0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebec0-110">Syntax</span></span>


```C++
HRESULT PurgeAllItems();
```



## <a name="parameters"></a><span data-ttu-id="ebec0-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ebec0-111">Parameters</span></span>

<span data-ttu-id="ebec0-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ebec0-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ebec0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ebec0-113">Return value</span></span>

<span data-ttu-id="ebec0-114">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ebec0-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ebec0-115">Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ebec0-115">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebec0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ebec0-116">Requirements</span></span>



| <span data-ttu-id="ebec0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ebec0-117">Requirement</span></span> | <span data-ttu-id="ebec0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ebec0-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ebec0-119">Header</span><span class="sxs-lookup"><span data-stu-id="ebec0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ebec0-120"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebec0-120"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="ebec0-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ebec0-121">Library</span></span><br/> | <dl> <span data-ttu-id="ebec0-122"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebec0-122"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ebec0-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebec0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebec0-124">ID3DX11ThreadPump</span><span class="sxs-lookup"><span data-stu-id="ebec0-124">ID3DX11ThreadPump</span></span>](id3dx11threadpump.md)
</dt> <dt>

[<span data-ttu-id="ebec0-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ebec0-125">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





