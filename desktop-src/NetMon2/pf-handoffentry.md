---
description: Структура PF \_ хандоффентри определяет протокол, который сетевой монитор добавляет к переданному набору средства синтаксического анализа.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Структура PF_HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: faf98490424754d6ae2223ca063e0e3a4eec69c113b1a220e9657b7db5edbb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778674"
---
# <a name="pf_handoffentry-structure"></a>\_Структура PF хандоффентри

Структура **PF \_ хандоффентри** определяет протокол, который сетевой монитор добавляет к переданному набору средства синтаксического анализа.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a>Члены

<dl> <dt>

**сзинифиле**
</dt> <dd>

Имя INI-файла, связанного с протоколом.

</dd> <dt>

**сзинисектион**
</dt> <dd>

Метка раздела в INI-файле.

</dd> <dt>

**сзпротокол**
</dt> <dd>

Имя протокола.

</dd> <dt>

**двхандоффвалуе**
</dt> <dd>

Значение, связанное с протоколом.

</dd> <dt>

**валуеформатбасе**
</dt> <dd>

Основание числового значения протокола, указанного в **двхандоффвалуе**. Для функции **валуеформатбасе** необходимо задать один из следующих элементов:



| Значение                                                                                                                                                                                                                        | Значение                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**формат переданного \_ значения является \_ \_ \_ неизвестным**</dt> </dl> | Неизвестный базовый<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**формат переданного \_ значения — \_ \_ базовое \_ десятичное**</dt> </dl> | Основание десятичного разделителя<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**формат переданного \_ значения, \_ \_ Базовый \_ Шестнадцатеричный**</dt> </dl>             | Основание шестнадцатеричного<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Массив структур **PF \_ хандоффентри** используется в структуре [PF \_ хандоффсет](pf-handoffset.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[PF \_ хандоффсет](pf-handoffset.md)
</dt> </dl>

 

 




