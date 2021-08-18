---
description: Windows пакеты аутентификации предоставляют службы проверки подлинности, реализуя зависящие от пакета функции для функций лсалогонусер и LsaCallAuthenticationPackage, предоставляемых LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows Пакеты проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8288e54398702994938627b13c745a67f96fbc44dc710e2e5a7ac65a8620685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915083"
---
# <a name="windows-authentication-packages"></a>Windows Пакеты проверки подлинности

Windows пакеты аутентификации предоставляют службы проверки подлинности, реализуя зависящие от пакета функции для функций [**лсалогонусер**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) и [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) , предоставляемых LSA.

MSV1 \_ 0 является примером [*пакета проверки подлинности*](../secgloss/a-gly.md)Windows. Пакет MSV1 \_ 0 принимает имя пользователя и [*хэшированный*](../secgloss/h-gly.md) пароль, который выполняется в базе данных [*диспетчера учетных записей безопасности*](../secgloss/s-gly.md) (SAM). В зависимости от результатов поиска \_ пакет проверки подлинности MSV1 0 принимает или отклоняет попытки проверки подлинности.

список функций поддержки, предоставляемых LSA для использования Windows пакетах проверки подлинности, требующих системных служб, см. в разделе [функции LSA, вызываемые пакетами проверки подлинности](authentication-functions.md).

Windows пакеты проверки подлинности должны реализовывать набор функций, которые вызываются LSA. Полный список функций см. в разделе [функции, реализованные пакетами проверки подлинности](authentication-functions.md).

 

 
