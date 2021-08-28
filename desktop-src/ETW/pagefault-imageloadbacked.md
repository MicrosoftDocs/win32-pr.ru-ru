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
ms.openlocfilehash: 75104fcf923ed59bfcc99e214e66a235549b7059ca0e36c41b6f90d308a3efff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811774"
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

## <a name="members"></a>Члены

Класс **PageFault \_ имажелоадбаккед** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

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

## <a name="remarks"></a>Remarks

Событие регистрируется во время создания раздела образа (например, загрузка DLL), когда диспетчер памяти определяет, что образ необходимо скопировать в файл подкачки и запустить из него. Как правило, образы запускаются из исходного файла, но резервное копирование может произойти, когда диспетчер памяти определяет, что исходный файл может быть изменен асинхронно существующими модулями записи или когда исходный файл находится на съемном носителе или удаленном устройстве.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




