---
description: Отправляется расширением диспетчера файлов для получения числа выбранных файлов в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска). Счетчик включает файлы с длинными именами файлов.
title: Сообщение FM_GETSELCOUNTLFN (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETSELCOUNTLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d0815afc-5356-48a7-a90d-5f48dae6bee5
ms.openlocfilehash: 1ec06c08775836a94b9ada6520ea7c5ea46b62f3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841345"
---
# <a name="fm_getselcountlfn-message"></a>\_Сообщение FM жетселкаунтлфн

Отправляется расширением диспетчера файлов для получения числа выбранных файлов в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска). Счетчик включает файлы с длинными именами файлов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число выбранных файлов.

## <a name="remarks"></a>Remarks

Только расширения, поддерживающие длинные имена файлов (например, сетевые расширения), должны использовать это сообщение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Вфекст. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**FM \_ жетфилесел**](fm-getfilesel.md)
</dt> <dt>

[**FM \_ жетфилеселлфн**](fm-getfilesellfn.md)
</dt> <dt>

[**FM \_ жетселкаунт**](fm-getselcount.md)
</dt> </dl>

 

 




