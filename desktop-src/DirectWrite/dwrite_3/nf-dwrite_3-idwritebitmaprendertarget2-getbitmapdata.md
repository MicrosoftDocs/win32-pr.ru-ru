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
# <a name="idwritebitmaprendertarget2getbitmapdata-method-dwrite_3h"></a>Метод IDWriteBitmapRenderTarget2::-BitmapData (dwrite_3. h)

Извлекает данные пикселя из целевого объекта прорисовки растрового изображения.

> [!IMPORTANT]
> Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md). DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах. Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](../dwritecore-overview.md).

## <a name="syntax"></a>Синтаксис

```cpp
HRESULT GetBitmapData(
  _Out_ DWRITE_BITMAP_DATA_BGRA32* bitmapData
);
```

## <a name="parameters"></a>Параметры

`bitmapData`

Тип: \_ out \_ **[DWRITE_BITMAP_DATA_BGRA32](./ns-dwrite_3-dwrite_bitmap_data_bgra32.md)\***

Указатель на данные пикселя.

## <a name="return-value"></a>Возвращаемое значение

Тип: <b>HRESULT</b>

Если этот метод завершается с ошибкой, возвращается <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. В противном случае возвращается код ошибки <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .

## <a name="examples"></a>Примеры

См. раздел [Обзор двритекоре](../dwritecore-overview.md) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, переобъединение проектов [приложения Win32] |
| **Header** | dwrite_3. h (включает dwrite_core. h) |
| **Библиотека** | Дврите. lib |
| **КОМПОНОВКИ** | Dwrite.dll |

## <a name="see-also"></a>См. также

[IDWriteBitmapRenderTarget2](/windows/win32/api/dwrite_1/nn-dwrite_3-idwritebitmaprendertarget2)