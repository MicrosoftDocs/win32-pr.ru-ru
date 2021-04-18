---
description: 'Вызовите его после ID3DX10Sprite:: Flush. Если \_ \_ \_ при вызове ID3DX10Sprite:: Begin было указано состояние Save D3DX10, то этот API восстановит состояние устройства до вызова ID3DX10Sprite:: Begin.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'Метод ID3DX10Sprite:: end (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714041"
---
# <a name="id3dx10spriteend-method"></a><span data-ttu-id="4f236-104">Метод ID3DX10Sprite:: end</span><span class="sxs-lookup"><span data-stu-id="4f236-104">ID3DX10Sprite::End method</span></span>

<span data-ttu-id="4f236-105">Вызовите его после ID3DX10Sprite:: Flush.</span><span class="sxs-lookup"><span data-stu-id="4f236-105">Call this after ID3DX10Sprite::Flush.</span></span> <span data-ttu-id="4f236-106">Если \_ \_ \_ при вызове ID3DX10Sprite:: Begin было указано состояние Save D3DX10, то этот API восстановит состояние устройства до вызова ID3DX10Sprite:: Begin.</span><span class="sxs-lookup"><span data-stu-id="4f236-106">If D3DX10\_SPRITE\_SAVE\_STATE was specified when ID3DX10Sprite::Begin was called, this API will restore the device state to how it was before ID3DX10Sprite::Begin was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f236-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f236-107">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="4f236-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f236-108">Parameters</span></span>

<span data-ttu-id="4f236-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4f236-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f236-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f236-110">Return value</span></span>

<span data-ttu-id="4f236-111">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4f236-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4f236-112">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="4f236-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4f236-113">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="4f236-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f236-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4f236-114">Requirements</span></span>



| <span data-ttu-id="4f236-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4f236-115">Requirement</span></span> | <span data-ttu-id="4f236-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4f236-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f236-117">Header</span><span class="sxs-lookup"><span data-stu-id="4f236-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4f236-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f236-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f236-119">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4f236-119">Library</span></span><br/> | <dl> <span data-ttu-id="4f236-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f236-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f236-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f236-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f236-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="4f236-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="4f236-123">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="4f236-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




