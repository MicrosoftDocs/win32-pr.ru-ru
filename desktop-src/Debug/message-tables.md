---
description: Таблицы сообщений — это специальные строковые ресурсы, используемые при отображении сообщений об ошибках. Они объявляются в файле ресурсов с помощью инструкции МЕССАЖЕТАБЛЕ Resource-Definition. Для доступа к строкам сообщений используйте функцию FormatMessage.
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: Таблицы сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6141f78342db2554e85053adda7ee68bdb0e855f213f103da1bb7f62eac1d703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691824"
---
# <a name="message-tables"></a>Таблицы сообщений

Таблицы сообщений — это специальные строковые ресурсы, используемые при отображении сообщений об ошибках. Они объявляются в файле ресурсов с помощью инструкции [мессажетабле](../menurc/messagetable-resource.md) Resource-Definition. Для доступа к строкам сообщений используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) .

Система предоставляет таблицу сообщений с [кодами системных ошибок](system-error-codes.md). Чтобы получить строку, которая соответствует коду ошибки, вызовите метод [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с \_ сообщением Format \_ из \_ системного флага.

Чтобы предоставить таблицу сообщений для приложения, следуйте инструкциям в [текстовых файлах сообщения](../eventlog/message-text-files.md). Чтобы получить строки из таблицы сообщений, вызовите метод [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с \_ сообщением Format \_ из \_ флага хмодуле.

 

 
