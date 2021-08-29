---
description: Отправляется в функцию Кплапплет приложения панели управления, когда пользователь дважды щелкает значок диалогового окна, поддерживаемого приложением.
title: Сообщение CPL_DBLCLK (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9faf3f589e9e3e69c3b8df82bbb6eb2c075d6fba2836b9d8e773b392ad9385c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351354"
---
# <a name="cpl_dblclk-message"></a>\_Сообщение CPL дблклк

Отправляется в функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) приложения панели управления, когда пользователь дважды щелкает значок диалогового окна, поддерживаемого приложением.

## <a name="parameters"></a>Параметры

<dl> <dt>

*уаппнум* 
</dt> <dd>

Число в диалоговом окне. Это число должно находиться в диапазоне от нуля до значения, возвращенного в ответ на сообщение [**CPL \_ NOCOUNT**](cpl-getcount.md) (CPL \_ -count – 1).

</dd> <dt>

*лдата* 
</dt> <dd>

Значение, которое приложение панели управления загрузило в элемент **лпдата** в структуре [**кплинфо**](/windows/win32/api/cpl/ns-cpl-cplinfo) или [**невкплинфо**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) для этого диалогового окна. Приложение загружает элемент **лпдата** в ответ на сообщение [**CPL Response \_**](cpl-inquire.md) или [**CPL \_ невинкуире**](cpl-newinquire.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) успешно обрабатывает это сообщение, возвращаемое значение равно нулю. в противном случае он не равен нулю.

## <a name="remarks"></a>Remarks

В ответ на это сообщение приложение панели управления должно отобразить соответствующее диалоговое окно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Заголовок<br/>                   | <dl> <dt>CPL. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CPL — \_ Выбор**](cpl-select.md)
</dt> </dl>

 

 
