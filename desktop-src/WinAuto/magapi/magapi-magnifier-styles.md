---
title: Стили экранной лупы
description: В этом разделе описываются стили, используемые с элементом управления "Экранная лупа".
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: ef65f736b50210ed52c542375aa340d5bd85ae38265a71858d82e069d830aa62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052582"
---
# <a name="magnifier-styles"></a>Стили экранной лупы

В этом разделе описываются стили, используемые с элементом управления "Экранная лупа". Чтобы создать элемент управления "Экранная лупа", используйте функцию [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) и укажите класс окна WC_MAGNIFIER, а также сочетание следующих стилей экранной лупы.

| Требование | Значение |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | Вырезает область окна экранной лупы, которая окружает системный курсор. Этот стиль позволяет пользователю видеть содержимое экрана, которое находится за окном экранной лупы. |
| MS_INVERTCOLORS 0x0004L | Отображает увеличенное содержимое экрана с использованием инвертированных цветов. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | Отображает увеличенный системный курсор вместе с увеличенным содержимым экрана. |

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Увеличение. h</dt> </dl> |

## <a name="see-also"></a>См. также

[Константы](entry-magapi-constants.md)
