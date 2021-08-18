---
title: Структура MPCOMPONENT_VERSION (Мпклиент. h)
description: Версия и время обновления отдельного компонента.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION структуры устаревшие функции среды Windows
- функции PMPCOMPONENT_VERSION Windows указателя структур в устаревшей среде
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6092fe2f3ec7ba921b1ef3adfc9355feeeae67f2381836056f2af65b276921cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976074"
---
# <a name="mpcomponent_version-structure"></a>\_Структура версии мпкомпонент

Версия и время обновления отдельного компонента.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>Члены

<dl> <dt>

**Version**
</dt> <dd>

Тип: **улонглонг**

</dd> <dd>

Поле версии. Каждое **слово** представляет основную, дополнительную, сборку и редакцию.

</dd> <dt>

**UpdateTime**
</dt> <dd>

Тип: **уларже \_ Integer**

</dd> <dd>

Время последнего обновления компонента в формате **fileTime** .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





