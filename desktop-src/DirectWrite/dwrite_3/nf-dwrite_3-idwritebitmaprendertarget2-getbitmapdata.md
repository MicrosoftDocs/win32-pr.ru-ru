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
ms.openlocfilehash: dff9904eef692b3858cc044f7b400a5b3641456a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105719957"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="cb9ee-103">Метод IDWriteBitmapRenderTarget2::-BitmapData (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="cb9ee-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="cb9ee-104">Извлекает данные пикселя из целевого объекта прорисовки растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb9ee-105">Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="cb9ee-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="cb9ee-106">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="cb9ee-107">Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="cb9ee-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb9ee-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb9ee-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="cb9ee-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb9ee-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="cb9ee-110">Тип: \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb9ee-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="cb9ee-111">Указатель на данные пикселя.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb9ee-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb9ee-112">Return value</span></span>

<span data-ttu-id="cb9ee-113">Тип: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="cb9ee-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="cb9ee-114">Если этот метод завершается с ошибкой, возвращается <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="cb9ee-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="cb9ee-115">В противном случае возвращается код ошибки <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="cb9ee-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="cb9ee-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="cb9ee-116">Examples</span></span>

<span data-ttu-id="cb9ee-117">См. раздел [Обзор двритекоре](/windows/win32/DirectWrite/dwrite/dwritecore-overview) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="cb9ee-117">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb9ee-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cb9ee-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cb9ee-119">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="cb9ee-119">**Minimum supported client**</span></span> | <span data-ttu-id="cb9ee-120">Windows 10, предварительная версия проекта Реюньон 0,1 [приложения Win32]</span><span class="sxs-lookup"><span data-stu-id="cb9ee-120">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="cb9ee-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="cb9ee-121">**Header**</span></span> | <span data-ttu-id="cb9ee-122">dwrite_3. h (включает dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="cb9ee-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="cb9ee-123">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="cb9ee-123">**Library**</span></span> | <span data-ttu-id="cb9ee-124">Дврите. lib</span><span class="sxs-lookup"><span data-stu-id="cb9ee-124">Dwrite.lib</span></span> |
| <span data-ttu-id="cb9ee-125">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="cb9ee-125">**DLL**</span></span> | <span data-ttu-id="cb9ee-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="cb9ee-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="cb9ee-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb9ee-127">See also</span></span>

[<span data-ttu-id="cb9ee-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="cb9ee-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)