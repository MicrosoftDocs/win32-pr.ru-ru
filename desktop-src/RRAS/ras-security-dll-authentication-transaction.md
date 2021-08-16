---
title: Транзакция проверки подлинности DLL безопасности RAS
description: сервер RAS Windows NT/Windows 2000 вызывает функцию рассекуритидиалогбегин библиотеки безопасности, чтобы начать проверку подлинности удаленного пользователя.
ms.assetid: e6549812-d906-4163-b9c8-86f8f1cb1ad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea463c56d96cad13fb55a2b6e0bbdfc154518ba012e4c71c6ab8bdd3213cd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789480"
---
# <a name="ras-security-dll-authentication-transaction"></a>Транзакция проверки подлинности DLL безопасности RAS

сервер RAS Windows NT/Windows 2000 вызывает функцию [**рассекуритидиалогбегин**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) библиотеки безопасности, чтобы начать проверку подлинности удаленного пользователя. Сервер RAS заблокирован и не может принимать другие вызовы, пока **рассекуритидиалогбегин** не вернет. По этой причине **рассекуритидиалогбегин** должен скопировать входные параметры, создать поток для выполнения проверки подлинности и вернуть их как можно быстрее.

Поток, созданный БИБЛИОТЕКой безопасности, использует функции [**рассекуритидиалогсенд**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) и [**рассекуритидиалогрецеиве**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) для взаимодействия с удаленным компьютером. Эти функции недоступны для статического импорта из любой библиотеки. Вместо этого библиотека безопасности должна использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к этим функциям в RASMAN.DLL.

Во время транзакции проверки подлинности Диспетчер подключений RAS на удаленном компьютере отображает окно терминала. Поток библиотеки DLL безопасности вызывает [**рассекуритидиалогсенд**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogsend) для отправки сообщения, отображаемого в окне терминала. Затем поток вызывает [**рассекуритидиалогрецеиве**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) для получения входных данных, которые типы удаленных пользователей находятся в окне терминала. Поток может выполнять любое количество вызовов **рассекуритидиалогсенд** с каждым вызовом, за которым следует вызов **рассекуритидиалогрецеиве** . После каждого вызова **рассекуритидиалогрецеиве** поток должен вызвать одну из функций ожидания, например [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), чтобы дождаться завершения асинхронных операций Send и Receive. Сервер RAS сигнализирует объекту события о завершении операции получения или по истечении необязательного интервала времени ожидания.

Когда поток завершил проверку подлинности удаленного пользователя, он вызывает функцию [**рассекуритидиалогкомплете**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) . Этот вызов передает структуру [**\_ сообщений безопасности**](/windows/desktop/api/Rasshost/ns-rasshost-security_message) , содержащую результаты транзакции проверки подлинности, на сервер удаленного доступа. Затем сервер RAS выполняет последовательность очистки, которая включает вызов функции [**рассекуритидиаложенд**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogend) библиотеки DLL. Это дает библиотеке DLL безопасности возможность выполнить необходимую очистку.

Библиотека безопасности может вызывать функцию [**рассекуритидиалогжетинфо**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialoggetinfo) для получения сведений о порте, связанном с транзакцией проверки подлинности. **Рассекуритидиалогжетинфо** заполняет структуру [**\_ \_ сведений о безопасности RAS**](/windows/desktop/api/Rasshost/ns-rasshost-ras_security_info) , которая указывает состояние последнего вызова [**рассекуритидиалогрецеиве**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogreceive) для порта.

 

 