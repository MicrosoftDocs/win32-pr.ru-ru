---
description: Чтобы освободить всю память, используемую обработчиком символов для процесса, используйте функцию Симклеануп.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Очистка обработчика символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db42f1fedfe68af4ab6eab885aefff0e8eb56e4ac9262f79adef8733f7ee7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956963"
---
# <a name="symbol-handler-cleanup"></a>Очистка обработчика символов

Чтобы освободить всю память, используемую обработчиком символов для процесса, используйте функцию [**симклеануп**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) . Эта функция перечисляет все загруженные модули, освобождает каждый модуль и освобождает память, выделенную для списка модулей. После вызова **симклеануп** нельзя использовать обработчик процесса в функциях обработки символов, пока не будет вызвана функция [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

 

 



