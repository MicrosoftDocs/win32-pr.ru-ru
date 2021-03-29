---
title: Код уведомления PSN_HELP (Пршт. h)
description: Уведомляет страницу о нажатии пользователем кнопки Справка. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- PSN_HELP кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa60e039211e4c8e63a831ae547c3db116ede3f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654547"
---
# <a name="psn_help-notification-code"></a>\_Код уведомления PSN Help

Уведомляет страницу о нажатии пользователем кнопки Справка. Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**пшнотифи**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) , содержащую сведения о коде уведомления. Эта структура содержит структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) в качестве первого элемента, **HDR**. Элемент **хвндфром** этой структуры **NMHDR** содержит маркер для страницы свойств. Член **lParam** структуры **пшнотифи** не содержит никаких сведений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Приложение должно отображать справочные сведения о странице.

> [!Note]  
> Этот код уведомления не поддерживается при использовании стиля мастера Aero ([**командном PSH \_ аеровизард**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





