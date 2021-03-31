---
title: Структура MPCOMPONENT_VERSION (Мпклиент. h)
description: Версия и время обновления отдельного компонента.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION структуры устаревшие функции среды Windows
- Функции PMPCOMPONENT_VERSION указателя структур в устаревшей среде Windows
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
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988601"
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





