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
ms.openlocfilehash: d31adcbf5a12d699750029c15a308ef73f4d8c03
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467231"
---
# <a name="shell-object"></a>Объект оболочки

Представляет объекты в оболочке. Предоставляются методы для управления оболочкой и выполнения команд в оболочке. Существуют также методы для получения других объектов, связанных с оболочкой.

## <a name="members"></a>Элементы

Объект **оболочки** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **оболочки** содержит следующие методы.




| Метод | Описание | 
|--------|-------------|
| <a href="/windows/desktop/shell/shell-addtorecent"><strong>аддторецент</strong></a> | Добавляет файл в список последних использованных файлов (MRU).<br /> | 
| <a href="shell-browseforfolder.md"><strong>бровсефорфолдер</strong></a> | Создает диалоговое окно, которое позволяет пользователю выбрать папку, а затем возвращает объект <a href="folder.md"><strong>папки</strong></a> выбранной папки.<br /> | 
| <a href="/windows/desktop/shell/shell-canstartstopservice"><strong>канстартстопсервице</strong></a> | Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.<br /> | 
| <a href="shell-cascadewindows.md"><strong>каскадевиндовс</strong></a> | Каскадное расположение всех окон на рабочем столе. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора <strong>Windows каскадом</strong>.<br /> | 
| <a href="shell-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Запускает указанное приложение панели управления (* .cpl). Если приложение уже открыто, будет активирован запущенный экземпляр. <br /><blockquote><p>[!Note]<br />начиная с Windows Vista большинство приложений панели управления являются элементами оболочки и не могут быть открыты с помощью этой функции. Чтобы открыть эти приложения панели управления, передайте каноническое имя в control.exe. Пример:</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="shell-ejectpc.md"><strong>ежектпк</strong></a> | Извлекает компьютер из стыковочного узла. Это то же самое, что и при нажатии кнопки " <strong>Пуск</strong> " и выборе пункта " <strong>извлечь компьютер</strong>", если компьютер поддерживает эту команду.<br /> | 
| <a href="shell-explore.md"><strong>Анализ</strong></a> | открывает указанную папку в окне проводника Windows.<br /> | 
| <a href="shell-explorerpolicy.md"><strong>експлорерполици</strong></a> | Возвращает значение для указанной политики Internet Explorer.<br /> | 
| <a href="shell-filerun.md"><strong>филерун</strong></a> | Отображает диалоговое окно <strong>запуска</strong> для пользователя. Этот метод оказывает тот же результат, что и при щелчке меню <strong>Пуск</strong> и выборе <strong>Run</strong>.<br /> | 
| <a href="shell-findcomputer.md"><strong>финдкомпутер</strong></a> | Отображает диалоговое окно <strong>Результаты поиска: компьютеры</strong> . В диалоговом окне отображается результат поиска указанного компьютера.<br /> | 
| <a href="shell-findfiles.md"><strong>финдфилес</strong></a> | Отображает диалоговое окно <strong>Поиск: все файлы</strong> . это то же самое, что и при нажатии кнопки " <strong>пуск</strong> ", а затем выборе <strong>поиска</strong> (или его эквивалента в системах, предшествующих Windows XP.<br /> | 
| <a href="/windows/desktop/shell/shell-findprinter"><strong>финдпринтер</strong></a> | Отображает диалоговое окно <strong>Поиск принтера</strong> .<br /> | 
| <a href="/windows/desktop/shell/shell-getsetting"><strong>GetSetting</strong></a> | Извлекает параметр глобальной оболочки.<br /> | 
| <a href="/windows/desktop/shell/shell-getsysteminformation"><strong>жетсистеминформатион</strong></a> | Возвращает сведения о системе.<br /> | 
| <a href="shell-help.md"><strong>Справка</strong></a> | отображает Windows центре справки и поддержки. Этот метод действует так же, как и при щелчке меню <strong>Пуск</strong> и выбрав пункт <strong>Справка и поддержка</strong>.<br /> | 
| <a href="/windows/desktop/shell/shell-isrestricted"><strong>Ограниченный доступ</strong></a> | Извлекает из реестра параметр ограничений группы.<br /> | 
| <a href="/windows/desktop/shell/shell-isservicerunning"><strong>иссервицеруннинг</strong></a> | Возвращает значение, указывающее, запущена ли определенная служба.<br /> | 
| <a href="shell-minimizeall.md"><strong>минимизеалл</strong></a> | Свертывает все окна на рабочем столе. этот метод имеет тот же результат, что и щелчок правой кнопкой мыши панели задач и выбора параметра <strong>свернуть все Windows</strong> в старых системах или нажатия значка " <strong>показывать рабочий стол</strong> " в области быстрого запуска на панели задач в Windows 2000 или Windows XP.<br /> | 
| <a href="shell-namespace.md"><strong>Имен</strong></a> | Создает и возвращает объект <a href="folder.md"><strong>Folder</strong></a> для указанной папки.<br /> | 
| <a href="shell-open.md"><strong>Открыть</strong></a> | Открывает указанную папку.<br /> | 
| <a href="shell-refreshmenu.md"><strong>рефрешмену</strong></a> | Обновляет содержимое меню " <strong>Пуск</strong> ". используется только с системами, предшествующими Windows XP.<br /> | 
| <a href="shell-searchcommand.md"><strong>сеарчкомманд</strong></a> | Отображает панель поиска приложений.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestart"><strong>сервицестарт</strong></a> | Запускает именованную службу.<br /> | 
| <a href="/windows/desktop/shell/shell-servicestop"><strong>сервицестоп</strong></a> | Останавливает именованную службу.<br /> | 
| <a href="shell-settime.md"><strong>SetTime</strong></a> | Отображает диалоговое окно <strong>Свойства даты и времени</strong> . Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра <strong>настроить дату и время</strong>.<br /> | 
| <a href="/windows/desktop/shell/shell-shellexecute"><strong>ShellExecute</strong></a> | Выполняет указанную операцию с указанным файлом.<br /> | 
| <a href="/windows/desktop/shell/shell-showbrowserbar"><strong>шовбровсербар</strong></a> | Отображает панель браузера.<br /> | 
| <a href="shell-shutdownwindows.md"><strong>шутдовнвиндовс</strong></a> | отображает диалоговое окно <strong>завершение работы Windows</strong> . Это то же самое, что и при нажатии кнопки « <strong>Пуск</strong> », и при выборе « <strong>Завершение работы</strong>».<br /> | 
| <a href="shell-suspend.md"><strong>Приостановить</strong></a> | < | 
| <a href="shell-tilehorizontally.md"><strong>тилехоризонталли</strong></a> | Мозаичное отображение всех окон на рабочем столе по горизонтали. этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора <strong>плитки Windows горизонтально</strong>.<br /> | 
| <a href="shell-tilevertically.md"><strong>тилевертикалли</strong></a> | Располагает все окна на рабочем столе по вертикали. этот метод имеет тот же результат, что и щелчок правой кнопкой мыши панели задач и выбор <strong>плитки Windows вертикально</strong>.<br /> | 
| <a href="shell-toggledesktop.md"><strong>тоггледесктоп</strong></a> | Отображает или скрывает Рабочий стол.<br /> | 
| <a href="shell-trayproperties.md"><strong>трайпропертиес</strong></a> | Отображает диалоговое окно <strong>Свойства панели задач и меню "Пуск</strong> ". Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора <strong>свойств</strong>.<br /> | 
| <a href="shell-undominimizeall.md"><strong>ундоминимизеалл</strong></a> | Восстанавливает все настольные компьютеры в том же состоянии, в котором они находились до последней команды <a href="shell-minimizeall.md"><strong>минимизеалл</strong></a> . этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора команды <strong>отменить свернуть все Windows</strong> в старых системах или второй щелчок значка " <strong>свернуть рабочий стол</strong> " в области быстрого запуска на панели задач в Windows 2000 или Windows XP.<br /> | 
| <a href="shell-windows.md"><strong>Windows</strong></a> | Создает и возвращает объект <a href="shellwindows.md"><strong>шеллвиндовс</strong></a> . Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.<br /> | 
| <a href="shell-windowssecurity.md"><strong>виндовссекурити</strong></a> | отображает диалоговое окно <strong>Безопасность Windows</strong> .<br /> | 
| <a href="shell-windowswitcher.md"><strong>виндовсвитчер</strong></a> | Отображает открытые окна в трехмерном стеке, который можно переворачивать.<br /> | 




 

### <a name="properties"></a>Свойства

Объект **оболочки** имеет следующие свойства.



| Свойство                                            | Тип доступа          | Описание                                                                 |
|:----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**Приложение**](shell-application.md)<br/> | Только для чтения<br/> | Содержит объект приложения объекта.<br/>                        |
| [**Parent**](shell-parent.md)<br/>           | Только для чтения<br/> | Возвращает объект, представляющий родительский объект текущего объекта.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
