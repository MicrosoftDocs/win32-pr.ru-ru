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
ms.openlocfilehash: 58f95a62d17ccafd308666a5632a1f7a42ebfda6ca0a54dfb6dfa9d9eda9b684
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715484"
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

## <a name="remarks"></a>Remarks

Это сообщение отправляется сразу после сообщения [**CPL \_ init**](cpl-init.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



 

 
