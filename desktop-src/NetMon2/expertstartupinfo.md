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
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990914"
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



 

 




