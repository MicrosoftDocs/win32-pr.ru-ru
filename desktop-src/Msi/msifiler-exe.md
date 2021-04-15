---
description: MsiFiler.exe заполняет таблицу файлов версиями, языками и размерами на основе исходного каталога. Также можно обновить таблицу Мсифилехаш с помощью хэшей файлов.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662370"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe заполняет [таблицу файлов](file-table.md) версиями, языками и размерами на основе исходного каталога. Также можно обновить [таблицу мсифилехаш](msifilehash-table.md) с помощью хэшей файлов.

## <a name="syntax"></a>Синтаксис

**msifiler.exe-d** *{Database}* **\[ -v \] \[ -h \] \[ -s алтсаурце \]**

## <a name="command-line-options"></a>Параметры командной строки

В Msifiler.exe используются следующие параметры командной строки без учета регистра. Вместо тире можно использовать разделитель с косой чертой.



| Параметр | Параметр   | Описание                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | База данных (MSI-файл), которая должна быть обновлена.                                                                                                                              |
| -v     |             | Использовать режим подробного вывода.                                                                                                                                                            |
| -H     |             | Заполнение [таблицы мсифилехаш](msifilehash-table.md). При этом создается таблица, если она еще не существует. Таблицу Мсифилехаш можно использовать только с файлами без версий. |
| -S     | *алтсаурце* | АЛТСАУРЦЕ указывает альтернативный каталог для поиска файлов.                                                                                                              |



 

Это средство доступно только в [компонентах Windows SDK для разработчиков установщик Windows](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Средства разработки установщик Windows](windows-installer-development-tools.md)
</dt> <dt>

[Использование таблицы Directory](using-the-directory-table.md)
</dt> <dt>

[Выпущенные версии, средства и распространяемые пакеты](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



