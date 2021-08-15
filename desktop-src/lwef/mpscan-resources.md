---
title: Структура MPSCAN_RESOURCES (Мпклиент. h)
description: Сведения о ресурсах, переданные во время операции просмотра.
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES структуры устаревшие функции среды Windows
- функции PMPSCAN_RESOURCES Windows указателя структур в устаревшей среде
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
ms.openlocfilehash: dd70b442e7179d516d2e9c60b81e6c52b0f696f5719a255871e8687773bf71ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747353"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_сведения о мпресаурце**](mpresource-info.md)
</dt> </dl>

 

 





