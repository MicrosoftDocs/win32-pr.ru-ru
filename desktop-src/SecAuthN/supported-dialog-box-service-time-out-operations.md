---
description: 'Winlogon реализует две операции времени ожидания: один для безопасных диалоговых окон, а другой — для активации и завершения заставки.'
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Поддерживаемые операции диалогового окна "Время использования службы"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809899"
---
# <a name="supported-dialog-box-service-time-out-operations"></a>Поддерживаемые операции диалогового окна "Время использования службы"

[*Winlogon*](../secgloss/w-gly.md) реализует две операции времени ожидания: один для безопасных диалоговых окон, а другой — для активации и завершения заставки.

При отображении защищенного диалогового окна, например входа в систему или разблокировки рабочей станции, Winlogon может исполнить время ожидания диалоговых окон и вернуть соответствующий код результата в процедуру диалогового окна. Winlogon предоставляет набор функций поддержки диалоговых окон для [*модели GINA*](../secgloss/g-gly.md). В модели GINA эти функции должны использоваться вместо своих аналогов в Windows, чтобы гарантировать, что GINA и Winlogon сохраняют соответствующий контроль над диалоговыми окнами. Невозможность использования версий Winlogon этих функций может привести к тому, что неавторизованные пользователи смогут получить доступ к системе.

Службы диалогов диалогового окна Winlogon предоставляются следующими функциями поддержки.



| Функция поддержки                                               | Описание                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**влксмессажебокс**](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | Аналогично функции Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) .                         |
| [**влксдиалогбокс**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | Аналогично функции Windows [**диалогбокс**](/windows/win32/api/winuser/nf-winuser-dialogboxa) .                           |
| [**влксдиалогбоксиндирект**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | Аналогично функции Windows [**диалогбоксиндирект**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) .           |
| [**влксдиалогбокспарам**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | Аналогично функции Windows [**диалогбокспарам**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) .                 |
| [**влксдиалогбоксиндиректпарам**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | Аналогично функции Windows [**диалогбоксиндиректпарам**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) . |



 

Библиотеки DLL GINA также могут получить \_ \_ сообщения SAS влкс WM из Winlogon. Эти сообщения отправляются в активные диалоговые окна при получении [*последовательности безопасности*](../secgloss/s-gly.md) (SAS). Это полезно в том случае, если GINA находится в процессе запроса на сопоставление для [*смарт-карты*](../secgloss/s-gly.md), и карта удаляется из [*считывателя*](../secgloss/r-gly.md)смарт-карт. Winlogon использует \_ SAS влкс DLG в \_ качестве кода результата EndDialog при возникновении события SAS во время операции диалогового окна.

Время ожидания также доставляется таким образом. \_ \_ Сообщение SAS влкс WM отправляется с влкс \_ SAS \_ типа \_ скрнсвр \_ timeout или влкс \_ SAS \_ Type \_ timeout. Диалоговое окно завершится соответствующим кодом выхода, чтобы позволить разработчикам GINA присоединить уведомления о времени ожидания.

Диалоговые окна GINA могут быть завершены с помощью программы Winlogon с кодом ВЛКС, выполнив \_ \_ \_ Выход пользователя. Это означает, что пользователь вышел из системы во время выполнения диалогового окна (например, путем вызова функции [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) из другого потока).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инициализация Winlogon](initializing-winlogon.md)
</dt> <dt>

[Состояния Winlogon](winlogon-states.md)
</dt> <dt>

[Отправка сообщений в GINA](sending-messages-to-the-gina.md)
</dt> <dt>

[Функции поддержки Winlogon](authentication-functions.md)
</dt> </dl>

 

 
