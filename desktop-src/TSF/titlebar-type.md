---
title: Перечисление TITLEBAR_TYPE (Софткбдк. h)
description: Элементы перечисления типа "строка заголовка" \_ используются для указания типов титлебарс, доступных для окна с экранной клавиатурой.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- Платформа текстовых служб для перечисления TITLEBAR_TYPE
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681896"
---
# <a name="titlebar_type-enumeration"></a>Перечисление типов в строке заголовка \_

Элементы перечисления **\_ типа "строка заголовка** " используются для указания типов титлебарс, доступных для окна с экранной клавиатурой.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**\_без заголовка**
</dt> <dd>

В окне экранной клавиатуры не используется заголовок.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**Захват окна "заголовок по \_ \_ горизонтали" \_**
</dt> <dd>

В окне экранной клавиатуры используется только горизонтальная панель захвата.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**\_захват заголовка окна \_ верти \_ только**
</dt> <dd>

В окне экранной клавиатуры используется только вертикальная панель захвата.

</dd> <dt>

<span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**\_кнопка захвата в строке заголовка \_**
</dt> <dd>

В окне экранной клавиатуры используется только кнопка захвата.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| Распространяемые компоненты<br/>          | TSF 1,0 в Windows 2000 профессиональная<br/>                                        |
| Header<br/>                   | <dl> <dt>Софткбдк. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Софткбд. idl</dt> </dl> |



 

 





