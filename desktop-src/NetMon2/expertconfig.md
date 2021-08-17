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
ms.openlocfilehash: 93b47054fd5b8103d5bbe0d762db87f285a5f01690d0b93f6da14d215e404a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366914"
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



 

 




