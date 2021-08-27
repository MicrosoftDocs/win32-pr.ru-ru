---
description: Представляет объект в оболочке.
title: Объект Ишеллдиспатч (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9B429C03-7F80-45db-B8CD-58D19FAD2E61
ms.openlocfilehash: 322b912ad7332b0862309b0ecc1510adb3aa1a10
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475300"
---
# <a name="ishelldispatch-object"></a>Объект Ишеллдиспатч

Представляет объект в оболочке. Предоставляются методы для управления оболочкой и выполнения команд в оболочке. Существуют также методы для получения других объектов, связанных с оболочкой.

> [!Note]  
> **Ишеллдиспатч** реализован и доступен через объект [**Shell**](shell.md) .

 

## <a name="members"></a>Элементы

Объект **ишеллдиспатч** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **ишеллдиспатч** содержит эти методы.




| Метод | Описание | 
|--------|-------------|
| <a href="ishelldispatch-browseforfolder.md"><strong>бровсефорфолдер</strong></a> | Создает диалоговое окно, которое позволяет пользователю выбрать папку, а затем возвращает объект <a href="folder.md"><strong>папки</strong></a> выбранной папки.<br /> | 
| <a href="ishelldispatch-cascadewindows.md"><strong>каскадевиндовс</strong></a> | Каскадное расположение всех окон на рабочем столе. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора <strong>окна каскадом</strong>.<br /> | 
| <a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a> | Запускает указанное приложение панели управления. Если приложение уже открыто, будет активирован запущенный экземпляр. <br /><blockquote><p>[!Note]<br />начиная с Windows Vista большинство приложений панели управления являются элементами оболочки и не могут быть открыты с помощью этой функции. Чтобы открыть эти приложения панели управления, передайте каноническое имя в control.exe. Пример:</p><pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre></blockquote><br /> | 
| <a href="ishelldispatch-ejectpc.md"><strong>ежектпк</strong></a> | Извлекает компьютер из стыковочного узла. Это то же самое, что и при нажатии кнопки " <strong>Пуск</strong> " и выборе пункта " <strong>извлечь компьютер</strong>", если компьютер поддерживает эту команду.<br /> | 
| <a href="ishelldispatch-explore.md"><strong>Анализ</strong></a> | открывает указанную папку в окне проводника Windows.<br /> | 
| <a href="ishelldispatch-filerun.md"><strong>филерун</strong></a> | Отображает диалоговое окно <strong>запуска</strong> для пользователя.<br /> | 
| <a href="ishelldispatch-findcomputer.md"><strong>финдкомпутер</strong></a> | Отображает диалоговое окно <strong>Результаты поиска: компьютеры</strong> . В диалоговом окне отображается результат поиска указанного компьютера.<br /> | 
| <a href="ishelldispatch-findfiles.md"><strong>финдфилес</strong></a> | Отображает диалоговое окно <strong>Поиск: все файлы</strong> . Это то же самое, что и при щелчке в меню <strong>Пуск</strong> , а затем выбрав <strong>Поиск</strong>.<br /> | 
| <a href="ishelldispatch-help.md"><strong>Справка</strong></a> | отображает окно справки и поддержки Windows. Этот метод действует так же, как и при щелчке меню <strong>Пуск</strong> и выбрав пункт <strong>Справка и поддержка</strong>.<br /> | 
| <a href="ishelldispatch-minimizeall.md"><strong>минимизеалл</strong></a> | Свертывает все окна на рабочем столе. этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора пункта <strong>свернуть все Windows</strong> в старых системах или щелчка значка свернуть <strong>рабочий стол</strong> на панели задач.<br /> | 
| <a href="ishelldispatch-namespace.md"><strong>Имен</strong></a> | Создает и возвращает объект <a href="folder.md"><strong>Folder</strong></a> для указанной папки.<br /> | 
| <a href="ishelldispatch-open.md"><strong>Открыть</strong></a> | Открывает указанную папку.<br /> | 
| <a href="ishelldispatch-refreshmenu.md"><strong>рефрешмену</strong></a> | Обновляет содержимое меню " <strong>Пуск</strong> ". используется только с системами, предшествующими Windows XP.<br /> | 
| <a href="ishelldispatch-settime.md"><strong>SetTime</strong></a> | Отображает диалоговое окно <strong>Дата и время</strong> . Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра <strong>настроить дату и время</strong>.<br /> | 
| <a href="ishelldispatch-shutdownwindows.md"><strong>шутдовнвиндовс</strong></a> | отображает диалоговое окно <strong>завершение работы Windows</strong> . Это то же самое, что и при нажатии кнопки « <strong>Пуск</strong> », и при выборе « <strong>Завершение работы</strong>».<br /> | 
| <a href="ishelldispatch-suspend.md"><strong>Приостановить</strong></a> | < | 
| <a href="ishelldispatch-tilehorizontally.md"><strong>тилехоризонталли</strong></a> | Мозаичное отображение всех окон на рабочем столе по горизонтали. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора пункта <strong>Показывать окна с накоплением</strong>.<br /> | 
| <a href="ishelldispatch-tilevertically.md"><strong>тилевертикалли</strong></a> | Располагает все окна на рабочем столе по вертикали. Этот метод оказывает тот же результат, что и щелчок правой кнопкой мыши панели задач и выбора параметра <strong>Показывать окна рядом</strong>.<br /> | 
| <a href="ishelldispatch-trayproperties.md"><strong>трайпропертиес</strong></a> | Отображает диалоговое окно <strong>Свойства панели задач и меню "Пуск</strong> ". Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора <strong>свойств</strong>.<br /> | 
| <a href="ishelldispatch-undominimizeall.md"><strong>ундоминимизеалл</strong></a> | Восстанавливает все настольные окна до состояния, в котором они были до последней команды <a href="shell-minimizeall.md"><strong>минимизеалл</strong></a> . этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора команды <strong>отменить свернуть все Windows</strong> (в старых системах) или второй щелчок значка " <strong>свернуть рабочий стол</strong> " на панели задач.<br /> | 
| <a href="ishelldispatch-windows.md"><strong>Windows</strong></a> | Создает и возвращает объект <a href="shellwindows.md"><strong>шеллвиндовс</strong></a> . Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.<br /> | 




 

### <a name="properties"></a>Свойства

Объект **ишеллдиспатч** имеет следующие свойства.



| Свойство                                                     | Тип доступа          | Описание                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Приложение**](ishelldispatch-application.md)<br/> | Только для чтения<br/> | Содержит объект, представляющий приложение.<br/>                    |
| [**Parent**](ishelldispatch-parent.md)<br/>           | Только для чтения<br/> | Извлекает объект, представляющий родителя текущего объекта.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Объект оболочки**](shell.md)
</dt> </dl>

 

 
