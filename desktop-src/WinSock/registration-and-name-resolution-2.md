---
description: Сокеты Windows 2 — это набор функций, которые стандартизируют способ доступа приложений к различным службам именования сетевых имен и их использования.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Регистрация и разрешение имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702015"
---
# <a name="registration-and-name-resolution"></a>Регистрация и разрешение имен

Сокеты Windows 2 — это набор функций, которые стандартизируют способ доступа приложений к различным службам именования сетевых имен и их использования. При использовании этих функций приложения не должны отличать широко отличающиеся протоколы, связанные с такими службами имен, как DNS, NIS, X. 500, SAP и т. д. Чтобы обеспечить полную обратную совместимость с сокетами Windows 1,1, существующие функции **жетксбии** и асинхронной **всаасинкжетксбии** базы данных по-прежнему поддерживаются, но реализуются в интерфейсе поставщика службы Windows Sockets с точки зрения новых возможностей разрешения имен. Дополнительные сведения см. в разделе функции [**жетсервбинаме**](/windows/desktop/api/winsock/nf-winsock-getservbyname) и [**жетсервбипорт**](/windows/desktop/api/winsock/nf-winsock-getservbyport) . См. также раздел [Совместимость разрешения имен для TCP/IP в сокетах Windows sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).

В этом разделе описаны возможности регистрации и разрешения имен, доступные для разработчиков Winsock. В следующем списке перечислены подразделы этого раздела.

-   [Разрешение имен, не зависящее от протокола](protocol-independent-name-resolution-2.md)
-   [Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Об Winsock](about-winsock.md)
</dt> <dt>

[Использование Winsock](using-winsock.md)
</dt> </dl>

 

 



