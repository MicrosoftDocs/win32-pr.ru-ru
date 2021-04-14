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
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415568"
---
# <a name="magnifier-styles"></a>Стили экранной лупы

В этом разделе описываются стили, используемые с элементом управления "Экранная лупа". Чтобы создать элемент управления "Экранная лупа", используйте функцию [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) и укажите класс окна WC_MAGNIFIER, а также сочетание следующих стилей экранной лупы.

| Требование | Значение |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | Вырезает область окна экранной лупы, которая окружает системный курсор. Этот стиль позволяет пользователю видеть содержимое экрана, которое находится за окном экранной лупы. |
| MS_INVERTCOLORS 0x0004L | Отображает увеличенное содержимое экрана с использованием инвертированных цветов. |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | Отображает увеличенный системный курсор вместе с увеличенным содержимым экрана. |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Увеличение. h</dt> </dl> |

## <a name="see-also"></a>См. также раздел

[Константы](entry-magapi-constants.md)
