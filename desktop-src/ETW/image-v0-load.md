---
description: Этот класс является классом типа событий для событий загрузки изображения. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: e2836153-8e4f-4c7f-9542-9402ed9e4356
title: Класс Image_V0_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_V0_Load
- Image_V0_Load.BaseAddress
- Image_V0_Load.ModuleSize
- Image_V0_Load.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: b2486e6918884e51a57f077dc9c569f926dc902e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984221"
---
# <a name="image_v0_load-class"></a>Image \_ v0 \_ Load, класс

Этот класс является классом типа событий для событий загрузки изображения.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(10), EventTypeName("Load")]
class Image_V0_Load
{
  uint32 BaseAddress;
  uint32 ModuleSize;
  string ImageFileName;
};
```

## <a name="members"></a>Участники

Класс **image \_ v0 \_ Load** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **image \_ v0 \_ Load** имеет следующие свойства.

<dl> <dt>

BaseAddress
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Базовый адрес приложения, в котором загружается образ.

</dd> <dt>

имажефиленаме
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Имя и расширение файла DLL или исполняемого образа для загрузки.

</dd> <dt>

модулесизе
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Размер изображения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_V0 изображения**](image-v0.md)
</dt> </dl>

 

 




