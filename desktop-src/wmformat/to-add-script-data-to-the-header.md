---
title: Добавление данных скрипта в заголовок
description: Добавление данных скрипта в заголовок
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media Format SDK, добавление данных скрипта в заголовки
- Расширенный системный формат (ASF), добавление данных скрипта в заголовки
- ASF (Расширенный системный формат), добавление данных скрипта в заголовки
- скрипты, добавление данных в заголовки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105700827"
---
# <a name="to-add-script-data-to-the-header"></a>Добавление данных скрипта в заголовок

Команды сценария можно включить в заголовок файла ASF. Чтобы записать команды сценария в заголовок во время кодирования, выполните следующие действия. Перед вызовом [**ивмвритер:: бегинвритинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)выполните следующие действия.

1.  Получите указатель на интерфейс **ивмхеадеринфо** , вызвав **Ивмвритер:: QueryInterface**.
2.  Добавьте каждую нужную команду сценария, вызвав [**ивмхеадеринфо:: аддскрипт**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript). Каждый вызов принимает две строки отдельно и время презентации для использования в качестве параметров команды.

Когда приложение считывает файл, ему необходимо получить все команды сценария. Чтобы найти все команды сценария в заголовке файла, выполните следующие действия. Это необходимо сделать перед запуском воспроизведения.

1.  Получите указатель на интерфейс **ивмхеадеринфо** объекта чтения (или синхронного объекта Reader), вызвав метод **QueryInterface** другого интерфейса в объекте.
2.  Получение общего числа скриптов в заголовке путем вызова [**ивмхеадеринфо:: жетскрипткаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).
3.  Перебрать все скрипты в заголовке по одному за раз, используя вызовы [**ивмхеадеринфо:: надстрочный**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).
4.  Создайте список времени презентации, чтобы приложение могла реагировать на команды в нужное время.

> [!Note]  
> При использовании DRM для шифрования файла ни одна из команд сценария не может иметь время презентации, равное 0.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Интерфейс Ивмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Использование команд сценария**](using-script-commands.md)
</dt> </dl>

 

 




