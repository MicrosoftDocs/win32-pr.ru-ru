---
description: описывает методы открытия элемента панели управления для Windows Vista и более поздних систем, а также для работы с устаревшими командами панели управления.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Исполнение элементов панели управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb6ae2fa08231d3876e1a5a636e404f519f4a6
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581762"
---
# <a name="executing-control-panel-items"></a>Исполнение элементов панели управления

> [!Note]  
> Если вы ищете список канонических имен и имена модулей для элементов панели управления, см. раздел [канонические имена элементов панели управления](controlpanel-canonical-names.md).

 

Существует два способа открыть элемент панели управления:

-   Пользователь может открыть панель управления, а затем открыть элемент, щелкнув или дважды щелкнув значок элемента.
-   Пользователь или приложение может запустить элемент панели управления, выполнив его непосредственно из командной строки.

Приложение может открыть панель управления программным способом с помощью функции [**винексек**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



В следующем примере показано, как приложение может запустить элемент панели управления с именем **MyCpl.cpl** с помощью функции [**винексек**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



При открытии элемента панели управления с помощью командной строки можно указать, что он открывается на определенной вкладке в элементе. из-за добавления и удаления определенных вкладок в некоторых элементах панели управления Windows Vista нумерация вкладок могла быть изменена в Windows XP. например, следующий пример запускает четвертую вкладку в системном элементе на Windows XP и третьей вкладке в Windows Vista.


```
control.exe sysdm.cpl,,3
```



В этом разделе обсуждается следующее.

-   [Windows Канонические имена в Vista](#windows-vista-canonical-names)
-   [новые команды для Windows Vista](#new-commands-for-windows-vista)
-   [Устаревшие команды панели управления](#legacy-control-panel-commands)
-   [Связанные разделы](#related-topics)

## <a name="windows-vista-canonical-names"></a>Windows Канонические имена в Vista

в Windows Vista и более поздних версиях предпочтительным способом запуска элемента панели управления из командной строки является использование канонического имени элемента панели управления. Каноническое имя — это нелокализованная строка, которая объявляется элементом панели управления в реестре. Значение по каноническому имени состоит в том, что оно абстрагирует имя модуля элемента панели управления. Элемент можно реализовать в .dll и затем повторно реализовать в качестве .exe или изменить имя модуля. При условии, что каноническое имя остается неизменным, любая программа, открывающая ее с помощью этого канонического имени, не нуждается в обновлении.

По соглашению каноническое имя формируется как "Корпоратионнаме. Контролпанелитемнаме".

в следующем примере показано, как приложение может запустить элемент панели управления **Центр обновления Windows** с [**винексек**](/windows/win32/api/winbase/nf-winbase-winexec).


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Чтобы запустить элемент панели управления с каноническим именем, используйте: "% SystemRoot% \\ system32 \\control.exe/Name *каноникалнаме*"

Чтобы открыть определенную подстраницу в элементе или открыть ее с дополнительными параметрами, используйте: "% SystemRoot% \\ system32 \\control.exe/Name **каноникалнаме** очищенную **PageName**"

Приложение может также реализовать метод [**иопенконтролпанел:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) для запуска элементов панели управления, включая возможность открытия конкретной подстраницы.

Полный список канонических имен элементов панели управления см. в разделе [канонические имена элементов панели управления](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>новые команды для Windows Vista

в Windows Vista некоторые параметры, которые были доступны в .cplном модуле в Windows XP, теперь реализуются как .exe файлы. Это обеспечивает дополнительную безопасность, разрешая стандартным пользователям получать запрос на ввод учетных данных администратора при попытке запуска файлов. к параметрам, которые не нуждаются в дополнительной безопасности, обращаются те же командные строки, которые использовались в Windows XP. ниже приведен список команд, используемых в Windows Vista для доступа к конкретным вкладкам элементов панели управления.

### <a name="personalization"></a>Personalization

-   Размер шрифта и число точек на дюйм:% WINDIR% \\ system32 \\DpiScaling.exe
-   разрешение экрана:% windir% \\ system32 \\control.exe desk.cpl, Параметры@Settings
-   параметры экрана:% windir% \\ system32 \\control.exe desk.cpl, Параметры@Settings
-   Темы:% WINDIR% \\ system32 \\control.exe desk.cpl, темы@Themes
-   Экранная заставка:% WINDIR% \\ system32 \\control.exe desk.cpl, экранная заставка@screensaver
-   Несколько мониторов:% WINDIR% \\ system32 \\control.exe desk.cpl, монитор,@Monitor
-   Цветовая схема:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Personal очищенную пажеколоризатион
-   Фон рабочего стола:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Personal очищенную пажеваллпапер

> [!Note]  
> Выпуски Starter и Basic не поддерживают команду control.exe/Name Microsoft. Personal.

 

### <a name="system"></a>Система

-   Производительность:% WINDIR% \\ system32 \\SystemPropertiesPerformance.exe
-   Удаленный доступ:% WINDIR% \\ system32 \\SystemPropertiesRemote.exe
-   Имя компьютера:% WINDIR% \\ system32 \\SystemPropertiesComputerName.exe
-   Защита системы:% WINDIR% \\ system32 \\SystemPropertiesProtection.exe
-   Дополнительные свойства системы:% WINDIR% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>"Программы и компоненты",

-   Установка и удаление программ:% WINDIR% \\ system32 \\control.exe/Name Microsoft. програмсандфеатурес
-   Windows функции:% windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Региональные и языковые параметры

-   Клавиатура:% systemroot% \\ system32 \\control.exe/Name Microsoft. регионаландлангуажеоптионс очищенную/p: "клавиатура"
-   Расположение:% systemroot% \\ system32 \\control.exe/Name Microsoft. регионаландлангуажеоптионс очищенную/p: "Location"
-   Администрирование:% systemroot% \\ system32 \\control.exe/Name Microsoft. регионаландлангуажеоптионс очищенную/p: "Administrative"

### <a name="folder-options"></a>Свойства папки

-   Поиск папки:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, параметры программы \_ Rundll 2
-   Сопоставления файлов:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Дефаултпрограмс очищенную пажефилеассок
-   Представление:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, параметры программы \_ Rundll 7
-   Общие:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, параметры программы \_ Rundll 0

### <a name="power-options"></a>Параметры электропитания

-   Изменение текущих параметров плана:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Повероптионс очищенную пажеплансеттингс
-   Параметры системы:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Повероптионс очищенную пажеглобалсеттингс
-   Создайте схему управления питанием:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Повероптионс очищенную пажекреатеневплан
-   не существует канонической команды для страницы Advanced Параметры, доступ к которой осуществляется по старому способу:% windir% \\ system32 \\control.exe powercfg.cpl,, 3

## <a name="legacy-control-panel-commands"></a>Устаревшие команды панели управления

При использовании функции [**винексек**](/windows/win32/api/winbase/nf-winbase-winexec) система может распознать специальные команды панели управления. эти команды Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>control.exe Desktop</td>
<td>Открывает окно <strong>Свойства экрана</strong> .
<blockquote>
[!Note]<br />
Выпуски Starter и Basic не поддерживают эту команду.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Цвет control.exe</td>
<td>Открывает окно <strong>свойства отображения</strong> с выделенной вкладкой <strong>Оформление</strong> .</td>
</tr>
<tr class="odd">
<td>Дата и время control.exe</td>
<td>Открывает окно <strong>Свойства даты и времени</strong> .</td>
</tr>
<tr class="even">
<td>control.exe Международная</td>
<td>Открывает окно язык <strong>и региональные параметры</strong> .</td>
</tr>
<tr class="odd">
<td>control.exe мыши</td>
<td>Запускает окно <strong>свойств мыши</strong> .</td>
</tr>
<tr class="even">
<td>control.exe клавиатура</td>
<td>Запускает окно <strong>Свойства клавиатуры</strong> .</td>
</tr>
<tr class="odd">
<td>control.exe принтеры</td>
<td>Отображает папку <strong>Принтеры и факсы</strong> .</td>
</tr>
<tr class="even">
<td>control.exe шрифты</td>
<td>Отображает папку <strong>Fonts</strong> .</td>
</tr>
</tbody>
</table>



 

для Windows 2000 и более поздних систем:



| Команда                    | Описание                                              |
|----------------------------|----------------------------------------------------------|
| control.exe папки        | Открывает окно " **Свойства папки** ".                  |
| control.exe NetWare        | Запускает окно **Novell NetWare** (если установлено).   |
| control.exe телефонии      | открывает окно **параметры Телефон и модема** .         |
| control.exe админтулс     | Отображение папки " **Администрирование** ".            |
| control.exe счедтаскс     | Отображает папку **Назначенные задания** .                 |
| control.exe нетконнектионс | Отображает папку **Сетевые подключения** .             |
| control.exe инфракрасной связи       | Запускает окно " **Монитор инфракрасной связи** " (если установлено). |
| control.exe усерпассвордс  | Открывает окно **учетные записи пользователей** .                   |



 

## <a name="related-topics"></a>Связанные разделы

<dl> <dt>

[Элементы панели управления](control-panel-applications.md)
</dt> <dt>

[Руководство по работе пользователей](user-experience-guidelines.md)
</dt> <dt>

[Регистрация элементов панели управления](registering-control-panel-items.md)
</dt> <dt>

[Использование Кплапплет](using-cplapplet.md)
</dt> <dt>

[Обработка сообщений в панели управления](message-processing.md)
</dt> <dt>

[Расширение элементов панели управления "система"](extending-system-control-panel-items.md)
</dt> <dt>

[Назначение категорий панели управления](assigning-control-panel-categories.md)
</dt> <dt>

[Создание ссылок на задачи с возможностью поиска для элемента панели управления](creating-searchable-task-links.md)
</dt> <dt>

[доступ к панели управления в режиме Сейф в разделе Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
