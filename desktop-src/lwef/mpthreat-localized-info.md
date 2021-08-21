---
title: Структура MPTHREAT_LOCALIZED_INFO (Мпклиент. h)
description: Локализованные сведения для угрозы.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO структуры устаревшие функции среды Windows
- функции PMPTHREAT_LOCALIZED_INFO Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff28c77c60421fcaabe31580400ad87823ad3edf3536d96ba3ba5eec177ad94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555954"
---
# <a name="mpthreat_localized_info-structure"></a>\_Локализованная \_ информационная структура мпсреат

Локализованные сведения для угрозы.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**среатид**
</dt> <dd>

Тип: **мпсреат \_ ID**

</dd> <dd>

Идентификатор угрозы. Верхний бит задан для выявления угроз, связанных с антивирусной программой.

</dd> <dt>

**Категория**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Классификация угроз, например Троян или троянская Keylogger.

</dd> <dt>

**категоридескриптион**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Описание категории угроз.

</dd> <dt>

**северитинаме**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Степень серьезности угрозы, например серьезная или умеренная.

</dd> <dt>

**северитидескриптион**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Описание уровня серьезности угрозы.

</dd> <dt>

**шортдескриптион**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Краткое описание угрозы.

</dd> <dt>

**Дефаултактионнаме;**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Имя действия по умолчанию, например Remove или карантин, предлагаемое ядром.

</dd> <dt>

**Advice**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Советы по конкретной угрозе.

</dd> <dt>

**среатурл**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

URL-адрес веб-страницы, содержащей сведения об угрозе.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





