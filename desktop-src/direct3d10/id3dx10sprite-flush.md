---
description: 'Принудительная отправка всех пакетированных спрайтов на устройство. Состояния устройств остаются в том виде, в котором они были после последнего вызова ID3DX10Sprite:: Begin. Затем список пакетных спрайтов удаляется.'
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'Метод ID3DX10Sprite:: Flush (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105714040"
---
# <a name="id3dx10spriteflush-method"></a><span data-ttu-id="ef4d9-105">Метод ID3DX10Sprite:: Flush</span><span class="sxs-lookup"><span data-stu-id="ef4d9-105">ID3DX10Sprite::Flush method</span></span>

<span data-ttu-id="ef4d9-106">Принудительная отправка всех пакетированных спрайтов на устройство.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-106">Force all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="ef4d9-107">Состояния устройств остаются в том виде, в котором они были после последнего вызова ID3DX10Sprite:: Begin.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-107">Device states remain as they were after the last call to ID3DX10Sprite::Begin.</span></span> <span data-ttu-id="ef4d9-108">Затем список пакетных спрайтов удаляется.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef4d9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef4d9-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="ef4d9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef4d9-110">Parameters</span></span>

<span data-ttu-id="ef4d9-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef4d9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef4d9-112">Return value</span></span>

<span data-ttu-id="ef4d9-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef4d9-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef4d9-114">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="ef4d9-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ef4d9-115">Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef4d9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ef4d9-116">Requirements</span></span>



| <span data-ttu-id="ef4d9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ef4d9-117">Requirement</span></span> | <span data-ttu-id="ef4d9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ef4d9-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4d9-119">Header</span><span class="sxs-lookup"><span data-stu-id="ef4d9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ef4d9-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef4d9-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef4d9-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ef4d9-121">Library</span></span><br/> | <dl> <span data-ttu-id="ef4d9-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef4d9-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef4d9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef4d9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef4d9-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="ef4d9-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="ef4d9-125">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="ef4d9-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




