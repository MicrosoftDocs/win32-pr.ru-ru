---
description: Таблицы сообщений — это специальные строковые ресурсы, используемые при отображении сообщений об ошибках. Они объявляются в файле ресурсов с помощью инструкции МЕССАЖЕТАБЛЕ Resource-Definition. Для доступа к строкам сообщений используйте функцию FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Таблицы сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990378"
---
# <a name="message-tables"></a>Таблицы сообщений

Таблицы сообщений — это специальные строковые ресурсы, используемые при отображении сообщений об ошибках. Они объявляются в файле ресурсов с помощью инструкции [мессажетабле](../menurc/messagetable-resource.md) Resource-Definition. Для доступа к строкам сообщений используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .

Система предоставляет таблицу сообщений с [кодами системных ошибок](system-error-codes.md). Чтобы получить строку, которая соответствует коду ошибки, вызовите метод [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с \_ сообщением Format \_ из \_ системного флага.

Чтобы предоставить таблицу сообщений для приложения, следуйте инструкциям в [текстовых файлах сообщения](../eventlog/message-text-files.md). Чтобы получить строки из таблицы сообщений, вызовите метод [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с \_ сообщением Format \_ из \_ флага хмодуле.

 

 
