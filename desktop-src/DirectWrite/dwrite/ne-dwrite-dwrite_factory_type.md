---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Указывает тип объекта фабрики DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
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
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 603b2ae525ddc6472a3b8581627f2877e06d1aac
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2020
ms.locfileid: "104071044"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>Перечисление DWRITE_FACTORY_TYPE (дврите. h)

Указывает тип объекта фабрики DirectWrite.

> [!IMPORTANT]
> Этот API доступен как часть реализации Двритекоре класса [DirectWrite](../direct-write-portal.md). DWriteCore — это один из видов DirectWrite, который работает с версиями Windows вплоть до Windows 8 и позволяет использовать его на разных платформах. Дополнительные сведения и примеры кода см. в разделе [двритекоре Overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Синтаксис
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_RESTRICTED
} ;
```

## <a name="constants"></a>Константы

| Имя | Описание |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | Указывает, что фабрика DirectWrite является общей фабрикой и позволяет повторно использовать кэшированные данные шрифтов в нескольких компонентах внутри процесса. Такие фабрики также используют компоненты кэширования шрифтов между процессами для повышения производительности. |
| DWRITE_FACTORY_TYPE_ISOLATED | Указывает, что объект фабрики DirectWrite является изолированным. Объекты, созданные из изолированной фабрики, не взаимодействуют с внутренним состоянием DirectWrite из других компонентов. |
| DWRITE_FACTORY_TYPE_RESTRICTED | Объекты, созданные из ограниченной фабрики, не используют и не изменяют внутреннее состояние или кэшированные данные, используемые другими фабриками. Кроме того, системная коллекция шрифтов содержит только хорошо известные шрифты.|

## <a name="examples"></a>Примеры

См. раздел [Обзор двритекоре](/windows/win32/DirectWrite/dwrite/dwritecore-overview) и пример приложения [двритекорегаллери](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Комментарии

Объект фабрики DirectWrite содержит сведения о его внутреннем состоянии, такие как регистрация загрузчика шрифтов и кэшированные данные шрифта. В большинстве случаев следует использовать объект Shared Factory, так как он позволяет нескольким компонентам, использующим DirectWrite, обмениваться внутренними сведениями о состоянии DirectWrite, тем самым уменьшая использование памяти. Однако бывают случаи, когда желательно уменьшить воздействие компонента на остальную часть процесса, например подключаемый модуль из ненадежного источника, с помощью песочницы и изоляции его от остальных компонентов процесса. В таких случаях для изолированного компонента следует использовать изолированную фабрику.

Ограниченная фабрика больше заблокирована, чем изолированная фабрика. Он не взаимодействует с межпроцессным или постоянным кэшем шрифтов каким-либо образом. Кроме того, системная коллекция шрифтов, возвращаемая из этой фабрики, включает только хорошо известные шрифты. При передаче **DWRITE_FACTORY_TYPE_RESTRICTED** в более раннюю версию дврите, чем Двритекоре, [двритекреатефактори](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) возвращает **E_INVALIDARG**.

## <a name="requirements"></a>Требования
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, предварительная версия проекта Реюньон 0,1 [приложения Win32] |
| **Header** | дврите. h (включает dwrite_core. h) |
