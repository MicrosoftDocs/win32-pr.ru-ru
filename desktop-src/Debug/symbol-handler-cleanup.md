---
description: Чтобы освободить всю память, используемую обработчиком символов для процесса, используйте функцию Симклеануп.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Очистка обработчика символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895693"
---
# <a name="symbol-handler-cleanup"></a>Очистка обработчика символов

Чтобы освободить всю память, используемую обработчиком символов для процесса, используйте функцию [**симклеануп**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) . Эта функция перечисляет все загруженные модули, освобождает каждый модуль и освобождает память, выделенную для списка модулей. После вызова **симклеануп** нельзя использовать обработчик процесса в функциях обработки символов, пока не будет вызвана функция [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

 

 



