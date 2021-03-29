---
title: Структура MPSCAN_RESOURCES (Мпклиент. h)
description: Сведения о ресурсах, переданные во время операции просмотра.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES структуры устаревшие функции среды Windows
- Функции PMPSCAN_RESOURCES указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989382"
---
# <a name="mpscan_resources-structure"></a>\_Структура ресурсов мпскан

Сведения о ресурсах, переданные во время операции просмотра.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a>Члены

<dl> <dt>

**двресаурцекаунт**
</dt> <dd>

Тип: **DWORD**

</dd> <dd>

Число ресурсов.

</dd> <dt>

**пресаурцелист**
</dt> <dd>

Тип: **пмпресаурце \_ info** .

</dd> <dd>

Массив ресурсов. См [**. \_ сведения о мпресаурце**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_сведения о мпресаурце**](mpresource-info.md)
</dt> </dl>

 

 





