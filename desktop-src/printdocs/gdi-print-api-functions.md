---
description: Функции API печати GDI
ms.assetid: cf3f4a61-8858-4c91-a778-d2a65998ef70
title: Функции API печати GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125e5feef16a64433dadd11e830a09241877a453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909375"
---
# <a name="gdi-print-api-functions"></a>Функции API печати GDI

## <a name="in-this-section"></a>Содержание раздела



| Функция                                                                    | Описание                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**абортдок**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                     | Функция [**абортдок**](/windows/desktop/api/wingdi/nf-wingdi-abortdoc) останавливает текущее задание печати и стирает все, что было выведено с момента последнего вызова функции [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .<br/>                                                                                                                                                                                                 |
| [*абортпрок*](/windows/desktop/api/Wingdi/nc-wingdi-abortproc)<br/>                                     | Функция [**абортпрок**](/windows/desktop/api/wingdi/nc-wingdi-abortproc) является определяемой приложением функцией обратного вызова, используемой с функцией [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc) . Он вызывается, когда задание печати должно быть отменено во время буферизации. Тип **абортпрок** определяет указатель на эту функцию обратного вызова. **Абортпрок** — это заполнитель для имени определяемой приложением функции.<br/> |
| [**девицекапабилитиес**](/windows/desktop/api/WinGdi/nf-wingdi-devicecapabilitiesa)<br/>                 | Функция [**девицекапабилитиес**](/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa) извлекает возможности драйвера принтера.<br/>                                                                                                                                                                                                                                                       |
| [**енддок**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                         | Функция [**енддок**](/windows/desktop/api/wingdi/nf-wingdi-enddoc) завершает задание печати.<br/>                                                                                                                                                                                                                                                                                                             |
| [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                       | Функция **EndPage** уведомляет устройство о том, что приложение завершило запись на страницу. Эта функция обычно используется для направления перехода драйвера устройства на новую страницу.<br/>                                                                                                                                                                             |
| [**ESCAPE**](/windows/desktop/api/Wingdi/nf-wingdi-escape)<br/>                                         | позволяет приложению получать доступ к системным функциям устройств, которые недоступны через GDI.<br/>                                                                                                                                                                                                                                                         |
| [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                   | Функция [**екстескапе**](/windows/desktop/api/wingdi/nf-wingdi-extescape) позволяет приложению получить доступ к возможностям устройства, которые недоступны через GDI.<br/>                                                                                                                                                                                                                                |
| [**исвиндовредиректедфорпринт**](iswindowredirectedforprint.md)<br/> | Функция [**исвиндовредиректедфорпринт**](iswindowredirectedforprint.md) определяет, перенаправлено ли указанное окно на печать в данный момент.<br/>                                                                                                                                                                                                         |
| [**принтвиндов**](/windows/desktop/api/Winuser/nf-winuser-printwindow)<br/>                               | Функция [**принтвиндов**](/windows/desktop/api/winuser/nf-winuser-printwindow) копирует визуальное окно в указанный контекст устройства (DC), обычно это контроллер домена принтера.<br/>                                                                                                                                                                                                                              |
| [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc)<br/>                             | Функция [**SetAbortProc**](/windows/desktop/api/wingdi/nf-wingdi-setabortproc) задает определяемую приложением функцию прерывания, которая позволяет отменить задание печати во время печати.<br/>                                                                                                                                                                                                               |
| [**стартдок**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                     | Функция [**стартдок**](/windows/desktop/api/wingdi/nf-wingdi-startdoca) запускает задание печати.<br/>                                                                                                                                                                                                                                                                                                       |
| [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                   | Функция [**StartPage**](/windows/desktop/api/wingdi/nf-wingdi-startpage) готовит драйвер принтера к приему данных.<br/>                                                                                                                                                                                                                                                                             |



 

 

