---
description: Компоненты Windows SDK для установщик Windows разработчиков содержат файлы VBScript, демонстрирующие использование интерфейса автоматизации установщик Windows для изменения пакетов установщик Windows.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Примеры сценариев установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c2ad75411201cdbf74ef3aa035906d7e58aa7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998739"
---
# <a name="windows-installer-scripting-examples"></a>Примеры сценариев установщик Windows

[Компоненты Windows SDK для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md) содержат файлы VBScript, демонстрирующие использование интерфейса автоматизации установщик Windows для изменения пакетов установщик Windows.

Примеры сценариев, указанные в этом разделе, не поддерживаются корпорацией Майкрософт, и они предоставляются только как потенциально полезные справочные материалы. Для выполнения этих примеров требуется сервер сценариев Windows. Дополнительные сведения о сервере сценариев Windows см. в разделе [сервер сценариев Windows](/previous-versions//9bbdkx3k(v=vs.85)) пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.



| Пример файла скрипта | Описание                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Вывод списка продуктов, свойств, компонентов и компонентов](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Импорт файлов](import-files.md)                                                                            |
| WiExport.vbs       | [Экспорт файлов](export-files.md)                                                                            |
| WiSubStg.vbs       | [Управление подхранилищами](manage-substorages.md)                                                                |
| WiStream.vbs       | [Управление двоичными потоками](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [Объединение двух баз данных](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [Создание преобразования](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [Применение преобразования](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | [Просмотр преобразования](view-a-transform.md) (только для cscript)                                                     |
| WiDiffDb.vbs       | [Просмотр различий между двумя базами данных](view-differences-between-two-databases.md) (только для cscript)         |
| WiLstScr.vbs       | [Просмотреть скрипт установщика](view-installer-script.md) (только для cscript)                                           |
| WiSumInf.vbs       | [Управление сводными сведениями](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [Управление параметрами политики](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [Управление языком и кодовой страницей](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [Копирование файла Юникода в файл ANSI](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [Управление размерами и версиями файлов](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [Создать CAB-файл](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [Выполнение инструкций SQL](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [Копирование файла ANSI в поле базы данных](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Составить список компонентов](list-components.md)                                                                      |
| WiFeatur.vbs       | [Функции списка](list-features.md)                                                                          |
| WiDialog.vbs       | [Предварительный просмотр пользовательского интерфейса](preview-user-interface.md)                                                        |



 

Все эти сценарии отображают экран справки с описанием аргументов командной строки. Чтобы отобразить экран справки в Windows, дважды щелкните файл. Чтобы отобразить экран справки из командной строки, введите? в качестве первого аргумента или введите меньше аргументов, чем требуется. Скрипты возвращают значение 0 для успешного выполнения, 1 при вызове справки и 2 в случае сбоя.

Для этих примеров требуется запуск сервера сценариев Windows. Сервер сценариев Windows на самом деле состоит из двух узлов:

-   CScript.exe — это версия, позволяющая запускать скрипты из командной строки, а также переключатели для установки свойств скриптов.
-   WScript.exe — это версия сервера сценариев Windows, позволяющая запускать сценарии из Windows. Дополнительные сведения см. в разделе " [сервер сценариев Windows](/previous-versions//9bbdkx3k(v=vs.85)) " в Windows SDK.

Программа Makecab.exe входит в состав примеров установки исправлений в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).

Дополнительные сведения об инструментарии WMI см. в разделе [использование установщик Windows с WMI](using-windows-installer-with-wmi.md).

 

 
