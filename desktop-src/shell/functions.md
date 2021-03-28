---
description: В этом разделе описываются функции оболочки Windows.
title: Функции оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f4d6c0c4-8db3-4721-80f5-2a73bb57cd99
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c8e31bdaac8ec581504326c17d5d37012dd019d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997726"
---
# <a name="shell-functions"></a>Функции оболочки

\[Эта функция больше не реализована.\]

В этом разделе описываются функции оболочки Windows.

## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="intsafe-h-functions-bumper.md">Функции интсафе. h</a><br/></td>

</tr>
<tr class="even">
<td><a href="library-functions-bumper.md">Функции библиотеки</a><br/></td>

</tr>
<tr class="odd">
<td><a href="path-functions.md">Функции пути</a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>ассоккреатефорклассес</strong></a><br/></td>
<td>Извлекает объект, реализующий интерфейс <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>икуеряссоЦиатионс</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-assocgetdetailsofpropkey"><strong>ассокжетдетаилсофпропкэй</strong></a><br/></td>
<td>Получает значение для заданного ключа свойства, используя сведения о сопоставлении файлов, предоставляемые <a href="nse-works.md">расширениями пространства имен</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2"><strong>CDefFolderMenu_Create2</strong></a><br/></td>
<td>Создает контекстное меню для выбранной группы объектов папки с файлами.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/ntquery/nf-ntquery-cishutdown"><strong>Цишутдовн</strong></a><br/></td>
<td>Завершает работу индексатора содержимого и закрывает все открытые каталоги. <br/>
<blockquote>
[!Note]<br />
Эта функция не поддерживается в Windows 8.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-commandlinetoargvw"><strong>коммандлинетоаргвв</strong></a><br/></td>
<td>Анализирует строку командной строки в Юникоде и возвращает массив указателей на аргументы командной строки, а также количество таких аргументов, аналогично стандартным значениям <em>argv</em> и <em>argc</em> времени выполнения C.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>APPLET_PROC</strong></a><br/></td>
<td>Выступает в качестве точки входа для приложения панели управления. Это функция обратного вызова, определяемая библиотекой.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createappcontainerprofile"><strong>креатеаппконтаинерпрофиле</strong></a><br/></td>
<td>Создает профиль "на пользователя" для приложений Магазина Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>креатинвиронментблокк</strong></a><br/></td>
<td>Извлекает переменные среды для указанного пользователя. Этот блок затем можно передать в функцию <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera"><strong>параметр CreateProcessAsUser</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="createmrulist.md"><strong>креатемрулиств</strong></a><br/></td>
<td>Создает новый список последних использованных (MRU) списков.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-createprofile"><strong>креатепрофиле</strong></a><br/></td>
<td>Создает новый профиль пользователя.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-defscreensaverproc"><strong>дефскринсаверпрок</strong></a><br/></td>
<td>Обеспечивает обработку по умолчанию для всех сообщений, которые не обрабатывается приложением-заставкой.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-defsubclassproc"><strong>дефсубкласспрок</strong></a><br/></td>
<td>Вызывает следующий обработчик в цепочке подклассов окна. Последний обработчик в цепочке подкласс вызывает исходную процедуру окна для окна.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteappcontainerprofile"><strong>делетеаппконтаинерпрофиле</strong></a><br/></td>
<td>Удаляет указанный профиль для каждого пользователя и каждого приложения.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deleteprofilea"><strong>делетепрофиле</strong></a><br/></td>
<td>Удаляет профиль пользователя и все параметры, связанные с пользователем, с указанного компьютера. Вызывающий объект должен иметь права администратора для удаления профиля пользователя.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock"><strong>дестройенвиронментблокк</strong></a><br/></td>
<td>Освобождает переменные среды, созданные функцией <a href="/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock"><strong>креатинвиронментблокк</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-deriveappcontainersidfromappcontainername"><strong>деривеаппконтаинерсидфромаппконтаинернаме</strong></a><br/></td>
<td>Возвращает идентификатор безопасности указанного профиля.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/userenv/nf-userenv-deriverestrictedappcontainersidfromappcontainersidandrestrictedname"><strong>дериверестриктедаппконтаинерсидфромаппконтаинерсидандрестриктеднаме</strong></a><br/></td>
<td>Дериверестриктедаппконтаинерсидфромаппконтаинерсидандрестриктеднаме зарезервирован для использования в будущем.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><em>дллжетверсионпрок</em></a><br/></td>
<td>Реализован многими библиотеками Windows Shell, чтобы позволить приложениям получать сведения о версии, относящиеся к библиотеке DLL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles"><strong>DragAcceptFiles</strong></a><br/></td>
<td>Регистрирует, принимает ли окно удаленные файлы.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragfinish"><strong>драгфиниш</strong></a><br/></td>
<td>Освобождает память, которую система выделила для использования при передаче имен файлов в приложение.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea"><strong>драгкуерифиле</strong></a><br/></td>
<td>Извлекает имена удаленных файлов, являющиеся результатом успешной операции перетаскивания.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint"><strong>драгкуерипоинт</strong></a><br/></td>
<td>Получает расположение указателя мыши во время удаления файла во время операции перетаскивания.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-duplicateicon"><strong>дупликатеикон</strong></a><br/></td>
<td>Создает дубликат указанного значка.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera"><strong>експанденвиронментстрингсфорусер</strong></a><br/></td>
<td>Развертывает исходную строку с помощью блока среды, установленного для указанного пользователя.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extractassociatedicona"><strong>екстрактассоЦиатедикон</strong></a><br/></td>
<td>Возвращает маркер для значка, хранящегося в виде ресурса в файле, или значок, хранящийся в связанном с файлом исполняемом файле.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticona"><strong>екстрактикон</strong></a><br/></td>
<td>Получает маркер для значка из указанного исполняемого файла, библиотеки DLL или файла значка. <br/> Чтобы получить массив дескрипторов для крупных или мелких значков, используйте функцию <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>екстрактиконекс</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>екстрактиконекс</strong></a><br/></td>
<td>Функция <a href="/windows/desktop/api/shellapi/nf-shellapi-extracticonexa"><strong>екстрактиконекс</strong></a> создает массив дескрипторов для крупных или мелких значков, извлеченных из указанного исполняемого файла, библиотеки DLL или файла значка.<br/></td>
</tr>
<tr class="odd">
<td><a href="fileiconinit.md"><strong>филеиконинит</strong></a><br/></td>
<td>Инициализирует или повторно инициализирует список системных образов.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-findexecutablea"><strong>финдексекутабле</strong></a><br/></td>
<td>Извлекает имя и обработчик для исполняемого файла (exe), связанного с конкретным файлом документа.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/syncmgr/nf-syncmgr-freeconfirmconflictitem"><strong>фриконфирмконфликтитем</strong></a><br/></td>
<td>Освобождает ресурсы, выделенные для структуры <a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarray"><strong>фриидлистаррай</strong></a><br/></td>
<td>Освобождает память, используемую указателем, на массив списка идентификаторов элементов (ПИДЛ).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarraychild"><strong>фриидлистаррайчилд</strong></a><br/></td>
<td>Освобождает пространство памяти для массива указателей на идентификаторы дочерних элементов. Это освобождает как PITEMID_CHILDs в массиве, так и сам массив.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeidlistarrayfull"><strong>фриидлистаррайфулл</strong></a><br/></td>
<td>Освобождает пространство памяти для массива ПИДЛ. Это освобождает как PIDLIST_ABSOLUTEs в массиве, так и сам массив.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-freeknownfolderdefinitionfields"><strong>фрикновнфолдердефинитионфиелдс</strong></a><br/></td>
<td>Освобождает выделенные поля в результате <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getfolderdefinition"><strong>икновнфолдер:: жетфолдердефинитион</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="freemrulist.md"><strong>фримрулист</strong></a><br/></td>
<td>Освобождает маркер, связанный с списком MRU, и записывает кэшированные данные в реестр.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya"><strong>жеталлусерспрофиледиректори</strong></a><br/></td>
<td>Возвращает путь к корню каталога, который содержит данные программы, совместно используемые всеми пользователями.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerfolderpath"><strong>жетаппконтаинерфолдерпас</strong></a><br/></td>
<td>Возвращает путь к папке локальных данных приложения для указанного контейнера приложения.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getappcontainerregistrylocation"><strong>жетаппконтаинеррегистрилокатион</strong></a><br/></td>
<td>Возвращает расположение хранилища реестра, связанного с контейнером приложения.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/jj152005(v=vs.85)"><strong>жетконтрактделегатевиндов</strong></a><br/></td>
<td>Извлекает окно, которое было задано как делегат для основного основного окна приложения, для привязки окна делегата к контрактам приложения. Используйте эту функцию, если разработчик пишет приложение Магазина Windows в машинном коде C++.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid"><strong>жеткуррентпроцессексплиЦитаппусермоделид</strong></a><br/></td>
<td>Получает определяемый приложением явный идентификатор модели пользователя приложения (AppUserModelID) для текущего процесса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya"><strong>жетдефаултусерпрофиледиректори</strong></a><br/></td>
<td>Возвращает путь к корню профиля пользователя по умолчанию.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiforshelluicomponent"><strong>жетдпифоршеллуикомпонент</strong></a><br/></td>
<td>Получает точки на дюйм (DPI), занятые <a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a> на основе текущего коэффициента масштабирования и <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness"><strong>PROCESS_DPI_AWARENESS</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid"><strong>жетменуконтексселпид</strong></a><br/></td>
<td>Извлекает идентификатор контекста справки, связанный с указанным меню.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya"><strong>жетпрофилесдиректори</strong></a><br/></td>
<td>Возвращает путь к корневому каталогу, в котором хранятся профили пользователей.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getprofiletype"><strong>жетпрофилетипе</strong></a><br/></td>
<td>Возвращает тип профиля, загруженного для текущего пользователя.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>жетскалефакторфордевице</strong></a><br/></td>
<td>Возвращает предпочтительный коэффициент масштабирования для устройства вывода.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorformonitor"><strong>жетскалефакторформонитор</strong></a><br/></td>
<td>Возвращает коэффициент масштабирования конкретного монитора. Эта функция заменяет <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getscalefactorfordevice"><strong>жетскалефакторфордевице</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya"><strong>жетусерпрофиледиректори</strong></a><br/></td>
<td>Возвращает путь к корневому каталогу указанного профиля пользователя.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid"><strong>жетвиндовконтексселпид</strong></a><br/></td>
<td>Возвращает идентификатор контекста справки (при наличии), связанный с указанным окном.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-getwindowsubclass"><strong>жетвиндовсубкласс</strong></a><br/></td>
<td>Извлекает ссылочные данные для указанного обратного вызова подкласса окна.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-idlistcontainerisconsistent"><strong>идлистконтаинерисконсистент</strong></a><br/></td>
<td>Проверяет, является ли структура контейнера IDList допустимой.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilappendid"><strong>илаппендид</strong></a><br/></td>
<td>Добавляет структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>шитемид</strong></a> в начало структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclone"><strong>илклоне</strong></a><br/></td>
<td>Создает точную копию структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonechild"><strong>илклонечилд</strong></a><br/></td>
<td>Создает клон дочерней структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefirst"><strong>илклонефирст</strong></a><br/></td>
<td>Создает точную копию первой структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>шитемид</strong></a> в структуре <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilclonefull"><strong>илклонефулл</strong></a><br/></td>
<td>Создает точную копию полной или абсолютной структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcombine"><strong>илкомбине</strong></a><br/></td>
<td>Объединяет две структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilcreatefrompath"><strong>илкреатефромпас</strong></a><br/></td>
<td>Возвращает структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> , связанную с указанным путем к файлу.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindchild"><strong>илфиндчилд</strong></a><br/></td>
<td>Определяет, является ли указанная структура <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> дочерней по отношению к другой структуре <strong>итемидлист</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfindlastid"><strong>илфиндластид</strong></a><br/></td>
<td>Возвращает указатель на последнюю структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>шитемид</strong></a> в структуре <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree"><strong>илфри</strong></a><br/></td>
<td>Освобождает структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> , выделенную оболочкой.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetnext"><strong>илжетнекст</strong></a><br/></td>
<td>Извлекает следующую структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>шитемид</strong></a> в структуре <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilgetsize"><strong>илжетсизе</strong></a><br/></td>
<td>Возвращает размер структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> в байтах.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisaligned"><strong>илисалигнед</strong></a><br/></td>
<td>Проверяет, соответствует ли константа <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> границе указателя, которая представляет собой <strong>DWORD</strong> в 32-разрядных архитектурах и значение <strong>QWORD</strong> на 64-разрядной архитектуре.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilischild"><strong>илисчилд</strong></a><br/></td>
<td>Проверяет, является ли ПИДЛ дочерним ПИДЛ, который представляет собой ПИДЛ с ровно одним <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>шитемид</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisempty"><strong>илисемпти</strong></a><br/></td>
<td>Проверяет, пуста ли структура <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisequal"><strong>илисекуал</strong></a><br/></td>
<td>Проверяет, равны ли две структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> в двоичном сравнении.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilisparent"><strong>илиспарент</strong></a><br/></td>
<td>Проверяет, является ли структура <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> родительской для другой структуры <strong>итемидлист</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilnext"><strong>Илнекст (PCUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Извлекает следующую структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>шитемид</strong></a> в структуре <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776455(v=vs.85)"><strong>Илнекст (PUIDLIST_RELATIVE)</strong></a><br/></td>
<td>Извлекает следующую структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>шитемид</strong></a> в структуре <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilremovelastid"><strong>илремовеластид</strong></a><br/></td>
<td>Удаляет последнюю структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>шитемид</strong></a> из структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilsavetostream"><strong>илсаветостреам</strong></a><br/></td>
<td>Сохраняет структуру <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> в поток.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ilskip"><strong>Илскип (PCUIDLIST_RELATIVE, UINT)</strong></a><br/></td>
<td>Пропускает заданное число байтов в константной, несогласованной структуре <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776459(v=vs.85)"><strong>Илскип (PUIDLIST_RELATIVE, UINT)</strong></a><br/></td>
<td>Пропускает заданное число байтов в несогласованной структуре <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-inetisoffline"><strong>инетисоффлине</strong></a><br/></td>
<td>Определяет, подключена ли система к Интернету.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol"><strong>инитнетворкаддрессконтрол</strong></a><br/></td>
<td>Инициализирует класс окна управления сетевыми адресами.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a><br/></td>
<td>Загружает профиль указанного пользователя. Профиль может быть <a href="local-user-profiles.md">локальным профилем пользователя</a> или <a href="roaming-user-profiles.md">перемещаемым профилем пользователя</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>мимеассоЦиатиондиалог</strong></a><br/></td>
<td>Выполняет диалоговое окно "незарегистрированный тип содержимого MIME".<br/>
<blockquote>
[!Note]<br />
Windows XP с пакетом обновления 2 (SP2) или более поздней версии: Эта функция больше не поддерживается.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathmakeuniquename"><strong>пасмакеуникуенаме</strong></a><br/></td>
<td>Создает уникальное имя пути из шаблона.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-pathyetanothermakeuniquename"><strong>пасетаносермакеуникуенаме</strong></a><br/></td>
<td>Создает уникальное имя файла на основе существующего имени файла.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>регистераппстатечанженотификатион</strong></a><br/></td>
<td>Позволяет приложению зарегистрировать функцию обратного вызова, с помощью которой можно получить уведомления о том, что ее библиотека переходит в приостановленное состояние или выходит из нее. Приложение может использовать эти сведения для выполнения необходимых операций, таких как сохранение состояния, которое должно выполняться в этот момент.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-registerdialogclasses"><strong>регистердиалогклассес</strong></a><br/></td>
<td>Регистрирует все нестандартные классы окон, необходимые для диалогового окна настройки экранной заставки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>регистерскалечанжеевент</strong></a><br/></td>
<td>Регистрируется для события, которое активируется, когда масштаб может измениться. Эта функция заменяет <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>регистерскалечанженотификатионс</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangenotifications"><strong>регистерскалечанженотификатионс</strong></a><br/></td>
<td>Регистрирует окно для получения обратных вызовов при изменении сведений о масштабировании.<br/>
<blockquote>
[!Note]<br />
Эта функция не поддерживается для Windows 8.1. Вместо этого используйте <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>регистерскалечанжеевент</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass"><strong>ремовевиндовсубкласс</strong></a><br/></td>
<td>Удаляет обратный вызов подкласса из окна.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>ревокескалечанженотификатионс</strong></a><br/></td>
<td>Отменяет регистрацию окна, предотвращая получение обратных вызовов при масштабировании изменений информации.<br/>
<blockquote>
[!Note]<br />
Эта функция не поддерживается для Windows 8.1. Вместо этого используйте <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>унрегистерскалечанжеевент</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverconfiguredialog"><strong>скринсаверконфигуредиалог</strong></a><br/></td>
<td>Получает сообщения, отправленные в диалоговое окно настройки экранной заставки. Эта функция должна определяться экранной заставкой, которая позволяет настраивать пользователя.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Scrnsave/nf-scrnsave-screensaverproc"><strong>скринсаверпрок</strong></a><br/></td>
<td>Получает сообщения, отправленные в указанное окно экранной заставки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcontractdelegatewindow"><strong>сетконтрактделегатевиндов</strong></a><br/></td>
<td>Связывает окно приложения, отличное от основного окна переднего плана, с контрактами приложения. Используйте эту функцию, если разработчик пишет приложение Магазина Windows в машинном коде C++.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid"><strong>сеткуррентпроцессексплиЦитаппусермоделид</strong></a><br/></td>
<td>Указывает уникальный определяемый приложением AppUserModelID, который определяет текущий процесс на панели задач. Этот идентификатор позволяет приложению группировать связанные процессы и окна на одной кнопке панели задач.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid"><strong>сетменуконтексселпид</strong></a><br/></td>
<td>Связывает идентификатор контекста справки с меню.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid"><strong>сетвиндовконтексселпид</strong></a><br/></td>
<td>Связывает идентификатор контекста справки с указанным окном.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass"><strong>сетвиндовсубкласс</strong></a><br/></td>
<td>Устанавливает или обновляет обратный вызов подкласса окна.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>шаддторецентдокс</strong></a><br/></td>
<td>Уведомляет систему о том, что к элементу осуществлялся доступ, в целях отслеживания элементов, которые использовались в последнее время и чаще всего. Эта функция также может использоваться для очистки всех данных об использовании.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage"><strong>шаппбармессаже</strong></a><br/></td>
<td>Отправляет в систему сообщение панель приложений.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlers"><strong>шассоценумхандлерс</strong></a><br/></td>
<td>Возвращает объект перечисления для указанного набора обработчиков расширений имен файлов.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shassocenumhandlersforprotocolbyapplication"><strong>шассоценумхандлерсфорпротоколбяппликатион</strong></a><br/></td>
<td>Возвращает интерфейс перечисления, предоставляющий доступ к обработчикам, связанным с данным протоколом.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>шбиндтофолдеридлистпарент</strong></a><br/></td>
<td>Учитывая элемент пространства имен оболочки, указанный в форме папки, и список идентификаторов элементов относительно этой папки, эта функция привязывается к родительскому элементу пространства имен и при необходимости возвращает указатель на последний компонент списка идентификаторов элементов.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparentex"><strong>шбиндтофолдеридлистпарентекс</strong></a><br/></td>
<td>Расширяет функцию <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtofolderidlistparent"><strong>шбиндтофолдеридлистпарент</strong></a> , позволяя вызывающей стороне указать контекст привязки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoobject"><strong>шбиндтубжект</strong></a><br/></td>
<td>Извлекает и привязывает к указанному объекту с помощью метода Namespace пространства имен <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>ишеллфолдер:: биндтубжект</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent"><strong>шбиндтопарент</strong></a><br/></td>
<td>Принимает указатель на полный список идентификаторов элементов (ПИДЛ) и возвращает указанный указатель интерфейса для родительского объекта.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>шбровсефорфолдер</strong></a><br/></td>
<td>Отображает диалоговое окно, позволяющее пользователю выбрать папку оболочки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_lock"><strong>SHChangeNotification_Lock</strong></a><br/></td>
<td>Блокирует общую память, связанную с событием уведомления об изменении оболочки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotification_unlock"><strong>SHChangeNotification_Unlock</strong></a><br/></td>
<td>Разблокирует общую память для уведомления об изменении.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>шчанженотифи</strong></a><br/></td>
<td>Уведомляет систему о событии, которое было выполнено приложением. Приложение должно использовать эту функцию, если она выполняет действие, которое может повлиять на работу оболочки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyderegister"><strong>шчанженотифидерегистер</strong></a><br/></td>
<td>Отменяет регистрацию процесса окна клиента из получения сообщений <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify"><strong>шчанженотифи</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>шчанженотифирегистер</strong></a><br/></td>
<td>Регистрирует окно для получения уведомлений из файловой системы или оболочки, если файловая система поддерживает уведомления.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>шчанженотифирегистерсреад</strong></a><br/></td>
<td>Включает асинхронную регистрацию и отмену регистрации потока.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateassociationregistration"><strong>шкреатеассоЦиатионрегистратион</strong></a><br/></td>
<td>Создает объект <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>иаппликатионассоЦиатионрегистратион</strong></a> , основанный на акции реализации интерфейса, предоставляемого Windows.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject"><strong>шкреатедатаобжект</strong></a><br/></td>
<td>Создает объект данных в родительской папке.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>шкреатедефаултконтекстмену</strong></a><br/></td>
<td>Создает объект, представляющий реализацию контекстного меню по умолчанию для оболочки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreatedefaultextracticon"><strong>шкреатедефаултекстрактикон</strong></a><br/></td>
<td>Создает стандартный средство извлечения значков, параметры которого по умолчанию можно настроить с помощью интерфейса <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>идефаултекстрактиконинит</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shcreatedefaultpropertiesop"><strong>шкреатедефаултпропертиесоп</strong></a><br/></td>
<td>Создает операцию с файлом, которая задает свойства по умолчанию для элемента оболочки, который еще не был задан.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>шкреатеитемфромидлист</strong></a><br/></td>
<td>Создает и инициализирует объект элемента оболочки из ПИДЛ. Полученный объект элемента оболочки поддерживает интерфейс <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>интерфейса IShellItem</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>шкреатеитемфромпарсингнаме</strong></a><br/></td>
<td>Создает и инициализирует объект элемента оболочки из имени синтаксического анализа.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromrelativename"><strong>шкреатеитемфромрелативенаме</strong></a><br/></td>
<td>Создает и инициализирует объект элемента оболочки на основе относительного имени синтаксического анализа.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateiteminknownfolder"><strong>шкреатеитеминкновнфолдер</strong></a><br/></td>
<td>Создает объект элемента оболочки для одного файла, который существует в известной папке.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>шкреатеитемвиспарент</strong></a><br/></td>
<td>Создание элемента оболочки с заданной родительской папкой и ИДЕНТИФИКАТОРом дочернего элемента.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>шкреатешеллфолдервиев</strong></a><br/></td>
<td>Создает новый экземпляр объекта представления папки оболочки по умолчанию (Дефвиев).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>шкреатешеллфолдервиевекс</strong></a><br/></td>
<td>Создает новый экземпляр объекта представления папки оболочки по умолчанию. Рекомендуется использовать <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>шкреатешеллфолдервиев</strong></a> , а не эту функцию.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellitem"><strong>шкреатешеллитем</strong></a><br/></td>
<td>Создает объект <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>интерфейса IShellItem</strong></a> . <br/>
<blockquote>
[!Note]<br />
Вместо этой функции рекомендуется использовать <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemwithparent"><strong>шкреатеитемвиспарент</strong></a> или <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist"><strong>шкреатеитемфромидлист</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray"><strong>шкреатешеллитемаррай</strong></a><br/></td>
<td>Создает объект массива элементов оболочки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject"><strong>шкреатешеллитемаррайфромдатаобжект</strong></a><br/></td>
<td>Создает объект массива элементов оболочки из объекта данных. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists"><strong>шкреатешеллитемаррайфромидлистс</strong></a><br/></td>
<td>Создает объект массива элементов оболочки из списка структур <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem"><strong>шкреатешеллитемаррайфромшеллитем</strong></a><br/></td>
<td>Создает массив из одного элемента в одной оболочке.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdefextracticona"><strong>шдефекстрактикон</strong></a><br/></td>
<td>Предоставляет обработчик по умолчанию для извлечения значка из файла.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop"><strong>шдодрагдроп</strong></a><br/></td>
<td>Выполняет операцию перетаскивания. Поддерживает создание источника перетаскивания по запросу, а также перетаскивание изображений.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a><br/></td>
<td>Отправляет сообщение в область состояния панели задач.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a><br/></td>
<td>Возвращает экранные координаты ограничивающего прямоугольника значка уведомления.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellabouta"><strong>шеллабаут</strong></a><br/></td>
<td>Отображает диалоговое окно <strong>шеллабаут</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="shellddeinit.md"><strong>шеллддеинит</strong></a><br/></td>
<td>Регистрирует службы оболочки платформа динамических данных Exchange (DDE) в текущем процессе, уведомляя систему о том, что текущему процессу требуется разместить объекты DDE.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a><br/></td>
<td>Выполняет операцию с указанным файлом.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a><br/></td>
<td>Выполняет операцию с указанным файлом.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shemptyrecyclebina"><strong>шемптирециклебин</strong></a><br/></td>
<td>Очищает корзину на указанном диске.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shenumerateunreadmailaccountsa"><strong>шенумератеунреадмаилаккаунтс</strong></a><br/></td>
<td>Перечисление учетных записей пользователей, имеющих непрочтенный адрес электронной почты.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shevaluatesystemcommandtemplate"><strong>шевалуатесистемкоммандтемплате</strong></a><br/></td>
<td>Обеспечивает строгую проверку параметров, используемых при вызове функции <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> или <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea"><strong>ShellExecute</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>шфилеоператион</strong></a><br/></td>
<td>Копирует, перемещает, переименовывает или удаляет объект файловой системы. Эта функция была заменена в Windows Vista <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>интерфейс IFileOperation</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shfreenamemappings"><strong>шфринамемаппингс</strong></a><br/></td>
<td>Освобождает объект сопоставления имен файлов, полученный функцией <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>шфилеоператион</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>шжетдатафромидлист</strong></a><br/></td>
<td>Извлекает данные расширенных свойств из списка относительного идентификатора.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder"><strong>шжетдесктопфолдер</strong></a><br/></td>
<td>Извлекает интерфейс <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>ишеллфолдер</strong></a> для папки Desktop, которая является корнем пространства имен оболочки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdiskfreespaceexa"><strong>шжетдискфриспацеекс</strong></a><br/></td>
<td>Извлекает сведения о дисковом пространстве для тома диска.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetdrivemedia"><strong>шжетдривемедиа</strong></a><br/></td>
<td>Возвращает тип носителя на указанном диске.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa"><strong>шжетфилеинфо</strong></a><br/></td>
<td>Извлекает сведения об объекте в файловой системе, например файл, папку, каталог или корень диска.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/mt757093(v=vs.85)"><strong>шжетфолдерпасекс</strong></a><br/></td>
<td>Получает полный путь к известной папке, идентифицируемой <a href="knownfolderid.md"><strong>кновнфолдерид</strong></a>папки. Это расширяет <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>шжеткновнфолдерпас</strong></a> , позволяя задавать начальный размер строкового буфера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgeticonoverlayindexa"><strong>шжетиконоверлайиндекс</strong></a><br/></td>
<td>Возвращает индекс значка оверлея в списке образов системы.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject"><strong>шжетидлистфромобжект</strong></a><br/></td>
<td>Возвращает ПИДЛ объекта.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetimagelist"><strong>шжетимажелист</strong></a><br/></td>
<td>Извлекает список изображений.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer"><strong>шжетинстанцеексплорер</strong></a><br/></td>
<td>Извлекает интерфейс, который позволяет расширениям оболочки размещения и другим компонентам предотвратить преждевременное закрытие хостных процессов. Хост-процесс обычно является проводником Windows или Windows Internet Explorer, но эта функция также может использоваться другими приложениями.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>шжетитемфромдатаобжект</strong></a><br/></td>
<td>Создает <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>интерфейса IShellItem</strong></a> или связанный объект на основе элемента, заданного интерфейсом <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>IDataObject</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromobject"><strong>шжетитемфромобжект</strong></a><br/></td>
<td>Возвращает объект <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>интерфейса IShellItem</strong></a> для объекта.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist"><strong>шжеткновнфолдеридлист</strong></a><br/></td>
<td>Получает путь к известной папке в виде структуры <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>итемидлист</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderitem"><strong>шжеткновнфолдеритем</strong></a><br/></td>
<td>Извлекает объект <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>интерфейса IShellItem</strong></a> , представляющий известную папку.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath"><strong>шжеткновнфолдерпас</strong></a><br/></td>
<td>Получает полный путь к известной папке, идентифицируемой <a href="knownfolderid.md"><strong>кновнфолдерид</strong></a>папки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetlocalizedname"><strong>шжетлокализеднаме</strong></a><br/></td>
<td>Извлекает локализованное имя файла в папке оболочки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>шжетнамефромидлист</strong></a><br/></td>
<td>Извлекает отображаемое имя элемента, идентифицируемого его IDList.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762192(v=vs.85)"><strong>шжетнамефромпропертикэй</strong></a><br/></td>
<td>Извлекает каноническое имя свойства по заданному <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetnewlinkinfoa"><strong>шжетневлинкинфо</strong></a><br/></td>
<td>Создает имя для нового ярлыка на основе предложенного целевого объекта ярлыка. Эта функция не создает ярлык, просто имя.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>шжетпасфромидлист</strong></a><br/></td>
<td>Преобразует список идентификаторов элементов в путь файловой системы.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlistex"><strong>шжетпасфромидлистекс</strong></a><br/></td>
<td>Преобразует список идентификаторов элементов в путь файловой системы. Эта функция расширяет <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista"><strong>шжетпасфромидлист</strong></a> , позволяя задать начальный размер буфера строк и объявить приведенные ниже параметры.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>шжетсеттингс</strong></a><br/></td>
<td>Получает текущие настройки параметров оболочки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>шжетстоккиконинфо</strong></a><br/></td>
<td>Извлекает сведения об определенных системой значках оболочки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgettemporarypropertyforitem"><strong>шжеттемпорарипропертифоритем</strong></a><br/></td>
<td>Извлекает временное свойство для данного элемента. Временное свойство — это хранилище для чтения и записи, которое содержит свойства только в течение времени существования объекта <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>интерфейса IShellItem</strong></a> , а не сохраняется обратно в элемент.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetunreadmailcountw"><strong>шжетунреадмаилкаунт</strong></a><br/></td>
<td>Возвращает число непрочитанных сообщений указанного пользователя для всех или всех учетных записей электронной почты.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shisfileavailableoffline"><strong>шисфилеаваилаблеоффлине</strong></a><br/></td>
<td>Определяет, доступен ли файл или папка для автономного использования. Эта функция также определяет, будет ли файл открываться из сети, из локального кэша автономные файлы или из обоих расположений.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shloadinproc"><strong>шлоадинпрок</strong></a><br/></td>
<td>Создает экземпляр указанного класса объекта в контексте процесса оболочки. <br/> <strong>Windows Vista</strong> и более поздние версии: Эта функция была отключена и возвращает E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shellapi/nf-shellapi-shloadnonloadediconoverlayidentifiers"><strong>шлоаднонлоадедиконоверлайидентифиерс</strong></a><br/></td>
<td>Сигнализирует оболочке о том, что во время следующей операции требуются сведения о наложении, он должен загрузить идентификаторы оверлея значков, которые не удалось создать или которые отсутствовали для создания при запуске. Идентификаторы, которые уже были загружены, не затрагиваются.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shlocalstrdupa"><strong>шлокалстрдуп</strong></a><br/></td>
<td>Создает копию строки в только что выделенной памяти.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shmultifileproperties"><strong>шмултифилепропертиес</strong></a><br/></td>
<td>Отображает объединенную страницу свойств для набора файлов. Значения свойств, общие для всех файлов, отображаются, в то время как те, которые различаются, отображают строку <strong>(несколько значений)</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenfolderandselectitems"><strong>шопенфолдерандселектитемс</strong></a><br/></td>
<td>Открывает окно проводника Windows с указанными элементами в определенной папке.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>шопенвисдиалог</strong></a><br/></td>
<td>Отображает диалоговое окно <strong>Открыть с помощью</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/showsharefolderui"><strong>шовшарефолдеруи</strong></a><br/></td>
<td>Отображает вкладку <strong>общий доступ к папке</strong> на странице свойств указанной папки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shparsedisplayname"><strong>шпарседисплайнаме</strong></a><br/></td>
<td>Преобразует отображаемое имя объекта пространства имен оболочки в список идентификаторов элементов и возвращает атрибуты объекта. Эта функция является предпочтительным методом преобразования строки в ПИДЛ.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shpathprepareforwritea"><strong>шпаспрепарефорврите</strong></a><br/></td>
<td>Проверяет, существует ли путь. Сюда входит повторное подключение сопоставленных сетевых дисков, запрос на извлечение извлеченных носителей, создание путей, запрос носителя для форматирования и предоставление соответствующих пользовательских интерфейсов при необходимости. Разрешения на чтение и запись для носителя не проверяются.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>шкуерирециклебин</strong></a><br/></td>
<td>Получение размера корзины и количества элементов в ней для указанного диска.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>шкуерюсернотификатионстате</strong></a><br/></td>
<td>Проверяет состояние компьютера для текущего пользователя, чтобы определить, подходит ли отправка уведомления.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shremovelocalizedname"><strong>шремовелокализеднаме</strong></a><br/></td>
<td>Удаляет локализованное имя файла в папке оболочки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-shruncontrolpanel"><strong>шрунконтролпанел</strong></a><br/></td>
<td>Открывает элемент панели управления. <br/>
<blockquote>
[!Note]<br />
Эта функция не поддерживается в Windows Vista
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nf-shobjidl-shsetdefaultproperties"><strong>шсетдефаултпропертиес</strong></a><br/></td>
<td>Применяет набор свойств по умолчанию для элемента оболочки.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer"><strong>шсетинстанцеексплорер</strong></a><br/></td>
<td>Предоставляет интерфейс, который позволяет расширениям оболочки размещения и другим компонентам предотвращать преждевременное закрытие хостных процессов. Хост-процесс обычно является проводником Windows или Internet Explorer, но эта функция также может использоваться другими приложениями.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath"><strong>шсеткновнфолдерпас</strong></a><br/></td>
<td>Перенаправляет известную папку в новое расположение.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetlocalizedname"><strong>шсетлокализеднаме</strong></a><br/></td>
<td>Задает локализованное имя файла в папке оболочки.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shsettemporarypropertyforitem"><strong>шсеттемпорарипропертифоритем</strong></a><br/></td>
<td>Задает временное свойство для указанного элемента. Временное свойство хранится в хранилище, доступном для чтения и записи и содержащее свойства только в течение времени существования объекта <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>интерфейса IShellItem</strong></a> , вместо того чтобы записывать их обратно в элемент.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shsetunreadmailcountw"><strong>шсетунреадмаилкаунт</strong></a><br/></td>
<td>Хранит число непрочитанных сообщений текущего пользователя для указанной учетной записи электронной почты в реестре.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/nf-shellapi-shtesttokenmembership"><strong>штесттокенмембершип</strong></a><br/></td>
<td>Использует <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-checktokenmembership"><strong>чекктокенмембершип</strong></a> для проверки того, является ли данный маркер членом локальной группы с указанным RID.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shupdateimagea"><strong>шупдатеимаже</strong></a><br/></td>
<td>Уведомляет оболочку о том, что изображение в списке системных образов изменилось.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/nf-shlobj-softwareupdatemessagebox"><strong>софтвареупдатемессажебокс</strong></a><br/></td>
<td>Отображает стандартное окно сообщения, которое можно использовать для уведомления пользователя об обновлении приложения.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-stgmakeuniquename"><strong>стгмакеуникуенаме</strong></a><br/></td>
<td>Создает уникальное имя для потока или объекта хранилища из шаблона.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrniw"><strong>стрстрнив</strong></a><br/></td>
<td>Находит первое вхождение подстроки в строке. При сравнении регистр не учитывается.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstrnw"><strong>стрстрнв</strong></a><br/></td>
<td>Находит первое вхождение подстроки в строке. При сравнении учитывается регистр.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>транслатеурл</strong></a><br/></td>
<td>Применяет общие переводы к заданной строке URL-адреса, создавая новую строку URL-адреса.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile"><strong>унлоадусерпрофиле</strong></a><br/></td>
<td>Выгружает профиль пользователя, который был загружен функцией <a href="/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea"><strong>LoadUserProfile</strong></a> . Вызывающий объект должен иметь права администратора на компьютере. Дополнительные сведения см. в разделе "Примечания" функции <strong>LoadUserProfile</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification"><strong>унрегистераппстатечанженотификатион</strong></a><br/></td>
<td>Отменяет уведомление об изменении, зарегистрированное с помощью <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification"><strong>регистераппстатечанженотификатион</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-unregisterscalechangeevent"><strong>унрегистерскалечанжеевент</strong></a><br/></td>
<td>Отменяет регистрацию для события изменения масштаба, зарегистрированного с помощью <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-registerscalechangeevent"><strong>регистерскалечанжеевент</strong></a>. Эта функция заменяет <a href="/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-revokescalechangenotifications"><strong>ревокескалечанженотификатионс</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>урлассоЦиатиондиалог</strong></a><br/></td>
<td>Вызывает диалоговое окно незарегистрированный протокол URL-адреса. Это диалоговое окно позволяет пользователю выбрать приложение для сопоставления с ранее неизвестным протоколом.<br/>
<blockquote>
[!Note]<br />
Windows XP SP2 или более поздней версии: Эта функция больше не поддерживается.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb762266(v=vs.85)"><strong>винексецеррор</strong></a><br/></td>
<td>Возвращает значение ошибки, формируемое, если функция <a href="/windows/win32/api/winbase/nf-winbase-winexec">винексек</a> не может запустить указанное приложение. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a><br/></td>
<td>Запускает справку Windows (Winhelp.exe) и передает дополнительные данные, указывающие характер справки, запрашиваемой приложением.<br/></td>
</tr>
</tbody>
</table>



 

 

 
