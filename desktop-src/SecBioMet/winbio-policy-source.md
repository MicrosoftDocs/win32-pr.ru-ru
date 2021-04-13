---
title: Перечисление WINBIO_POLICY_SOURCE (Винбио \_ types. h)
description: Список возможных источников сведений о политике для обнаружения подмены для биометрических факторов.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- API биометрическая платформа Windows перечисления WINBIO_POLICY_SOURCE
- API биометрическая платформа Windows указателя перечисления PWINBIO_POLICY_SOURCE
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341265"
---
# <a name="winbio_policy_source-enumeration"></a>\_ \_ Перечисление источников политики винбио

Список возможных источников сведений о политике для обнаружения подмены для биометрических факторов.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**\_неизвестная политика винбио \_**
</dt> <dd>

Неизвестный источник политики.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_Политика винбио \_ по умолчанию**
</dt> <dd>

Политика является политикой по умолчанию, которую предоставляет биометрическая платформа Windows.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_ \_ Локальная политика винбио**
</dt> <dd>

Политика, которую отдельный пользователь задает для своей учетной записи с помощью приложения " **Параметры** ". Эта политика переопределяет политику по умолчанию.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_Администратор политики \_ винбио**
</dt> <dd>

Групповая политика, заданная ИТ-администратором для предприятия. Отдельные пользователи не могут переопределить эту политику.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ действие политики АНТИфишинга винбио \_**](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





