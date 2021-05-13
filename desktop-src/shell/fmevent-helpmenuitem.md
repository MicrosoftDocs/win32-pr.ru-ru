---
description: Отправляется в процедуру DLL расширения диспетчера файлов, когда пользователь нажимает клавишу F1 в меню или элементе команды панели инструментов. Расширение должно вызывать WinHelp, а параметр HWND этой функции имеет значение, равное значению параметра HWND расширения.
title: Сообщение FMEVENT_HELPMENUITEM (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: 46cb246e91f9901204432527ba36fd8ac72beba4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842315"
---
# <a name="fmevent_helpmenuitem-message"></a>\_Сообщение фмевент хелпменуитем

Отправляется в процедуру DLL расширения диспетчера файлов, когда пользователь нажимает клавишу F1 в меню или элементе команды панели инструментов. Расширение должно вызывать [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), а параметр *HWND* этой функции имеет значение, равное значению параметра *HWND* расширения.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*уитем* 
</dt> <dd>

Значение, идентифицирующее элемент команды меню или панели инструментов, для которого требуется справка. Процедура расширения использует это значение для определения наилучшего вызова [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При обработке этого сообщения процедура DLL расширения должна вернуть нуль.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> <dt>

[**ФМЕВЕНТ \_ HELPSTRING**](fmevent-helpstring.md)
</dt> </dl>

 

 




