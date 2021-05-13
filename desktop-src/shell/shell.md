---
description: Представляет объекты в оболочке. Предоставляются методы для управления оболочкой и выполнения команд в оболочке. Существуют также методы для получения других объектов, связанных с оболочкой.
title: 'Объект оболочки (Shldisp.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 75fc151e-5b9e-476b-b4e5-b848917357a8
ms.openlocfilehash: 55f8062b71e553ec5ceefa413b45f439874744b8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841765"
---
# <a name="shell-object"></a>Объект оболочки

Представляет объекты в оболочке. Предоставляются методы для управления оболочкой и выполнения команд в оболочке. Существуют также методы для получения других объектов, связанных с оболочкой.

## <a name="members"></a>Элементы

Объект **оболочки** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **оболочки** содержит следующие методы.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Метод</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-addtorecent"><strong>аддторецент</strong></a></td>
<td style="text-align: left;">Добавляет файл в список последних использованных файлов (MRU).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-browseforfolder.md"><strong>бровсефорфолдер</strong></a></td>
<td style="text-align: left;">Создает диалоговое окно, которое позволяет пользователю выбрать папку, а затем возвращает объект <a href="folder.md"><strong>папки</strong></a> выбранной папки.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-canstartstopservice"><strong>канстартстопсервице</strong></a></td>
<td style="text-align: left;">Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-cascadewindows.md"><strong>каскадевиндовс</strong></a></td>
<td style="text-align: left;">Каскадное расположение всех окон на рабочем столе. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора <strong>окна каскадом</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Запускает указанное приложение панели управления (*. cpl). Если приложение уже открыто, будет активирован запущенный экземпляр. <br/>
<blockquote>
<p>[!Note]<br />
Начиная с Windows Vista, большинство приложений панели управления являются элементами оболочки и не могут быть открыты с помощью этой функции. Чтобы открыть эти приложения панели управления, передайте каноническое имя в control.exe. Пример:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-ejectpc.md"><strong>ежектпк</strong></a></td>
<td style="text-align: left;">Извлекает компьютер из стыковочного узла. Это то же самое, что и при нажатии кнопки " <strong>Пуск</strong> " и выборе пункта " <strong>извлечь компьютер</strong>", если компьютер поддерживает эту команду.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-explore.md"><strong>Просматриваем</strong></a></td>
<td style="text-align: left;">Открывает указанную папку в окне проводника Windows.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-explorerpolicy.md"><strong>експлорерполици</strong></a></td>
<td style="text-align: left;">Возвращает значение для указанной политики Internet Explorer.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-filerun.md"><strong>филерун</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>запуска</strong> для пользователя. Этот метод оказывает тот же результат, что и при щелчке меню <strong>Пуск</strong> и выборе <strong>Run</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-findcomputer.md"><strong>финдкомпутер</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Результаты поиска: компьютеры</strong> . В диалоговом окне отображается результат поиска указанного компьютера.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-findfiles.md"><strong>финдфилес</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Поиск: все файлы</strong> . Это то же самое, что и при нажатии кнопки « <strong>Пуск</strong> », а затем при выборе <strong>поиска</strong> (или его эквивалента в системах, предшествующих Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-findprinter"><strong>финдпринтер</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Поиск принтера</strong> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a></td>
<td style="text-align: left;">Извлекает параметр глобальной оболочки.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-getsysteminformation"><strong>жетсистеминформатион</strong></a></td>
<td style="text-align: left;">Возвращает сведения о системе.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-help.md"><strong>Справка</strong></a></td>
<td style="text-align: left;">Отображает центр справки и поддержки Windows. Этот метод действует так же, как и при щелчке меню <strong>Пуск</strong> и выбрав пункт <strong>Справка и поддержка</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isrestricted"><strong>Ограниченный доступ</strong></a></td>
<td style="text-align: left;">Извлекает из реестра параметр ограничений группы.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-isservicerunning"><strong>иссервицеруннинг</strong></a></td>
<td style="text-align: left;">Возвращает значение, указывающее, запущена ли определенная служба.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-minimizeall.md"><strong>минимизеалл</strong></a></td>
<td style="text-align: left;">Свертывает все окна на рабочем столе. Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора пункта <strong>Свернуть все окна</strong> в старых системах или нажатия значка <strong>Показывать Рабочий стол</strong> в области Быстрый запуск панели задач в Windows 2000 или Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-namespace.md"><strong>Имен</strong></a></td>
<td style="text-align: left;">Создает и возвращает объект <a href="folder.md"><strong>Folder</strong></a> для указанной папки.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-open.md"><strong>Открыт</strong></a></td>
<td style="text-align: left;">Открывает указанную папку.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-refreshmenu.md"><strong>рефрешмену</strong></a></td>
<td style="text-align: left;">Обновляет содержимое меню " <strong>Пуск</strong> ". Используется только с системами, предшествующими Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-searchcommand.md"><strong>сеарчкомманд</strong></a></td>
<td style="text-align: left;">Отображает панель поиска приложений.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestart"><strong>сервицестарт</strong></a></td>
<td style="text-align: left;">Запускает именованную службу.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-servicestop"><strong>сервицестоп</strong></a></td>
<td style="text-align: left;">Останавливает именованную службу.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Свойства даты и времени</strong> . Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра <strong>настроить дату и время</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a></td>
<td style="text-align: left;">Выполняет указанную операцию с указанным файлом.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/windows/desktop/shell/shell-showbrowserbar"><strong>шовбровсербар</strong></a></td>
<td style="text-align: left;">Отображает панель браузера.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-shutdownwindows.md"><strong>шутдовнвиндовс</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Завершение работы Windows</strong> . Это то же самое, что и при нажатии кнопки « <strong>Пуск</strong> », и при выборе « <strong>Завершение работы</strong>».<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-suspend.md"><strong>Анализируем</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-tilehorizontally.md"><strong>тилехоризонталли</strong></a></td>
<td style="text-align: left;">Мозаичное отображение всех окон на рабочем столе по горизонтали. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбор <strong>окон мозаики по горизонтали</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-tilevertically.md"><strong>тилевертикалли</strong></a></td>
<td style="text-align: left;">Располагает все окна на рабочем столе по вертикали. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбор <strong>окон мозаики по вертикали</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-toggledesktop.md"><strong>тоггледесктоп</strong></a></td>
<td style="text-align: left;">Отображает или скрывает Рабочий стол.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-trayproperties.md"><strong>трайпропертиес</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Свойства панели задач и меню "Пуск</strong> ". Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора <strong>свойств</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-undominimizeall.md"><strong>ундоминимизеалл</strong></a></td>
<td style="text-align: left;">Восстанавливает все настольные компьютеры в том же состоянии, в котором они находились до последней команды <a href="shell-minimizeall.md"><strong>минимизеалл</strong></a> . Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора команды <strong>отменить свернуть все окна</strong> в старых системах или второй щелчок значка Свернуть <strong>Рабочий стол</strong> в области Быстрый запуск панели задач в Windows 2000 или Windows XP.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Создает и возвращает объект <a href="shellwindows.md"><strong>шеллвиндовс</strong></a> . Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="shell-windowssecurity.md"><strong>виндовссекурити</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Безопасность Windows</strong> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="shell-windowswitcher.md"><strong>виндовсвитчер</strong></a></td>
<td style="text-align: left;">Отображает открытые окна в трехмерном стеке, который можно переворачивать.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Свойства

Объект **оболочки** имеет следующие свойства.



| Свойство                                            | Тип доступа          | Описание                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Приклад**](shell-application.md)<br/> | Только для чтения<br/> | Содержит объект приложения объекта.<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Только для чтения<br/> | Возвращает объект, представляющий родительский объект текущего объекта.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
