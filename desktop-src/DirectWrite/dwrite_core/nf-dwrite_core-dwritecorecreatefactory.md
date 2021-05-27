---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core.h)
description: Создает объект фабрики, который используется для последующего создания отдельных объектов Двритекоре.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
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
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 3ba1b8f6e09212c1ba2f4a0093e2205acaa2e835
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548939"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a>Функция Двритекорекреатефактори (dwrite_core. h)

Создает объект фабрики, который используется для последующего создания отдельных объектов Двритекоре.

> [!IMPORTANT]
> Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md). DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах. Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](../dwritecore-overview.md).

## <a name="syntax"></a>Синтаксис
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a>Параметры

`factoryType`

Тип: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b>

Значение типа, указывающее, будет ли объект фабрики общим, изолированным или ограниченным.

`iid`

Тип: <b>рефиид</b>

Значение идентификатора GUID, идентифицирующее интерфейс фабрики DirectWrite, например __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">идвритефактори</a>).

`factory`

Тип: <b>IUnknown * *</b> .

Адрес указателя на вновь созданный объект фабрики DirectWrite.

## <a name="return-value"></a>Возвращаемое значение

Тип: <b>HRESULT</b>

Если этот метод завершается с ошибкой, возвращается <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. В противном случае возвращается код ошибки <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> .

## <a name="examples"></a>Примеры

См. раздел [Обзор двритекоре](../dwritecore-overview.md) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Комментарии

Это функционально аналогично функции [двритекреатефактори](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) , экспортируемой системной версией DirectWrite. Функция Двритекоре имеет другое имя, чтобы избежать неоднозначности.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, переобъединение проектов [приложения Win32] |
| **Header** | дврите. h (включает dwrite_core. h) |