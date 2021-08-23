---
description: компоненты Windows SDK для установщик Windows разработчиков содержат файлы VBScript, демонстрирующие использование интерфейса автоматизации установщик Windows для изменения пакетов установщик Windows.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Windows Примеры сценариев для установщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3addf648460418daad783b6c5dbcc71078f9904c4a0bba1324f025896692cd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065774"
---
# <a name="windows-installer-scripting-examples"></a>Windows Примеры сценариев для установщика

[компоненты Windows SDK для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md) содержат файлы VBScript, демонстрирующие использование интерфейса автоматизации установщик Windows для изменения пакетов установщик Windows.

Примеры сценариев, указанные в этом разделе, не поддерживаются корпорацией Майкрософт, и они предоставляются только как потенциально полезные справочные материалы. для выполнения этих примеров требуется сервер сценариев Windows. дополнительные сведения о сервере сценариев Windows см. в разделе [сервер скриптов Windows](/previous-versions//9bbdkx3k(v=vs.85)) раздела пакет средств разработки программного обеспечения Microsoft Windows.



| Пример файла скрипта | Описание                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Вывод списка продуктов, свойств, компонентов и компонентов](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Импорт файлов](import-files.md)                                                                            |
| WiExport.vbs       | [Экспорт файлов](export-files.md)                                                                            |
| WiSubStg.vbs       | [Управление подхранилищами](manage-substorages.md)                                                                |
| WiStream.vbs       | [управление двоичными Потоки](manage-binary-streams.md)                                                          |
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
| WiRunSQL.vbs       | [выполнение инструкций SQL](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [Копирование файла ANSI в поле базы данных](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Составить список компонентов](list-components.md)                                                                      |
| WiFeatur.vbs       | [Функции списка](list-features.md)                                                                          |
| WiDialog.vbs       | [Предварительный просмотр пользовательского интерфейса](preview-user-interface.md)                                                        |



 

Все эти сценарии отображают экран справки с описанием аргументов командной строки. чтобы отобразить экран справки в Windows дважды щелкните файл. Чтобы отобразить экран справки из командной строки, введите? в качестве первого аргумента или введите меньше аргументов, чем требуется. Скрипты возвращают значение 0 для успешного выполнения, 1 при вызове справки и 2 в случае сбоя.

для выполнения этих примеров требуется Windows сервера сценариев. Windows Сервер сценариев на самом деле состоит из двух узлов:

-   CScript.exe — это версия, позволяющая запускать скрипты из командной строки, а также переключатели для установки свойств скриптов.
-   WScript.exe — это версия сервера сценариев Windows, позволяющая выполнять скрипты из Windows. дополнительные сведения см. в разделе [Windows сценариев](/previous-versions//9bbdkx3k(v=vs.85)) в Windows SDK.

программа Makecab.exe входит в состав примеров установки исправлений в [Windows SDK компонентов для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md).

дополнительные сведения об инструментарии wmi см. в разделе [использование установщик Windows с wmi](using-windows-installer-with-wmi.md).

 

 
