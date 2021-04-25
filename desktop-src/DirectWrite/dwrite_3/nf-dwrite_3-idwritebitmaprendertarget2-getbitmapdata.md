---
UID: NF:dwrite_3.IDWriteBitmapRenderTarget2.GetBitmapData
title: IDWriteBitmapRenderTarget2::GetBitmapData (dwrite_3.h)
description: Извлекает данные пикселя из целевого объекта прорисовки растрового изображения.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2::GetBitmapData
- dwrite_3/IDWriteBitmapRenderTarget2::GetBitmapData
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2.GetBitmapData
ms.openlocfilehash: f84959338550722d9ce1d2d7097d652fcb140f1f
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955047"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="d3b3e-103">Метод IDWriteBitmapRenderTarget2::-BitmapData (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="d3b3e-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="d3b3e-104">Извлекает данные пикселя из целевого объекта прорисовки растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="d3b3e-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3b3e-105">Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="d3b3e-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="d3b3e-106">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="d3b3e-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="d3b3e-107">Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](/windows/win32/directwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="d3b3e-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b3e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3b3e-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="d3b3e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3b3e-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="d3b3e-110">Тип: \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3b3e-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="d3b3e-111">Указатель на данные пикселя.</span><span class="sxs-lookup"><span data-stu-id="d3b3e-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3b3e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3b3e-112">Return value</span></span>

<span data-ttu-id="d3b3e-113">Тип: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="d3b3e-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="d3b3e-114">Если этот метод завершается с ошибкой, возвращается <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="d3b3e-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="d3b3e-115">В противном случае возвращается код ошибки <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="d3b3e-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="d3b3e-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="d3b3e-116">Examples</span></span>

<span data-ttu-id="d3b3e-117">См. раздел [Обзор двритекоре](/windows/win32/directwrite/dwritecore-overview) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="d3b3e-117">See the [DWriteCore overview](/windows/win32/directwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b3e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d3b3e-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d3b3e-119">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="d3b3e-119">**Minimum supported client**</span></span> | <span data-ttu-id="d3b3e-120">Windows 10, переобъединение проектов [приложения Win32]</span><span class="sxs-lookup"><span data-stu-id="d3b3e-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="d3b3e-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="d3b3e-121">**Header**</span></span> | <span data-ttu-id="d3b3e-122">dwrite_3. h (включает dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="d3b3e-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="d3b3e-123">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="d3b3e-123">**Library**</span></span> | <span data-ttu-id="d3b3e-124">Дврите. lib</span><span class="sxs-lookup"><span data-stu-id="d3b3e-124">Dwrite.lib</span></span> |
| <span data-ttu-id="d3b3e-125">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="d3b3e-125">**DLL**</span></span> | <span data-ttu-id="d3b3e-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="d3b3e-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="d3b3e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="d3b3e-127">See also</span></span>

[<span data-ttu-id="d3b3e-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="d3b3e-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)
