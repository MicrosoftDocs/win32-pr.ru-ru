---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: Двритекорекреатефактори (dwrite_core. h)
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
ms.openlocfilehash: 6606ad884fd65195e9922d348cc4fe565b95f2ee
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107882145"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a>Функция Двритекорекреатефактори (dwrite_core. h)

Создает объект фабрики, который используется для последующего создания отдельных объектов Двритекоре.

> [!IMPORTANT]
> Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md). DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах. Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

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

См. раздел [Обзор двритекоре](/windows/win32/DirectWrite/dwrite/dwritecore-overview) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Remarks

Это функционально аналогично функции [двритекреатефактори](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) , экспортируемой системной версией DirectWrite. Функция Двритекоре имеет другое имя, чтобы избежать неоднозначности.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, переобъединение проектов [приложения Win32] |
| **Header** | дврите. h (включает dwrite_core. h) |
