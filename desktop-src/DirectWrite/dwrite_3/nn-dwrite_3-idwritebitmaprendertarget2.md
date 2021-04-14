---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: 32 инкапсулирует независимое от устройства битовое изображение и контекст устройства, которые можно использовать для отрисовки глифов.
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
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
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
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: edc1df695424eac0bbf0d5a4951b5e9fe4ec0809
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104273207"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a>Интерфейс IDWriteBitmapRenderTarget2 (dwrite_3. h)

32 инкапсулирует независимое от устройства битовое изображение и контекст устройства, которые можно использовать для отрисовки глифов.

> [!IMPORTANT]
> Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md). DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах. Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="inheritance"></a>Наследование

Интерфейс **IDWriteBitmapRenderTarget2** наследует от [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).

## <a name="methods"></a>Методы

Интерфейс **IDWriteBitmapRenderTarget2** содержит следующие методы.

| Метод | Описание |
| ---- |:---- |
| [IDWriteBitmapRenderTarget2:: "BitmapData"](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | Извлекает данные пикселя из целевого объекта прорисовки растрового изображения. |

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, предварительная версия проекта Реюньон 0,1 [приложения Win32] |
| **Header** | dwrite_3. h (включает dwrite_core. h) |