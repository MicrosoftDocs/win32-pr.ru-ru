---
description: Crypt32.dll — это модуль, который реализует многие функции CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Версии Crypt32.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809341"
---
# <a name="crypt32dll-versions"></a>Версии Crypt32.dll

Crypt32.dll — это модуль, который реализует многие функции сертификатов и шифрования сообщений в интерфейсе CryptoAPI, например [**криптсигнмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage). Crypt32.dll — это модуль, входящий в состав операционных систем Windows и Windows Server, но разные версии этой библиотеки предоставляют различные возможности. Нет API для определения используемой версии CryptoAPI, но вы можете определить версию Crypt32.dll, которая используется в данный момент с помощью функций [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) и [**веркуеривалуе**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .

В общем случае диапазоны версий Crypt32.dll сопоставляются с версиями операционной системы, как показано в следующей таблице. Однако эта таблица должна использоваться только в качестве рекомендации, так как это возможно благодаря другим способам обновления, что Crypt32.dll версия будет отличаться от указанной в таблице.

| Версия Crypt32.dll                               | Операционная система                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *версия* >= 5.131.3790.0                      | Windows Server 2003                                                                                                                                                             |
| *версия* >= 5.131.2600.1243                   | Windows XP с пакетом обновления 2 (SP2) Windows XP с пакетом обновления 1 (SP1) с исправлением [Q329433](https://support.microsoft.com/kb/329433)<br/> Windows XP<br/> |
| 5.131.2600.0 <= *версия* < 5.131.2600.1243 | Windows XP с SP1Windows XP<br/>                                                                                                                                        |



 

 

 
