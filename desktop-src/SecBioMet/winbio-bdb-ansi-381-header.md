---
title: Структура WINBIO_BDB_ANSI_381_HEADER (Винбио \_ types. h)
description: Указывает сведения о ряде образцов отпечатков пальцев или карманных ПК.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- API структуры WINBIO_BDB_ANSI_381_HEADER биометрическая платформа Windows
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bc9eee5d3ca99799c76b849e7b990eee2b94c61309c4d729f736ad33a00eecc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911282"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>ВИНБИО \_ БДБ \_ ANSI \_ 381, \_ структура заголовка

В **\_ \_ \_ \_ заголовке винбио БДБ ANSI 381** указаны сведения о ряде образцов отпечатков пальцев или карманных ПК.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a>Члены

<dl> <dt>

**RecordLength**
</dt> <dd>

Размер (в байтах) этой структуры плюс размер всех структур [**\_ записи винбио бдб \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) для образцов отпечатка и карманного компьютера, полученных от конечного пользователя. Допустимы только младшие шесть байт.

</dd> <dt>

**форматидентифиер**
</dt> <dd>

Задает формат. В настоящее время это должно быть 0x46495200.

</dd> <dt>

**VersionNumber**
</dt> <dd>

Указывает номер версии. В настоящее время это должно быть 0x30313000, которое соответствует внутреннему 0.1.0.0.

</dd> <dt>

**ProductId**
</dt> <dd>

[**Винбио \_ зарегистрированная структура \_ формата**](winbio-registered-format.md) , которая содержит зарегистрированный формат данных в виде пары "владелец-тип".

</dd> <dt>

**каптуредевицеид**
</dt> <dd>

Содержит идентификатор единицы устройства, используемого для записи образца.

</dd> <dt>

**имажеаккуиситионлевел**
</dt> <dd>

Указывает уровень разрешения, на котором захватывается образец.

</dd> <dt>

**хоризонталсканресолутион**
</dt> <dd>

Задает горизонтальное разрешение сканирования.

</dd> <dt>

**вертикалсканресолутион**
</dt> <dd>

Задает вертикальное разрешение сканирования.

</dd> <dt>

**хоризонталимажересолутион**
</dt> <dd>

Задает горизонтальное разрешение захваченного отпечатка или карманного образа.

</dd> <dt>

**вертикалимажересолутион**
</dt> <dd>

Задает вертикальное разрешение захваченного отпечатка или карманного образа.

</dd> <dt>

**ElementCount**
</dt> <dd>

Число записей Finger или Palm в этой структуре.

</dd> <dt>

**Единицы масштабирования**
</dt> <dd>

Содержит единицу измерения, 1 для сантиметров и 2 для сантиметров.

</dd> <dt>

**пикселдепс**
</dt> <dd>

Указывает число битов в пикселе. Это может быть от 1 до 16 бит на пиксель для цвета.

</dd> <dt>

**имажекомпрессионалг**
</dt> <dd>

Указывает алгоритм, используемый для сжатия изображения пальца или карманного компьютера.

</dd> <dt>

**Reserved**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры клиентских приложений](client-application-structures.md)
</dt> </dl>

 

 





