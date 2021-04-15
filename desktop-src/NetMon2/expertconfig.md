---
description: Структура ЕКСПЕРТКОНФИГ содержит данные конфигурации эксперта. Эксперт накладывает элемент Равконфигдата на структуру, относящуюся к эксперту.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Структура ЕКСПЕРТКОНФИГ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662207"
---
# <a name="expertconfig-structure"></a>Структура ЕКСПЕРТКОНФИГ

Структура **експертконфиг** содержит данные конфигурации эксперта. Эксперт накладывает элемент **равконфигдата** на структуру, относящуюся к эксперту.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a>Члены

<dl> <dt>

**равконфигленгс**
</dt> <dd>

Общая длина структуры, включая четыре байта, используемые для элемента. Сетевой монитор использует значение при сохранении структуры на диске и при чтении с диска.

</dd> <dt>

**равконфигдата**
</dt> <dd>

Данные конфигурации. Эксперт должен добавить данные конфигурации. Например, предположим, что у вас есть структура данных, похожая на эту.

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

Обратите внимание, что **равконфигленгс** обеспечивает правильную работу оверлея. При использовании данных код может выглядеть следующим образом:

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




