---
title: Использование BITS
description: Использование BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Фоновая интеллектуальная служба передачи
- Фоновая интеллектуальная служба передачи, задачи
- БИТЫ передачи файлов
- Использование битов BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b301c1d96956bca924d99ef41ade3032f58dc4e194b420069cbae1071c916b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801164"
---
# <a name="using-bits"></a>Использование BITS

Ниже показано, как выполнить перенос файлов с помощью  [интерфейсов](bits-interfaces.md)ФОНОВАЯ интеллектуальная служба передачи (BITS).

**Выполнение обмена файлами**

1.  [Подключение службе BITS](connecting-to-the-bits-service.md)
2.  [Создание задания перемещения](creating-a-job.md)
3.  [Добавление файлов в задание](adding-files-to-a-job.md)
4.  [Запустите задание](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Определение успешной передачи файлов службой BITS](determining-the-status-of-a-job.md)
6.  [Завершение задания](completing-and-canceling-a-job.md)

На предыдущих шагах показано, как передавать файлы, используя значения свойств по умолчанию для задания. Поведение по умолчанию можно изменить, изменив одно или несколько значений свойств задания. Например, можно изменить приоритет обработки задания относительно других заданий в очереди, указать свой собственный параметр прокси-сервера и зарегистрироваться для получения уведомления о событии при передаче файлов службой BITS. Дополнительные сведения см. [в разделе Установка и получение свойств задания](setting-and-retrieving-the-properties-of-a-job.md).

Windows PowerShell предоставляет простой механизм управления множеством задач BITS. этот раздел содержит следующие разделы, в которых показано, как использовать командлеты Windows PowerShell с BITS.

-   [Использование Windows PowerShell для создания заданий передачи BITS](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Использование командлетов Windows PowerShell в WinRM для управления заданиями передачи BITS](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [использование командлетов WMI Windows PowerShell для управления облегченным сервером BITS](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> начиная с Windows 10 версии 1607 можно также запускать командлеты PowerShell и использовать битсадмин или другие приложения, использующие [интерфейсы](bits-interfaces.md) BITS из удаленной командной строки PowerShell, подключенной к другому компьютеру (физическому или виртуальному). Эта возможность недоступна при использовании командной строки [PowerShell Direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) для виртуальной машины на том же физическом компьютере и недоступна при использовании командлетов WinRM.
>
> Задание BITS, созданное на основе удаленного сеанса PowerShell, будет выполняться в контексте учетной записи пользователя этого сеанса и будет работать только при наличии хотя бы одного активного локального сеанса входа или удаленного сеанса PowerShell, связанного с этой учетной записью пользователя. Дополнительные сведения см. [в разделе Управление удаленными сеансами PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).

 

Этот раздел также содержит следующие разделы:

-   [Рекомендации по использованию BITS](best-practices-when-using-bits.md)
-   [Перечисление заданий в очереди на перемещение](enumerating-jobs-in-the-transfer-queue.md)
-   [Перечисление файлов в задании](enumerating-files-in-a-job.md)
-   [Обработка ошибок](handling-errors.md)
-   [Получение ответа из задания отправки и ответа](retrieving-the-reply-from-an-upload-reply-job.md)

Пример кода, в котором используются интерфейсы BITS, см. в разделе [примеры и средства BITS](bits-samples-and-tools.md).

 

 