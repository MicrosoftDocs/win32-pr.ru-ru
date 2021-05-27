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
ms.openlocfilehash: 15a51fdea0d7e579e427ab52af3016e58a39831a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550289"
---
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a><span data-ttu-id="2a902-103">Метод IDWriteBitmapRenderTarget2::-BitmapData (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="2a902-103">IDWriteBitmapRenderTarget2::GetBitmapData method (dwrite_3.h)</span></span>

<span data-ttu-id="2a902-104">Извлекает данные пикселя из целевого объекта прорисовки растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="2a902-104">Retrieves the pixel data from a bitmap render target.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2a902-105">Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2a902-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="2a902-106">DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="2a902-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="2a902-107">Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](../dwritecore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2a902-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a902-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a902-108">Syntax</span></span>

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a><span data-ttu-id="2a902-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a902-109">Parameters</span></span>

`bitmapData`

<span data-ttu-id="2a902-110">Тип: \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a902-110">Type: \_Out\_**[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***</span></span>

<span data-ttu-id="2a902-111">Указатель на данные пикселя.</span><span class="sxs-lookup"><span data-stu-id="2a902-111">A pointer to the pixel data.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a902-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a902-112">Return value</span></span>

<span data-ttu-id="2a902-113">Тип: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="2a902-113">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="2a902-114">Если этот метод завершается с ошибкой, возвращается <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span><span class="sxs-lookup"><span data-stu-id="2a902-114">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="2a902-115">В противном случае возвращается код ошибки <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .</span><span class="sxs-lookup"><span data-stu-id="2a902-115">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="2a902-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="2a902-116">Examples</span></span>

<span data-ttu-id="2a902-117">См. раздел [Обзор двритекоре](../dwritecore-overview.md) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="2a902-117">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a902-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2a902-118">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2a902-119">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="2a902-119">**Minimum supported client**</span></span> | <span data-ttu-id="2a902-120">Windows 10, переобъединение проектов [приложения Win32]</span><span class="sxs-lookup"><span data-stu-id="2a902-120">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="2a902-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="2a902-121">**Header**</span></span> | <span data-ttu-id="2a902-122">dwrite_3. h (включает dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="2a902-122">dwrite_3.h (include dwrite_core.h)</span></span> |
| <span data-ttu-id="2a902-123">**Библиотека**</span><span class="sxs-lookup"><span data-stu-id="2a902-123">**Library**</span></span> | <span data-ttu-id="2a902-124">Дврите. lib</span><span class="sxs-lookup"><span data-stu-id="2a902-124">Dwrite.lib</span></span> |
| <span data-ttu-id="2a902-125">**КОМПОНОВКИ**</span><span class="sxs-lookup"><span data-stu-id="2a902-125">**DLL**</span></span> | <span data-ttu-id="2a902-126">Dwrite.dll</span><span class="sxs-lookup"><span data-stu-id="2a902-126">Dwrite.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="2a902-127">См. также</span><span class="sxs-lookup"><span data-stu-id="2a902-127">See also</span></span>

[<span data-ttu-id="2a902-128">IDWriteBitmapRenderTarget2</span><span class="sxs-lookup"><span data-stu-id="2a902-128">IDWriteBitmapRenderTarget2</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)