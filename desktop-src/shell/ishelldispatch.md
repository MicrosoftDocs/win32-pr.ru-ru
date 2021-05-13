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
ms.openlocfilehash: 02fbead4b2d40a91ec6dab70f536d1ea3241ee84
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840895"
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
<td style="text-align: left;"><a href="ishelldispatch-browseforfolder.md"><strong>бровсефорфолдер</strong></a></td>
<td style="text-align: left;">Создает диалоговое окно, которое позволяет пользователю выбрать папку, а затем возвращает объект <a href="folder.md"><strong>папки</strong></a> выбранной папки.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-cascadewindows.md"><strong>каскадевиндовс</strong></a></td>
<td style="text-align: left;">Каскадное расположение всех окон на рабочем столе. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора <strong>окна каскадом</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-controlpanelitem.md"><strong>ControlPanelItem</strong></a></td>
<td style="text-align: left;">Запускает указанное приложение панели управления. Если приложение уже открыто, будет активирован запущенный экземпляр. <br/>
<blockquote>
<p>[!Note]<br />
Начиная с Windows Vista, большинство приложений панели управления являются элементами оболочки и не могут быть открыты с помощью этой функции. Чтобы открыть эти приложения панели управления, передайте каноническое имя в control.exe. Пример:</p>
<pre class="syntax" data-space="preserve"><code>control.exe /name Microsoft.Personalization</code></pre>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-ejectpc.md"><strong>ежектпк</strong></a></td>
<td style="text-align: left;">Извлекает компьютер из стыковочного узла. Это то же самое, что и при нажатии кнопки " <strong>Пуск</strong> " и выборе пункта " <strong>извлечь компьютер</strong>", если компьютер поддерживает эту команду.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-explore.md"><strong>Просматриваем</strong></a></td>
<td style="text-align: left;">Открывает указанную папку в окне проводника Windows.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-filerun.md"><strong>филерун</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>запуска</strong> для пользователя.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-findcomputer.md"><strong>финдкомпутер</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Результаты поиска: компьютеры</strong> . В диалоговом окне отображается результат поиска указанного компьютера.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-findfiles.md"><strong>финдфилес</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Поиск: все файлы</strong> . Это то же самое, что и при щелчке в меню <strong>Пуск</strong> , а затем выбрав <strong>Поиск</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-help.md"><strong>Справка</strong></a></td>
<td style="text-align: left;">Отображает окно справки и поддержки Windows. Этот метод действует так же, как и при щелчке меню <strong>Пуск</strong> и выбрав пункт <strong>Справка и поддержка</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-minimizeall.md"><strong>минимизеалл</strong></a></td>
<td style="text-align: left;">Свертывает все окна на рабочем столе. Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора пункта <strong>Свернуть все окна</strong> в старых системах или нажатия значка " <strong>Свернуть Рабочий стол</strong> " на панели задач.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-namespace.md"><strong>Имен</strong></a></td>
<td style="text-align: left;">Создает и возвращает объект <a href="folder.md"><strong>Folder</strong></a> для указанной папки.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-open.md"><strong>Открыт</strong></a></td>
<td style="text-align: left;">Открывает указанную папку.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-refreshmenu.md"><strong>рефрешмену</strong></a></td>
<td style="text-align: left;">Обновляет содержимое меню " <strong>Пуск</strong> ". Используется только с системами, предшествующими Windows XP.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-settime.md"><strong>SetTime</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Дата и время</strong> . Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра <strong>настроить дату и время</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-shutdownwindows.md"><strong>шутдовнвиндовс</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Завершение работы Windows</strong> . Это то же самое, что и при нажатии кнопки « <strong>Пуск</strong> », и при выборе « <strong>Завершение работы</strong>».<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-suspend.md"><strong>Анализируем</strong></a></td>
<td style="text-align: left;"></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-tilehorizontally.md"><strong>тилехоризонталли</strong></a></td>
<td style="text-align: left;">Мозаичное отображение всех окон на рабочем столе по горизонтали. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора пункта <strong>Показывать окна с накоплением</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-tilevertically.md"><strong>тилевертикалли</strong></a></td>
<td style="text-align: left;">Располагает все окна на рабочем столе по вертикали. Этот метод оказывает тот же результат, что и щелчок правой кнопкой мыши панели задач и выбора параметра <strong>Показывать окна рядом</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-trayproperties.md"><strong>трайпропертиес</strong></a></td>
<td style="text-align: left;">Отображает диалоговое окно <strong>Свойства панели задач и меню "Пуск</strong> ". Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора <strong>свойств</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="ishelldispatch-undominimizeall.md"><strong>ундоминимизеалл</strong></a></td>
<td style="text-align: left;">Восстанавливает все настольные окна до состояния, в котором они были до последней команды <a href="shell-minimizeall.md"><strong>минимизеалл</strong></a> . Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора команды <strong>отменить свернуть все окна</strong> (в старых системах) или второй щелчок значка Свернуть <strong>Рабочий стол</strong> на панели задач.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="ishelldispatch-windows.md"><strong>Windows</strong></a></td>
<td style="text-align: left;">Создает и возвращает объект <a href="shellwindows.md"><strong>шеллвиндовс</strong></a> . Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Свойства

Объект **ишеллдиспатч** имеет следующие свойства.



| Свойство                                                     | Тип доступа          | Описание                                                                      |
|:-------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------|
| [**Приклад**](ishelldispatch-application.md)<br/> | Только для чтения<br/> | Содержит объект, представляющий приложение.<br/>                    |
| [**Parent**](ishelldispatch-parent.md)<br/>           | Только для чтения<br/> | Извлекает объект, представляющий родителя текущего объекта.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Объект оболочки**](shell.md)
</dt> </dl>

 

 
