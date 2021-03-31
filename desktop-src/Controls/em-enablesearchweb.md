---
title: Сообщение EM_ENABLESEARCHWEB (Коммктрл. h)
description: Включает или отключает функцию "Поиск в Интернете" и запись в контекстном меню.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Элементы управления Windows для EM_ENABLESEARCHWEB сообщений
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988913"
---
# <a name="em_enablesearchweb-message"></a>\_Сообщение ЕНАБЛЕСЕАРЧВЕБ EM

Включает или отключает функцию "Поиск в Интернете" и запись в контекстном меню.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Значение **true** указывает, что функция "Поиск в Интернете" включена, а значение " **ложь** " означает, что она отключена.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

Если отключить "Поиск в Интернете" с помощью этого сообщения, сообщение [**EM \_ сеарчвеб**](em-searchweb.md) не будет действовать.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, \[ только классические приложения 1809\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2019\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ сеарчвеб**](em-searchweb.md)
</dt> </dl>

 

 





