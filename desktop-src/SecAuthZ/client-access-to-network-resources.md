---
description: Описание стратегий доступа к сетевым ресурсам.
ms.assetid: d55b3204-430d-4fa4-b7a7-1e279beed8e3
title: Клиентский доступ к сетевым ресурсам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0873a10c708f9aab2e9c250375a63e8a2167873
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647214"
---
# <a name="client-access-to-network-resources"></a>Клиентский доступ к сетевым ресурсам

Сервер может использовать следующие стратегии для доступа к сетевым ресурсам.

-   Если у сервера есть имя учетной записи и пароль клиента, он может вызвать [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) с [*учетными данными*](/windows/desktop/SecGloss/c-gly) клиента, чтобы связать букву локального диска с сетевым ресурсом.
-   После вызова функции [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) с учетными данными клиента сервер может вызвать функцию [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) , чтобы [создать процесс для клиента](processes-in-the-client-security-context.md). Этот новый клиентский процесс может получить доступ к сетевым ресурсам с помощью [*контекста безопасности*](/windows/desktop/SecGloss/s-gly)клиента. Например, процесс может вызвать функцию [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) , чтобы открыть файл на удаленном компьютере. Система использует [*основной маркер*](/windows/desktop/SecGloss/p-gly) клиента для проверки попыток доступа клиентским процессом.
-   Сервер может вызвать [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a) с учетными данными null, чтобы установить подключение к сетевому ресурсу с доступом к серверу или подключение по умолчанию. Если сервер работает под учетной записью LocalSystem, он выполняет проверку подлинности в сетевом ресурсе в [*контексте безопасности*](/windows/desktop/SecGloss/s-gly) сервера домена. Если сервер работает под учетной записью службы, он выполняет проверку подлинности в качестве этой учетной записи. Дополнительные сведения см. в [учетной записи LocalSystem](/windows/desktop/Services/localsystem-account).

Сведения о защите паролей см. в разделе [обработка паролей](/windows/desktop/SecBP/handling-passwords). Дополнительные сведения о получении учетных данных см. [в разделе запрос учетных данных у пользователя](/windows/desktop/SecBP/asking-the-user-for-credentials).

 

 
