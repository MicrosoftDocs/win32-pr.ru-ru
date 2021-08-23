---
title: Структура MPNIS_PRIVATE_DATA (Мпклиент. h)
description: Частные уведомления NIS.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- MPNIS_PRIVATE_DATA структуры устаревшие функции среды Windows
- функции PMPNIS_PRIVATE_DATA Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50719e4ecc0beff848467023a1c5f941ff06ceb891b05674e199d47a38b8659
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556144"
---
# <a name="mpnis_private_data-structure"></a>\_Структура закрытых \_ данных мпнис

Частные уведомления NIS.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**двнотификатионтипе**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Тип уведомления.

</dd> <dt>

**кбдатасизе**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Размер зарезервированных данных в байтах.

</dd> <dt>

**pbData**
</dt> <dd>

Тип: **Byte \***

</dd> <dd>

Указатель на зарезервированные данные.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





