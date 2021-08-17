---
title: Структура MPSIGUPDATE_DATA (Мпклиент. h)
description: Данные уведомления, передаваемые функции обратного вызова обновления сигнатур.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA структуры устаревшие функции среды Windows
- функции PMPSIGUPDATE_DATA Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3c117b92882a24a825aee5c5b008e10721c40b8a93d26a9a677bb79858635c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476256"
---
# <a name="mpsigupdate_data-structure"></a>\_Структура данных мпсигупдате

Данные уведомления, передаваемые функции обратного вызова обновления сигнатур.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**двперценткомплете**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Оценка процента между всеми обновлениями, которые были загружены и (или) установлены.

</dd> <dt>

**двтоталупдатес**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Общее число обновлений для скачивания и (или) установки.

</dd> <dt>

**двкуррентупдатеиндекс**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Значение индекса, начинающееся с нуля, которое указывает, какое обновление в данный момент должно быть загружено и (или) установлено.

</dd> <dt>

**eType**
</dt> <dd>

Тип: **мпсигупдате \_ тип**

</dd> <dd>

Тип обновления. Одно из следующих возможных значений:



| Значение                                                                                                                                                                                                                             | Значение                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**\_тип мпсигупдате \_ None**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**\_ \_ управляемый тип мпсигупдате**</dt> </dl>                                   | Обновление WSUS. Для отмены требуются права администратора.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**МПСИГУПДАТЕ \_ тип \_ http**</dt> </dl>                                            | Обновление HTTP. Права администратора, которые не требуются для отмены.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**МПСИГУПДАТЕ \_ тип \_ HTTP \_ SRV**</dt> </dl>                               | HTTP из службы. Для отмены требуются права администратора.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**МПСИГУПДАТЕ \_ типа \_ UNC**</dt> </dl>                                               | Общий UNC-ресурс. Права администратора, которые не требуются для отмены.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**\_НЕуправляемый тип мпсигупдате \_**</dt> </dl>                             | Обновление MU/WU. Для отмены требуются права администратора.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**\_ \_ управляемая платформа типа мпсигупдате \_**</dt> </dl>       | Обновление WSUS для платформы. Для отмены требуются права администратора.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**\_ \_ неуправляемая платформа типа \_ мпсигупдате**</dt> </dl> | Обновление MU/WU для платформы. Для отмены требуются права администратора.<br/> |



 

</dd> <dt>

**Этап**
</dt> <dd>

Тип: **\_ \_ этап обновления пакета управления**

</dd> <dd>

Стадия обновления. Одно из следующих возможных значений:



| Значение                                                                                                                                                                         | Значение                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**\_неизвестная стадия пакета управления \_**</dt> </dl>       | Неизвестный этап обновления.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**\_Обновление поиска \_ MP**</dt> </dl>       | Обновление этапа поиска.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**\_обновление загрузки пакета управления \_**</dt> </dl> | Стадия скачивания обновлений.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**\_Установка \_ обновления MP**</dt> </dl>    | Обновление этапа установки.<br/>  |



 

</dd> <dt>

**Путь**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Путь обновления.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





