---
title: Перечисление MP_FASTPATH_TYPE (Мпклиент. h)
description: Тип Фастпас.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE перечисления устаревших Windows компонентов среды
- PMP_FASTPATH_TYPEные компоненты среды Windows указателя перечисления
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd9a8ce26f930a35c9c4fa547234b0d55b0b588b60881cf8aae31621e9a83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247449"
---
# <a name="mp_fastpath_type-enumeration"></a>\_ \_ Перечисление типов фастпас MP

Тип Фастпас.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**фастпас пакета управления \_ \_ неизвестен**
</dt> <dd>

Неизвестно.

</dd> <dt>

<span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**пакет управления \_ фастпас \_ VDM**
</dt> <dd>

Обновление VDM.

</dd> <dt>

<span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**\_ФАСТПАС MP \_ отключен**
</dt> <dd>

Уведомление об отключении подписи.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





