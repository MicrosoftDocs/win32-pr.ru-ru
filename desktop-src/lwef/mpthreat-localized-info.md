---
title: Структура MPTHREAT_LOCALIZED_INFO (Мпклиент. h)
description: Локализованные сведения для угрозы.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO структуры устаревшие функции среды Windows
- Функции PMPTHREAT_LOCALIZED_INFO указателя структур в устаревшей среде Windows
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
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415476"
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

**CategoryName**
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





