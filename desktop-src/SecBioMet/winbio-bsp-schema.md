---
title: Структура WINBIO_BSP_SCHEMA (Винбио \_ types. h)
description: Описание возможностей поставщика биометрической службы.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- API структуры WINBIO_BSP_SCHEMA биометрическая платформа Windows
- PWINBIO_BSP_SCHEMA API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff46f5484addb0221d9e441df73ecca3e8283da88ee7849e4362314aa1c375e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080784"
---
# <a name="winbio_bsp_schema-structure"></a>\_ \_ Структура схемы BSP винбио

В **структуре \_ \_ схемы BSP винбио** описываются возможности поставщика биометрической службы. Эта структура используется функцией [**винбиоенумсервицепровидерс**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a>Члены

<dl> <dt>

**биометрикфактор**
</dt> <dd>

Тип биометрического измерения, используемого этим устройством. В настоящее время это должен быть **винбио \_ типа " \_ отпечаток**".

</dd> <dt>

**бспид**
</dt> <dd>

Значение, уникально идентифицирующее этот компонент биометрической службы.

</dd> <dt>

**Описание**
</dt> <dd>

Строка **в Юникоде**, заканчивающаяся нулем, которая содержит описание поставщика биометрической службы.

</dd> <dt>

**поставщик**
</dt> <dd>

Строка **в Юникоде**, заканчивающаяся нулем и содержащая имя поставщика биометрической службы.

</dd> <dt>

**Version**
</dt> <dd>

Структура [**\_ версии винбио**](winbio-version.md) , содержащая версию программного обеспечения компонента биометрической службы поставщика.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры клиентских приложений](client-application-structures.md)
</dt> <dt>

[**винбиоенумсервицепровидерс**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





