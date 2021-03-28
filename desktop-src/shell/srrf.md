---
description: Флаги, ограничивающие установленные или возвращаемые данные.
title: СРРФ (Shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080944"
---
# <a name="srrf"></a>сррф

Флаги, ограничивающие установленные или возвращаемые данные.



| Константа/значение                                                                                                                                                                                                                                           | Описание                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <dt>**Сррф \_ RT \_ reg \_ None**</dt> <dt></dt> </dl>                 | Введите REG \_ None.<br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <dt>**Сррф \_ RT \_ reg \_ SZ**</dt> <dt>0x00000002</dt> </dl>                       | Введите REG \_ SZ. \_ \_ Типы SZ Expand автоматически преобразуются в REG- \_ SZ, если не \_ указан флаг сррф NOEXPAND.<br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <dt>**Сррф \_ \_ \_ \_ SZ с развернутой ПОДразделом RT**</dt> <dt></dt> </dl> | Введите REG \_ expand \_ SZ. При получении значения необходимо также получить \_ флаг СРРФ NOEXPAND, иначе [**шрегжетвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) завершится ошибкой с \_ недопустимым \_ параметром.<br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <dt>**Сррф \_ \_ \_ Двоичный**</dt> <dt>0x00000008</dt> "RT reg" </dl>           | Введите \_ двоичный файл REG.<br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <dt>**Сррф \_ \_ \_ Параметр DWORD**</dt> <dt>0x00000010</dt> в RT </dl>              | Введите REG \_ DWORD.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <dt>**Сррф \_ RT \_ reg \_ Multi \_ SZ**</dt> <dt>0x00000020</dt> </dl>    | Введите REG \_ Multi \_ SZ.<br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <dt>**Сррф \_ 0x00000040 \_ \_ QWORD reg**</dt> <dt></dt> </dl>              | Введите REG \_ QWORD.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <dt>**Сррф \_ RT \_ DWORD**</dt> <dt>0x00000018</dt> </dl>                           | REG \_ DWORD и 32-разрядные \_ двоичные типы reg. Это эквивалентно \_ \_ \_ двоичному параметру сррф RT reg Binary \| сррф \_ RT \_ reg \_ . Если при извлечении значения двоичные данные значения имеют размер больше 32 бит, он не возвращается.<br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <dt>**Сррф \_ 0x00000048 \_ QWORD 8**</dt> <dt></dt> </dl>                           | REG \_ QWORD и 64-разрядные \_ двоичные типы reg. Это эквивалентно \_ \_ двоичному сррф RT REG \_ двоичный \| сррф \_ RT \_ reg \_ . Если при извлечении значения двоичные данные значения имеют размер больше 64 бит, он не возвращается.<br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <dt>**Сррф \_ RT \_ ANY**</dt> <dt>0x0000FFFF</dt> </dl>                                 | Все типы. Установите этот флаг, если не \_ задано другое значение сррф RT.<br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <dt>**Сррф \_ RM — \_ любое**</dt> <dt>0x00000000</dt> </dl>                                 | Нет ограничений режима. Это значение по умолчанию.<br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <dt>**Сррф \_ \_Нормальная**</dt> <dt>0x00010000а</dt> RM </dl>                        | Ограничьте режим запуска системы на "нормальная загрузка".<br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <dt>**Сррф \_ Надежное \_**</dt> <dt>0x00020000</dt> </dl>                              | Ограничьте режим запуска системы на "защищенный режим".<br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <dt>**Сррф \_ RM \_ сафенетворк**</dt> <dt>0x00040000</dt> </dl>         | Ограничьте режим запуска системы на "защищенный режим с помощью сети".<br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <dt>**Сррф \_ РАЗВЕРНУТЬ**</dt> <dt>0x10000000</dt> </dl>                            | Не разворачивайте автоматически \_ строки reg Expand \_ SZ.<br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <dt>**Сррф \_ ЗЕРУНФАИЛУРЕ**</dt> <dt>0x20000000</dt> </dl>             | Если при извлечении значения *пвдата* не равно **null**, установите в качестве содержимого буфера *пвдата* все нули при сбое.<br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <dt>**Сррф \_ НОВИРТ**</dt> <dt>0x40000000</dt> </dl>                                  | При получении значения, если запрошенный ключ виртуализирован, \_ не удается найти файл с ошибкой \_ \_ .<br/>                                                                                                            |



## <a name="remarks"></a>Примечания

Эти значения определены в Shlwapi. h.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Shlwapi. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**шрегсетвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[**шрегжетвалуе**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




