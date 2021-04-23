---
description: 'Принудительная отправка всех пакетированных спрайтов на устройство. Состояния устройств остаются в том виде, в котором они были после последнего вызова ID3DXSprite:: Begin. Затем список пакетных спрайтов удаляется.'
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'Метод ID3DXSprite:: Flush (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713770"
---
# <a name="id3dxspriteflush-method"></a><span data-ttu-id="71399-105">Метод ID3DXSprite:: Flush</span><span class="sxs-lookup"><span data-stu-id="71399-105">ID3DXSprite::Flush method</span></span>

<span data-ttu-id="71399-106">Принудительная отправка всех пакетированных спрайтов на устройство.</span><span class="sxs-lookup"><span data-stu-id="71399-106">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="71399-107">Состояния устройств остаются в том виде, в котором они были после последнего вызова [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="71399-107">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="71399-108">Затем список пакетных спрайтов удаляется.</span><span class="sxs-lookup"><span data-stu-id="71399-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="71399-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71399-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="71399-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="71399-110">Parameters</span></span>

<span data-ttu-id="71399-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="71399-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="71399-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71399-112">Return value</span></span>

<span data-ttu-id="71399-113">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71399-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71399-114">Если метод выполнен успешно, возвращается значение S \_ .</span><span class="sxs-lookup"><span data-stu-id="71399-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="71399-115">Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="71399-115">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="71399-116">Требования</span><span class="sxs-lookup"><span data-stu-id="71399-116">Requirements</span></span>



| <span data-ttu-id="71399-117">Требование</span><span class="sxs-lookup"><span data-stu-id="71399-117">Requirement</span></span> | <span data-ttu-id="71399-118">Значение</span><span class="sxs-lookup"><span data-stu-id="71399-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="71399-119">Header</span><span class="sxs-lookup"><span data-stu-id="71399-119">Header</span></span><br/>  | <dl> <span data-ttu-id="71399-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="71399-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="71399-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71399-121">Library</span></span><br/> | <dl> <span data-ttu-id="71399-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71399-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="71399-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71399-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71399-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="71399-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="71399-125">**ID3DXSprite:: end**</span><span class="sxs-lookup"><span data-stu-id="71399-125">**ID3DXSprite::End**</span></span>](id3dxsprite--end.md)
</dt> </dl>

 

 




