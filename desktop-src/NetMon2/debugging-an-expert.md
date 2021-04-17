---
description: Используйте следующую процедуру для отладки экспертов, написанных на Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Отладка эксперта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663640"
---
# <a name="debugging-an-expert"></a>Отладка эксперта

Используйте следующую процедуру для отладки экспертов, написанных на Microsoft Visual C++.

**Отладка эксперта**

1.  Установите эксперт (DLL-файл) и файл базы данных программы (. pdb), созданный при компиляции эксперта в нужное расположение. Дополнительные сведения см. [в статье Установка эксперта в сетевой монитор 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Запустите Microsoft Visual C++.
3.  В меню **файл** щелкните **Открыть** и выберите имя библиотеки DLL эксперта.
4.  После загрузки Microsoft Visual C++ в меню **проект** выберите пункт **Параметры**.
5.  Нажмите кнопку **Отладка**. В разделе **исполняемый файл для сеанса отладки** введите полный путь к Netmon.exe, например:

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Задайте точки останова в коде.

 

 



