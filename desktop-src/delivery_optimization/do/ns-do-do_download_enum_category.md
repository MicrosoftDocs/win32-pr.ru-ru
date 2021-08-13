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
ms.openlocfilehash: 32bdc7ca9a84bfe87ff453d34c4ecff57a8dabf5f67b21cc0d54ba079efd1578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543766"
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

## <a name="requirements"></a>Requirements (Требования)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Do. h |
