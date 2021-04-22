---
UID: NS:dwrite_3.DWRITE_BITMAP_DATA_BGRA32
title: DWRITE_BITMAP_DATA_BGRA32 (dwrite_3.h)
description: Представляет данные точечного рисунка в формате BGRA32.
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_BITMAP_DATA_BGRA32
- dwrite_3/DWRITE_BITMAP_DATA_BGRA32
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_3.h
api_name:
- DWRITE_BITMAP_DATA_BGRA32
ms.openlocfilehash: 3d5b2168e5154f2e55b6f5acb83897f68d4a029c
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881833"
---
# <a name="dwrite_bitmap_data_bgra32-structure-dwrite_3h"></a>Структура DWRITE_BITMAP_DATA_BGRA32 (dwrite_3. h)

Представляет данные точечного рисунка в формате BGRA32.

> [!IMPORTANT]
> Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md). DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах. Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Синтаксис

```cpp
struct DWRITE_BITMAP_DATA_BGRA32
{
  UINT32 width;
  UINT32 height;
  _Field_size_(width * height) UINT32* pixels;
};
```

## <a name="members"></a>Члены

`width`

Тип: **[UINT32](../../winprog/windows-data-types.md)**

Ширина точечного рисунка в пикселях.


`height`

Тип: **[UINT32](../../winprog/windows-data-types.md)**

Высота точечного рисунка (в пикселях).


`pixels`

Тип: \_ \_ Размер поля \_ (ширина * высота)**[UINT32](../../winprog/windows-data-types.md)\***

Указатель на расположение битовых значений для точечного рисунка.


## <a name="examples"></a>Примеры

См. раздел [Обзор двритекоре](/windows/win32/DirectWrite/dwrite/dwritecore-overview) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, переобъединение проектов [приложения Win32] |
| **Header** | dwrite_3. h (включает dwrite_core. h) |