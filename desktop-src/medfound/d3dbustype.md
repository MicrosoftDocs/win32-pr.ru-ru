---
description: Указывает тип шины ввода-вывода, используемой графическим адаптером.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Перечисление D3DBUSTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710827"
---
# <a name="d3dbustype-enumeration"></a>Перечисление D3DBUSTYPE

Указывает тип шины ввода-вывода, используемой графическим адаптером.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_**
</dt> <dd>

Указывает тип шины, отличный от перечисленных здесь типов.

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**
</dt> <dd>

Шина PCI.

</dd> <dt>

<span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ пЦикс**
</dt> <dd>

Шина PCI-X.

</dd> <dt>

<span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ пЦиекспресс**
</dt> <dd>

Шина PCI Express.

</dd> <dt>

<span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**
</dt> <dd>

Шина ускорения графического порта (AGP).

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_Модификатор D3DBUSIMPL \_ в \_ \_ наборе микросхем**
</dt> <dd>

Реализация графического адаптера входит в Северный мост набора микросхем материнской платы. Этот флаг подразумевает, что данные никогда не передаются через шину расширения (например, PCI или AGP) при передаче из основной памяти в графический адаптер.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**\_Модификатор D3DBUSIMPL \_ отслеживает \_ на \_ \_ плате \_ \_ микросхемы**
</dt> <dd>

Указывает, что графический адаптер подключен к северному мосту набора микросхем материнской платы с помощью дорожек на материнской плате, и все микросхемы графического адаптера помещаются на материнскую плату. Этот флаг подразумевает, что данные никогда не передаются через шину расширения (например, PCI или AGP) при передаче из основной памяти в графический адаптер.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**\_Модификатор D3DBUSIMPL \_ отслеживает \_ на \_ \_ плате 8 \_ на \_ сокете**
</dt> <dd>

Графический адаптер подключен к северному мосту набора микросхем материнской платы с помощью дорожек на материнской плате, и все микросхемы графического адаптера подключены к материнской плате через сокеты.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_ \_ Соединитель дочерней \_ платы модификатора D3DBUSIMPL \_**
</dt> <dd>

Графический адаптер подключен к материнской плате через соединитель даугхтербоард.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ Соединитель дочерней платы модификатора D3DBUSIMPL \_ \_ \_ внутри \_ \_ Нуае**
</dt> <dd>

Графический адаптер подключен к материнской плате через соединитель даугхтербоард, и графический адаптер находится внутри корпуса, который не доступен пользователю.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Модификатор D3DBUSIMPL \_ не является \_ стандартным**
</dt> <dd>

Задан один из флагов модификатора D3DBUSIMPL \_ \_ \_ xxx.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Можно задать до трех флагов. Флаги в диапазоне от 0x00 до 0x04 (**D3DBUSTYPE \_ xxx**) предоставляют базовый тип шины. Флаги в диапазоне от 0x10000 до 0x50000 **( \_ Модификатор D3DBUSIMPL \_ xxx**) изменяют базовое описание. Драйвер устанавливает один флаг типа Bus и может устанавливать ноль или один флаг модификатора. Если драйвер задает флаг модификатора, он также задает **\_ \_ \_ нестандартный флаг модификатора D3DBUSIMPL** . Флаги объединяются с побитовой **или**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types. h (включение D3d9. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления видео Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




