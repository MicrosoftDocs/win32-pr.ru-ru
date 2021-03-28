---
description: Отправляется в функцию Кплапплет приложения панели управления для получения количества диалоговых окон, поддерживаемых приложением.
title: Сообщение CPL_GETCOUNT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6b88b56c-aad7-4144-ab95-15d7eef21861
api_name:
- CPL_GETCOUNT
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3bf8980fa29841d3c5341daeeccf26cea05db80c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540546"
---
# <a name="cpl_getcount-message"></a>\_Сообщение CPL NOCOUNT

Отправляется в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления для получения количества диалоговых окон, поддерживаемых приложением.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) возвращает число диалоговых окон, поддерживаемых приложением панели управления.

## <a name="remarks"></a>Примечания

Это сообщение отправляется сразу после сообщения [**CPL \_ init**](cpl-init.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
