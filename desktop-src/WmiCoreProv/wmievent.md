---
description: Класс WMIEvent является базовым классом, из которого производятся все классы событий WMI.
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: Класс WMIEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081354"
---
# <a name="wmievent-class"></a>Класс WMIEvent

Класс **WMIEvent** является базовым классом, из которого производятся все классы событий WMI.

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Члены

Класс **WMIEvent** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **WMIEvent** имеет следующие свойства.

<dl> <dt>

**\_дескриптор безопасности**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие. Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event). Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**ВРЕМЯ \_ создания**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальное значение, указывающее время создания события. Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г. Эти сведения находятся в формате всеобщего скоординированного времени (UTC). Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **WMIEvent** является производным от [**\_ \_ екстринсицевент**](/windows/desktop/WmiSdk/--extrinsicevent).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                                                                                        |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                                                                                  |
| MOF<br/>                      | <dl> <dt>WMI. mof; </dt> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl>                                                                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы МСМКА](msmca-classes.md)
</dt> <dt>

[**\_\_екстринсицевент**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

