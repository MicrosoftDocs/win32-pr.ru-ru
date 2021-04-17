---
description: В этом разделе описаны рекомендации по переносу Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Перенос приложений сокета в Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711021"
---
# <a name="porting-socket-applications-to-winsock"></a>Перенос приложений сокета в Winsock

В этом разделе описаны рекомендации по переносу Winsock.

Существует ограниченное количество случаев, когда сокеты Windows переносят строгое соответствие соглашениям Berkeley, обычно из-за проблем с реализацией в среде Microsoft Windows.

Если в сокетах Windows происходит отклонение от соглашений Berkeley, то отклонения заменяются специально и четко. Например, если функция относится к сокетам Windows, это отклонение указывается с помощью фразы в описании функции, как показано ниже:

Функция **\[ имени \]** функции — это расширение для API Windows Sockets 2, относящееся к корпорации Майкрософт.

В этом разделе содержатся сведения о переносе приложений сокетов UNIX (BSD) в Winsock:

-   [Тип данных сокета](socket-data-type-2.md)
-   [Макросы SELECT, ДЕМОна \_ Set и демона \_ xxx](select-and-fd---2.md)
-   [Коды ошибок — код возврата, h \_ и всажетластеррор](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [Указатели](pointers-2.md)
-   [Переименованные функции](renamed-functions-2.md)
-   [Максимальное число поддерживаемых сокетов](maximum-number-of-sockets-supported-2.md)
-   [Включаемые файлы](include-files-2.md)
-   [Возвращаемые значения при сбое функции](return-values-on-function-failure-2.md)
-   [Необработанные сокеты](service-provided-raw-sockets-2.md)
-   [Порядок байтов](byte-ordering-2.md)
-   [Расширенные подпрограммы преобразования Byte-Order](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Обработка ошибок Winsock](handling-winsock-errors.md)
</dt> <dt>

[Перенос приложений сокета в Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Коды ошибок сокетов Windows](windows-sockets-error-codes-2.md)
</dt> <dt>

[Вопросы программирования Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



