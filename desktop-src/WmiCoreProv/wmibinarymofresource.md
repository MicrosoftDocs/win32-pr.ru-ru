---
description: Поставщик классов WDM определяет класс Вмибинаримофресаурце в \\ корневом \\ пространстве имен WMI для поддержки задачи отслеживания состояния данных в репозитории WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Класс Вмибинаримофресаурце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898098"
---
# <a name="wmibinarymofresource-class"></a>Класс Вмибинаримофресаурце

Поставщик классов WDM определяет класс **вмибинаримофресаурце** в \\ корневом \\ пространстве имен WMI для поддержки задачи отслеживания состояния данных в репозитории WMI.

## <a name="syntax"></a>Синтаксис

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a>Члены

Класс **вмибинаримофресаурце** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **вмибинаримофресаурце** имеет следующие свойства.

<dl> <dt>

**хигхдатетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Старшая половина метки даты и времени.

</dd> <dt>

**ловдатетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Минимальная половина метки даты и времени.

</dd> <dt>

**мофпроцессед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Флаг, указывающий, была ли MOF-файл обработана полностью.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Имя драйвера с поддержкой WDM, который содержит двоичный MOF-файл, успешно скомпилированный в репозитории WMI.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Поставщик классов WDM создает экземпляр **вмибинаримофресаурце** для каждого драйвера WDM, который предоставляет двоичный MOF-файл.

Всякий раз, когда инструментарий WMI Инициализирует поставщик, поставщик сравнивает метку времени с меткой времени файла изображения драйвера. Если метки времени отличаются, WMI повторно компилирует MOF-файл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                     |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поставщик WDM](wdm-provider.md)
</dt> </dl>

 

