---
title: Создание списка привязок переменных
description: Функция Снмпкреатевбл создает новый список привязок переменных.
ms.assetid: 18e8a04d-612f-4d85-9cff-8c541a4cdf71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2530b59524375ad6413ff9aa1416db8e25ee3641136284cb4a0f70795e388a8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009582"
---
# <a name="creating-a-variable-binding-list"></a>Создание списка привязок переменных

Функция [**снмпкреатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) создает новый список привязок переменных. Если в приложении WinSNMP указано имя переменной и значение, функция создает список и добавляет имя и значение в качестве первой записи в списке. Если в приложении для имени переменной указано **значение NULL** , то функция создает пустой список.

Чтобы скопировать список привязок переменных, вызовите функцию [**снмпдупликатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . Функция создает новый список привязок переменных и инициализирует новый список копией данных в списке привязок исходной переменной.

Функция [**снмпкреатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) и функция [**снмпдупликатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) выделяют любую необходимую память для нового списка привязок переменных. В приложении WinSNMP должны освобождаться ресурсы, связанные с этими списками. Рекомендуется, чтобы приложение выделило это, сопоставляя каждый вызов [**снмпкреатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) и [**снмпдупликатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) с соответствующим вызовом функции [**снмпфривбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl) , когда нужно освободить выделенную память.

 

 




