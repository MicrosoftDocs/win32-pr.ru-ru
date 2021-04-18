---
description: Пакеты проверки подлинности Windows предоставляют службы проверки подлинности путем реализации функциональных возможностей пакета для функций Лсалогонусер и LsaCallAuthenticationPackage, предоставляемых LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Пакеты проверки подлинности Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541151"
---
# <a name="windows-authentication-packages"></a>Пакеты проверки подлинности Windows

Пакеты проверки подлинности Windows предоставляют службы проверки подлинности путем реализации функциональных возможностей пакета для функций [**лсалогонусер**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) и [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) , предоставляемых LSA.

MSV1 \_ 0 является примером [*пакета проверки подлинности*](../secgloss/a-gly.md)Windows. Пакет MSV1 \_ 0 принимает имя пользователя и [*хэшированный*](../secgloss/h-gly.md) пароль, который выполняется в базе данных [*диспетчера учетных записей безопасности*](../secgloss/s-gly.md) (SAM). В зависимости от результатов поиска \_ пакет проверки подлинности MSV1 0 принимает или отклоняет попытки проверки подлинности.

Список функций поддержки, предоставляемых LSA для использования пакетами проверки подлинности Windows, которые нуждаются в системных службах, см. в разделе [функции LSA, вызываемые пакетами проверки подлинности](authentication-functions.md).

Пакеты проверки подлинности Windows должны реализовывать набор функций, которые вызываются LSA. Полный список функций см. в разделе [функции, реализованные пакетами проверки подлинности](authentication-functions.md).

 

 
