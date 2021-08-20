---
title: Перечисление ТИПЕМОДЕ (Софткбдк. h)
description: Элементы перечисления ТИПЕМОДЕ используются для указания режимов типов, доступных для экранной клавиатуры.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- Платформа текстовых служб перечисления ТИПЕМОДЕ
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ae25435b48d1482441b8617a52bace8debabb210b62782a234837553e2c36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949841"
---
# <a name="typemode-enumeration"></a>Перечисление ТИПЕМОДЕ

Элементы перечисления **типемоде** используются для указания режимов типов, доступных для экранной клавиатуры.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**кликкмаусе**
</dt> <dd>

Пользователь может щелкнуть клавиши на экране, чтобы ввести текст.

</dd> <dt>

<span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Помещении**
</dt> <dd>

Пользователь может указать ключ на определенный период времени, и выбранный символ будет введен автоматически.

</dd> <dt>

<span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Проверяет**
</dt> <dd>

С помощью экранной клавиатуры постоянно проверяются область ввода и выделяются области, в которых пользователь может нажать сочетание клавиш или выбрать устройство ввода.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Распространяемые компоненты<br/>          | TSF 1,0 на Windows 2000 Professional<br/>                                        |
| Заголовок<br/>                   | <dl> <dt>Софткбдк. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Софткбд. idl</dt> </dl> |



 

 





