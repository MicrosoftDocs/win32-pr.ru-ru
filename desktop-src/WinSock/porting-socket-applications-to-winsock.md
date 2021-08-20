---
description: В этом разделе описаны рекомендации по переносу Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Перенос приложений сокета в Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97b545c679d9ceb13e3173550dd04b4724309d078b2e8e39fb20419921ba941f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111872"
---
# <a name="porting-socket-applications-to-winsock"></a>Перенос приложений сокета в Winsock

В этом разделе описаны рекомендации по переносу Winsock.

существует ограниченное количество экземпляров, в которых Windows сокеты поступили от строгого соответствия соглашениям Berkeley, обычно из-за проблем с реализацией в среде Microsoft Windows.

если в Windows сокетах происходит отклонение соглашений об использовании bind, отклонения заменяются специально и четко. например, если функция относится к Windows сокетам, это отклонение указывается с помощью фразы в описании функции, как показано ниже:

функция **\[ имени \]** функции — это расширение для интерфейса API Windows sockets 2, специфическое для майкрософт.

в этом разделе приводятся сведения о переносе приложений сокета (BSD) UNIX в Winsock:

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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обработка ошибок Winsock](handling-winsock-errors.md)
</dt> <dt>

[Перенос приложений сокета в Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Коды ошибок сокетов](windows-sockets-error-codes-2.md)
</dt> <dt>

[Вопросы программирования Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 



