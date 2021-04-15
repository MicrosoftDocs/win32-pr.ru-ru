---
title: Структура WINBIO_STORAGE_SCHEMA (Винбио \_ types. h)
description: Описание возможностей адаптера биометрического хранилища.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- API структуры WINBIO_STORAGE_SCHEMA биометрическая платформа Windows
- PWINBIO_STORAGE_SCHEMA API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661983"
---
# <a name="winbio_storage_schema-structure"></a>\_ \_ Структура схемы хранилища винбио

Структура **\_ \_ схемы хранилища винбио** описывает возможности использования адаптера биометрического хранилища. Эта структура используется функцией [**винбиоенумдатабасес**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a>Члены

<dl> <dt>

**биометрикфактор**
</dt> <dd>

Тип биометрического измерения, сохраненный в базе данных.

</dd> <dt>

**DatabaseId**
</dt> <dd>

Идентификатор GUID, идентифицирующий базу данных.

</dd> <dt>

**DataFormat**
</dt> <dd>

Идентификатор GUID, определяющий формат шаблонов в базе данных.

</dd> <dt>

**Атрибуты**
</dt> <dd>

Сведения о характеристиках базы данных. Это может быть побитовое **или** для следующих констант.



| Значение                                                                                                                                                                                                                                                                              | Значение                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**Винбио \_ 0xFFFF0000 \_ \_ маска флага базы данных**</dt> <dt></dt> </dl>                | Представляет маску для битов флагов.<br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**Винбио \_ Флаг базы данных \_ \_ Remote**</dt> <dt>0x00020000</dt> </dl>          | База данных находится на удаленном компьютере.<br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**Винбио \_ Флаг базы данных \_ \_ съемный**</dt> <dt>0x00010000</dt> </dl> | База данных находится на съемном носителе.<br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**Винбио \_ Тип базы данных \_ \_ СУБД**</dt> <dt>0x00000002</dt> </dl>                | База данных управляется системой управления базами данных.<br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**Винбио \_ \_ \_ Файл типа базы данных**</dt> <dt>0x00000001</dt> </dl>                | База данных содержится в файле.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**Винбио \_ 0x0000FFFF \_ типа \_ маски базы данных**</dt> <dt></dt> </dl>                | Представляет маску для битов типа.<br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**Винбио \_ \_Тип базы \_ данных**</dt> <dt>onchip</dt> </dl>          | База данных находится на биометрических датчиках.<br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**Винбио \_ \_Смарт- \_ карта типа базы данных**</dt> <dt>0x00000004</dt> </dl> | База данных находится на смарт-карте.<br/>                    |



 

</dd> <dt>

**Равно**
</dt> <dd>

Путь и имя файла базы данных, если она находится на диске компьютера.

</dd> <dt>

**ConnectionString**
</dt> <dd>

Строковое значение, которое может быть отправлено на сервер базы данных для обнаружения базы данных.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры клиентских приложений](client-application-structures.md)
</dt> <dt>

[**винбиоенумдатабасес**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





