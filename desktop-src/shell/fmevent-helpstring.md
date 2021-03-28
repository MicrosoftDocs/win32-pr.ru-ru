---
description: Отправляется в процедуру DLL расширения диспетчера файлов, когда диспетчеру файлов требуется строка справки для элемента команды меню или панели инструментов.
title: Сообщение FMEVENT_HELPSTRING (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264434"
---
# <a name="fmevent_helpstring-message"></a>\_Сообщение фмевент HELPSTRING

Отправляется в процедуру DLL расширения диспетчера файлов, когда диспетчеру файлов требуется строка справки для элемента команды меню или панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*лпфмшс* 
</dt> <dd>

Адрес структуры [**FMS \_ HELPSTRING**](fms-helpstring.md) , который передает строковые данные справки по командным элементам. Структура **FMS \_ HELPSTRING** определяет элемент команды, для которого требуется строка справки, вместе с маркером ее меню. Затем приложение записывает соответствующую строку справки в элемент **сзелп** структуры **FMS \_ HELPSTRING** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При обработке этого сообщения процедура DLL расширения должна вернуть нуль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**фмекстенсионпрок**](fmextensionproc.md)
</dt> <dt>

[**ФМЕВЕНТ \_ хелпменуитем**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




