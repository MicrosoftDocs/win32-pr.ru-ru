---
description: Содержит данные, описывающие эксперт при запуске.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Структура ЕКСПЕРТСТАРТУПИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f49fcf3c87795dbd7c9e65745e1b5560331c96c471d8ff7b2c8a24560b143cb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911054"
---
# <a name="expertstartupinfo-structure"></a>Структура ЕКСПЕРТСТАРТУПИНФО

Структура **експертстартупинфо** содержит данные, описывающие эксперт при запуске.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Флаги**
</dt> <dd>

Флаги, описывающие эксперт.

</dd> <dt>

**хкаптуре**
</dt> <dd>

Обработчик для записи.

</dd> <dt>

**сзкаптурефиле**
</dt> <dd>

Имя файла записи.

</dd> <dt>

**двфраменумбер**
</dt> <dd>

Номер кадра.

</dd> <dt>

**хпротокол**
</dt> <dd>

Обработчик для протокола.

</dd> <dt>

**лппропертинст**
</dt> <dd>

Указатель на структуру [**пропертинст**](propertyinst.md) .

</dd> <dt>

**сбитфиелд**
</dt> <dd> <dl> <dt>

**битнумбер**
</dt> <dd>

Используется только в том случае, если элементу **квалификатора** данных структуры [**пропертинст**](propertyinst.md) задано значение Prop \_ куал \_ flags.

</dd> <dt>

**Системе**
</dt> <dd>

Используется только в том случае, если элементу **квалификатора** данных структуры [**пропертинст**](propertyinst.md) задано значение Prop \_ куал \_ flags.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




