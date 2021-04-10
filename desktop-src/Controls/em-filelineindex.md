---
title: Сообщение EM_FILELINEINDEX (Коммктрл. h)
description: Возвращает символьный индекс первого символа указанной строки в многострочном элементе управления Edit, независимо от того, как линии отображаются на экране.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Элементы управления Windows для EM_FILELINEINDEX сообщений
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136263"
---
# <a name="em_filelineindex-message-commctrlh"></a>Сообщение EM_FILELINEINDEX (Коммктрл. h)

Возвращает символьный индекс первого символа указанной строки в многострочном элементе управления Edit, независимо от того, как линии отображаются на экране. Индекс символа — это Отсчитываемый от нуля индекс символа, начиная с начала элемента управления "поле ввода".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Номер строки, начинающейся с нуля. Значение-1 указывает текущий номер строки (строка, содержащая курсор).

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение — это индекс символа строки, указанной в параметре *wParam* , независимо от того, как линии отображаются на экране, или-1, если номер строки больше числа строк в элементе управления "поле ввода".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, \[ только классические приложения 1809\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2019\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ филелинефромчар**](em-filelinefromchar.md)
</dt> </dl>

 

 





