---
description: Этот класс является классом типа события для загрузки изображения в событиях файла подкачки. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: Класс PageFault_ImageLoadBacked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985704"
---
# <a name="pagefault_imageloadbacked-class"></a>\_Класс PageFault имажелоадбаккед

Этот класс является классом типа события для загрузки изображения в событиях файла подкачки.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a>Участники

Класс **PageFault \_ имажелоадбаккед** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **PageFault \_ имажелоадбаккед** имеет следующие свойства.

<dl> <dt>

**девицечар**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Format ("x")
</dt> </dl>

Зарезервировано.

</dd> <dt>

**филечар**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3), Format ("x")
</dt> </dl>

Зарезервировано.

</dd> <dt>

**Закрыт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**FileIo \_ Name**](fileio-name.md) , чтобы определить имя файла.

</dd> <dt>

**лоадфлагс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Format ("x")
</dt> </dl>

Зарезервировано.

</dd> </dl>

## <a name="remarks"></a>Примечания

Событие регистрируется во время создания раздела образа (например, загрузка DLL), когда диспетчер памяти определяет, что образ необходимо скопировать в файл подкачки и запустить из него. Как правило, образы запускаются из исходного файла, но резервное копирование может произойти, когда диспетчер памяти определяет, что исходный файл может быть изменен асинхронно существующими модулями записи или когда исходный файл находится на съемном носителе или удаленном устройстве.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




