---
description: Чтобы создать приложение для WMI с помощью C++, необходимо инициализировать COM, доступ и задать протоколы WMI, а также выполнить ручную очистку.
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Создание приложения WMI с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348405"
---
# <a name="creating-a-wmi-application-using-c"></a>Создание приложения WMI с помощью C++

Чтобы создать приложение для WMI с помощью C++, необходимо инициализировать COM, доступ и задать протоколы WMI, а также выполнить ручную очистку. Однако C++ обладает преимуществом гибкости и энергопотребления. Таким образом, если вы лучше используете Visual Basic Scripting Edition (VBScript) или Windows PowerShell для простых процессов, C++ работает лучше для более сложных приложений и требуется для написания [поставщиков](providing-data-to-wmi.md).

В следующей процедуре описывается создание приложения WMI.

**Создание приложения WMI**

1.  [Инициализация COM](initializing-com-for-a-wmi-application.md).

    Поскольку Инструментарий WMI основан на технологии COM, необходимо выполнять вызовы функций [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) для доступа к WMI.

2.  [Создайте соединение с пространством имен WMI](creating-a-connection-to-a-wmi-namespace.md).

    По определению Инструментарий WMI работает в процессе, отличном от процесса приложения. Поэтому необходимо создать подключение между приложением и WMI.

3.  [Задайте уровни безопасности для WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).

    Чтобы использовать подключение, созданное в WMI, необходимо задать уровни олицетворения и проверки подлинности для приложения.

4.  Реализуйте назначение приложения.

    Инструментарий WMI предоставляет разнообразные интерфейсы COM, используемые для доступа к данным и управления ими на предприятии. Дополнительные сведения см. в статьях [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md), [Получение WMI-события](receiving-a-wmi-event.md)и [COM API для WMI](com-api-for-wmi.md).

    Именно здесь должно существовать основная часть клиентского приложения инструментария WMI, например доступ к объектам WMI или обработка данных.

5.  [Очистка и завершение работы приложения](cleaning-up-and-shutting-down-a-wmi-application.md).

    После выполнения запросов к инструментарию WMI следует уничтожить все COM-указатели и правильно завершить работу приложения.

Дополнительные сведения и пример кода о создании приложения WMI см. в разделе [пример. Создание приложения WMI](example-creating-a-wmi-application.md).

 

 
