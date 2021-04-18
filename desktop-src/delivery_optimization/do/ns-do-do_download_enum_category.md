---
title: Структура DO_DOWNLOAD_ENUM_CATEGORY
description: 'Используется **идоманажер:: енумдовнлоадс** для фильтрации перечисления Downloads по значению конкретного свойства.'
keywords:
- Структура DO_DOWNLOAD_ENUM_CATEGORY
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105719081"
---
# <a name="do_download_enum_category-structure"></a>Структура DO_DOWNLOAD_ENUM_CATEGORY

Структура **DO_DOWNLOAD_ENUM_CATEGORY** используется **Идоманажер:: енумдовнлоадс** для фильтрации перечисления Downloads по значению конкретного свойства.

## <a name="syntax"></a>Синтаксис
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a>Члены

`Property`

Имя свойства, используемого для перечисления загрузки. Эти свойства поддерживаются в целях перечисления.
- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`Value`

Значение свойства.

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
