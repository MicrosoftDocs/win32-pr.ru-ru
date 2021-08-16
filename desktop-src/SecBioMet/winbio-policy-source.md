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
ms.openlocfilehash: 962d4bc3e8cffb778df56d78a9ddaf0641f57f8f96c8f7b024745a4b879f2f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909941"
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

политика является политикой по умолчанию, которую предоставляет биометрическая платформа Windows.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_ \_ Локальная политика винбио**
</dt> <dd>

политика, которую отдельный пользователь задает для своей учетной записи с помощью приложения **Параметры** . Эта политика переопределяет политику по умолчанию.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_Администратор политики \_ винбио**
</dt> <dd>

Групповая политика, заданная ИТ-администратором для предприятия. Отдельные пользователи не могут переопределить эту политику.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                                                                                              |
| Минимальная версия сервера<br/> | Windows Server 2016 \[ только классические приложения\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ \_ действие политики АНТИфишинга винбио \_**](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





