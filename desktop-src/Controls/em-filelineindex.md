---
title: Сообщение EM_FILELINEINDEX (Коммктрл. h)
description: Возвращает символьный индекс первого символа указанной строки в многострочном элементе управления Edit, независимо от того, как линии отображаются на экране.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- элементы управления Windows сообщений EM_FILELINEINDEX
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
ms.openlocfilehash: df7c4bd1f21ee6bcdf7bec56828ea9c2996c837def614c0c537ef83ee053ebfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915614"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, \[ только классические приложения 1809\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2019\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**EM \_ филелинефромчар**](em-filelinefromchar.md)
</dt> </dl>

 

 





