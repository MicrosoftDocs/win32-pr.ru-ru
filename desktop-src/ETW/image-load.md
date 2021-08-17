---
description: Этот класс является классом типа событий для событий изображений. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Класс Image_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 44b957fbc1f8ffad78ec73d03a81fa45a8733a53e0e1d78fb31e48b9129a9e93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394654"
---
# <a name="image_load-class"></a>\_Класс загрузки Image

Этот класс является классом типа событий для событий изображений.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a>Члены

Класс **\_ загрузки Image** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ загрузки Image** имеет следующие свойства.

<dl> <dt>

дефаултбасе
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (7), Pointer
</dt> </dl>

Базовый адрес по умолчанию.

</dd> <dt>

FileName
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (12), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Имя файла и расширение библиотеки DLL или исполняемого образа.

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

имажечекксум
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Контрольная сумма для образа.

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

</dd> <dt>

Reserved0
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6)
</dt> </dl>

Зарезервировано.

</dd> <dt>

Reserved1
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (8)
</dt> </dl>

Зарезервировано.

</dd> <dt>

Reserved2
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (9)
</dt> </dl>

Зарезервировано.

</dd> <dt>

Reserved3
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (10)
</dt> </dl>

Зарезервировано.

</dd> <dt>

Reserved4
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (11)
</dt> </dl>

Зарезервировано.

</dd> <dt>

тимедатестамп
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5)
</dt> </dl>

Время и Дата загрузки или выгрузки изображения.

</dd> </dl>

## <a name="remarks"></a>Remarks

События Дкстарт и Дценд перечисляют все загруженные изображения в начале и в конце трассировки соответственно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Изображение**](image.md)
</dt> <dt>

[**\_V0 изображения**](image-v0.md)
</dt> <dt>

[**Образ \_ v1**](image-v1.md)
</dt> </dl>

 

 




