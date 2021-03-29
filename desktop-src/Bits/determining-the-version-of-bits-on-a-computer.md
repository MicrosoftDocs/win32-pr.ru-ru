---
title: Определение версии BITS на компьютере
description: Чтобы определить версию BITS на клиентском компьютере, проверьте версию QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773397"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>Определение версии BITS на компьютере

Чтобы определить версию BITS на клиентском компьютере, проверьте версию QMgr.dll. Чтобы найти номер версии библиотеки DLL, выполните следующие действия.

-   Обнаружение QMgr.dll в папке% WINDIR% \\ System32.
-   Щелкните правой кнопкой мыши QMgr.dll и выберите пункт **Свойства**.
-   Перейдите на вкладку **версия** .
-   Запишите номер версии.

Для определения версии библиотеки DLL в системе можно также использовать следующий код PowerShell:

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

Если библиотека DLL также существует в битах% WINDIR% \\ system32 \\ , повторите предыдущие шаги. Служба BITS использует библиотеку DLL с более высоким номером версии.

В следующей таблице перечислены версии битов и соответствующие номера версий файлов QMgr.dll.



| Версия BITS | Номер версии файла QMgr.dll |
|--------------|------------------------------|
| BITS 10,1    | 7,8. xxxx. xxxx                |
| BITS 5,0     | 7.7. xxxx. xxxx                |
| BITS 4,0     | 7,5. xxxx. xxxx                |
| BITS 3,0     | 7.0. xxxx. xxxx                |
| BITS 2,5     | 6.7. xxxx. xxxx                |
| BITS 2,0     | 6,6. xxxx. xxxx                |
| BITS 1,5     | 6.5. xxxx. xxxx                |
| BITS 1,2     | 6.2. xxxx. xxxx                |
| BITS 1,0     | 6.0. xxxx. xxxx                |



 

Кроме того, можно использовать символьные идентификаторы классов для определения версии битов, зарегистрированных на компьютере. В следующей таблице перечислены версии битов и соответствующие им символьные идентификаторы классов. Функция **CoCreateInstance** возвращает **регдб \_ E \_ класснотрег** , если класс не зарегистрирован.



| Версия BITS  | Символьный идентификатор класса         |
|---------------|-----------------------------------|
| BITS 10,1     | CLSID \_ BackgroundCopyManager10 \_ 1 |
| BITS 5,0      | CLSID \_ BackgroundCopyManager5 \_ 0  |
| BITS 4,0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| BITS 3,0      | CLSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2,5      | CLSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2,0      | CLSID \_ BackgroundCopyManager2 \_ 0  |
| BITS 1,5      | CLSID \_ BackgroundCopyManager1 \_ 5  |
| BITS 1,2, 1,0 | \_БАККГРАУНДКОПИМАНАЖЕР CLSID      |



 

 

 




