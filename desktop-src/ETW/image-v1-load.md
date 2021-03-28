---
description: Этот класс является классом типа событий для событий загрузки изображения. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 43bf0b2b-3ab4-4561-b48c-65fbace38a79
title: Класс Image_V1_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V1_Load
- Image_V1_Load.ImageBase
- Image_V1_Load.ImageSize
- Image_V1_Load.ProcessId
- Image_V1_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd0a2a61b263ce78c2cf28cdf1cd5df4b702140d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984220"
---
# <a name="image_v1_load-class"></a>Image \_ v1, \_ класс загрузки

Этот класс является классом типа событий для событий загрузки изображения.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V1_Load : Image_V1
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  string FileName;
};
```

## <a name="members"></a>Участники

Класс **\_ \_ загрузки Image v1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ загрузки Image v1** имеет эти свойства.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Имя и расширение файла DLL или исполняемого образа для загрузки.

</dd> <dt>

ImageBase
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Базовый адрес приложения, в котором загружается образ.

</dd> <dt>

ImageSize
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Pointer
</dt> </dl>

Размер загружаемого образа.

При использовании этого свойства тип данных для этого свойства фактически имеет размер \_ t. Квалификатор указателя используется, чтобы определить, равен ли размер \_ t 4-байтам или 8-байтам.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Определяет процесс, в который загружается образ.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Образ \_ v1**](image-v1.md)
</dt> </dl>

 

 




