---
description: Представляет DVD-дисковод.
ms.assetid: 6127b58d-c70f-47c7-9eeb-6aff819f672e
title: Класс CIM_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DVDDrive
- CIM_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f21e301150fe0f9f03f62180ac4b42fb19d498724a31ab390ca5c391d7190c6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812615"
---
# <a name="cim_dvddrive-class"></a>\_Класс CIM двддриве

Представляет DVD-дисковод.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_DVDDrive : CIM_MediaAccessDevice
{
  uint16 FormatsSupported[];
};
```

## <a name="members"></a>Члены

Класс **CIM \_ двддриве** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ двддриве** имеет следующие свойства.

<dl> <dt>

**форматссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалмедиа**](/windows/desktop/CIMWin32Prov/cim-physicalmedia).**MediaType**)
</dt> </dl>

Форматы компакт-дисков и DVD-дисков, поддерживаемые устройством.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

**Компакт-** диск (16)


</dt> <dd></dd> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>

**CD-ROM/XA** (17)


</dt> <dd></dd> <dt>

<span id="CD-I"></span><span id="cd-i"></span>

**Компакт-I** (18)


</dt> <dd></dd> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>

**Записываемый компакт-диск** (19)


</dt> <dd></dd> <dt>

<span id="DVD"></span><span id="dvd"></span>

**DVD-диск** (22)


</dt> <dd></dd> <dt>

<span id="DVD-RW_"></span><span id="dvd-rw_"></span>

**DVD-RW +** (23)


</dt> <dd></dd> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>

**DVD-RAM** (24)


</dt> <dd></dd> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>

**DVD-ROM** (25)


</dt> <dd></dd> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>

**DVD-видео** (26)


</dt> <dd></dd> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>

**Дивкс** (27)


</dt> <dd></dd> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>

**CD-RW** (33)


</dt> <dd></dd> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>

**CD-DA** (34)


</dt> <dd></dd> <dt>

<span id="CD_"></span><span id="cd_"></span>

**CD +** (35)


</dt> <dd></dd> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>

**Записываемый DVD-диск** (36)


</dt> <dd></dd> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>

**DVD-RW** (37)


</dt> <dd></dd> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>

**Аудио DVD** (38)


</dt> <dd></dd> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>

**DVD-5** (39)


</dt> <dd></dd> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>

**DVD-9** (40)


</dt> <dd></dd> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>

**DVD-10** (41)


</dt> <dd></dd> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>

**DVD-18** (42)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_МЕДИААКЦЕССДЕВИЦЕ CIM**](cim-mediaaccessdevice.md)
</dt> </dl>

 

