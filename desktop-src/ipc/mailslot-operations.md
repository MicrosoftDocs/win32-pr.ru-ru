---
description: Описание функций, используемых при работе с маилслотс, клиентами и серверами.
ms.assetid: 40758d5e-8538-47d9-b8ca-8de5b053ee8b
title: Операции с слотом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fefce55c70971f5d611c41d473180897706bc04960509818cb0d092c7f83825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829504"
---
# <a name="mailslot-operations"></a>Операции с слотом

При работе с маилслотс клиенты и серверы должны использовать только функции, описанные в следующих таблицах. Не используйте другие функции, даже если они принимают дескрипторы файлов или имена файлов в качестве параметров, так как они не предназначены для работы с маилслотс.

## <a name="mailslot-server-functions"></a>Функции сервера слота

Серверы слота имеют эксклюзивное использование трех функций, как показано в следующей таблице.



| Функция                                   | Описание                                                                                                                                                                                                  |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**креатемаилслот**](/windows/desktop/api/Winbase/nf-winbase-createmailslota)   | Создает почтовый слот и возвращает маркер в виде слота.                                                                                                                                                            |
| [**жетмаилслотинфо**](/windows/desktop/api/Winbase/nf-winbase-getmailslotinfo) | Извлекает максимальный размер сообщения, Размер слота, размер следующего сообщения в слоте, количество сообщений в слоте и время, в течение которого операция чтения может ожидать сообщения. |
| [**сетмаилслотинфо**](/windows/desktop/api/Winbase/nf-winbase-setmailslotinfo) | Изменяет время ожидания чтения для слота сообщений.                                                                                                                                                                    |



 

В качестве серверов слота также используются следующие функции.



| Функция                                                         | Описание                                         |
|------------------------------------------------------------------|-----------------------------------------------------|
| [**дупликатехандле**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                      | Дублирует обработчик слота.                     |
| [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [ **реадфиликс**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) | Извлекает сообщения из слота сообщений.                 |
| [**Функции getFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime)                              | Извлекает дату и время создания почтового слота. |
| [**сетфилетиме**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)                              | Задает дату и время создания почтового слота.      |
| [**жесандлеинформатион**](/windows/desktop/api/handleapi/nf-handleapi-gethandleinformation)            | Извлекает свойства обработчика слота сообщений.        |
| [**сесандлеинформатион**](/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation)            | Задает свойства обработчика слота.             |



 

## <a name="mailslot-client-functions"></a>Клиентские функции слота

При взаимодействии с слотом клиентский процесс использует следующие функции.



| Функция                                                             | Описание                                     |
|----------------------------------------------------------------------|-------------------------------------------------|
| [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)                                  | Закрывает обработчик слота для клиентского процесса.  |
| [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)                                    | Создает обработчик в слоте для клиентского процесса. |
| [**дупликатехандле**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)                          | Дублирует обработчик слота.                   |
| [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [ **вритефиликс**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) | Записывает данные в почтовый слот.                      |



 

 

 
