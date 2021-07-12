---
description: оболочка Windows предоставляет мощный набор объектов автоматизации, позволяющих программировать оболочку с помощью microsoft Visual Basic и языков сценариев, таких как microsoft JScript (совместимая со спецификацией ECMA 262) и Microsoft Visual Basic scripting Edition (VBScript). Эти объекты можно использовать для доступа ко многим функциям и диалоговым окнам оболочки. Например, можно получить доступ к файловой системе, запустить программы и изменить параметры системы.
title: Объекты оболочки с скриптами
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e8685b44d00d3f48e8de2a567218ef08c1cb5070
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581782"
---
# <a name="scriptable-shell-objects"></a>Объекты оболочки с скриптами

оболочка Windows предоставляет мощный набор объектов автоматизации, позволяющих программировать оболочку с помощью microsoft Visual Basic и языков сценариев, таких как microsoft JScript (совместимая со спецификацией ECMA 262) и Microsoft Visual Basic scripting Edition (VBScript). Эти объекты можно использовать для доступа ко многим функциям и диалоговым окнам оболочки. Например, можно получить доступ к файловой системе, запустить программы и изменить параметры системы.

В этом разделе представлены объекты оболочки, поддерживающие скрипты.

-   [Версии оболочки](#shell-versions)
-   [Создание экземпляров объектов оболочки](#instantiating-shell-objects)
    -   [Позднее связывание](#late-binding)
    -   [HTML-элемент OBJECT](#html-object-element)
-   [Объект оболочки](#shell-object)
    -   [Безопасность](#security)
-   [Объекты папки](#folder-objects)

## <a name="shell-versions"></a>Версии оболочки

Многие объекты оболочки стали доступны в [версии 4,71](versions.md) оболочки. Другие доступны в версии 5,00 и более поздних версиях. версия 5,00 стала доступна с Windows 2000. В следующей таблице перечислены все объекты оболочки в версии оболочки, в которой объект стал доступным.



| Версия 4,71                                            | Версия 5,00                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [**Folder**](folder.md)                                | [**дидисккуотаусер**](didiskquotauser-object.md)     |
| [**фолдеритемверб**](folderitemverb.md)                | [**дисккуотаконтрол**](diskquotacontrol-object.md)   |
| [**фолдеритемвербс**](folderitemverbs.md)              | [**Folder2**](folder2-object.md)                     |
| [**Shell**](shell.md)                                  | [**FolderItem**](folderitem.md)                      |
| [**шеллфолдервиев**](shellfolderview.md)              | [**фолдеритемс**](folderitems.md)                    |
| [**шеллуихелпер**](shelluihelper.md)                  | [**FolderItems2**](folderitems2-object.md)           |
| [**шеллвиндовс**](shellwindows.md)                    | [**IShellDispatch2**](ishelldispatch2-object.md)     |
| [**вебвиевфолдерконтентс**](../lwef/webviewfoldercontents.md) | [**IShellLinkDual2**](ishelllinkdual2-object.md)     |
|                                                         | [**шеллфолдеритем**](shellfolderitem-object.md)     |
|                                                         | [**шеллфолдервиевок**](shellfolderviewoc-object.md) |
|                                                         | [**шелллинкобжект**](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a>Создание экземпляров объектов оболочки

чтобы создать экземпляр объектов оболочки в Visual Basic приложениях с ранней привязкой, добавьте ссылки на следующие библиотеки в проекте:

-   Элементы управления Microsoft Internet (SHDocVw)
-   Элементы управления и автоматизации Microsoft Shell (shell32)

### <a name="late-binding"></a>Позднее связывание

Кроме того, можно создать экземпляры многих объектов оболочки с помощью позднего связывания. этот подход работает в Visual Basic приложениях и в сценарии. В следующем примере показано, как создать экземпляр объекта [**оболочки**](shell.md) в JScript.


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



В следующем примере показано, как создать экземпляр объекта [**Folder**](folder.md) в VBScript.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



В предыдущем примере *сдир* — это путь к объекту [**Folder**](folder.md) . Обратите внимание, что значения перечисления [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) недоступны в скрипте.

Идентификатор ProgID для каждого из объектов оболочки показан в следующей таблице.



| Объект                                                  | ProgID:                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**дидисккуотаусер**](didiskquotauser-object.md)       | Microsoft. Дисккуота. 1                                                                   |
| [**дисккуотаконтрол**](diskquotacontrol-object.md)     | Не удается выполнить позднее связывание                                                                        |
| [**Folder**](folder.md)                                | консоль. Shell \_ Application. Namespace ("...")                                               |
| [**Folder2**](folder2-object.md)                       | консоль. Shell \_ Application. Namespace ("...")                                               |
| [**FolderItem**](folderitem.md)                        | консоль. Shell \_ Application. Namespace ("..."). Self или Folder. Items. Item или Folder. ParseName |
| [**фолдеритемс**](folderitems.md)                      | Папка. элементы                                                                            |
| [**FolderItems2**](folderitems2-object.md)             | Папка. элементы                                                                            |
| [**фолдеритемверб**](folderitemverb.md)                | Shell. NameSpace ("..."). Собственные глаголы. Item ()                                                |
| [**фолдеритемвербс**](folderitemverbs.md)              | FolderItem. Verbs или Shell. NameSpace ("..."). Собственные глаголы                                   |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | консоль. \_Приложение оболочки                                                                |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | Shell. NameSpace ("..."). Self. Link или Shell. NameSpace ("..."). Items (). Соединение           |
| [**Shell**](shell.md)                                  | консоль. \_Приложение оболочки                                                                |
| [**шеллфолдеритем**](shellfolderitem-object.md)       | Shell. NameSpace ("..."). Self или Shell. NameSpace ("..."). Items ()                           |
| [**шеллфолдервиев**](shellfolderview.md)              | Не удается выполнить позднее связывание                                                                        |
| [**шеллфолдервиевок**](shellfolderviewoc-object.md)   | Не удается выполнить позднее связывание                                                                        |
| [**шелллинкобжект**](shelllinkobject-object.md)       | Shell. NameSpace ("..."). Self. Link или Shell. NameSpace ("..."). Items (). Соединение           |
| [**шеллуихелпер**](shelluihelper.md)                  | Не удается выполнить позднее связывание                                                                        |
| [**шеллвиндовс**](shellwindows.md)                    | консоль. \_Windows или шеллвиндовс оболочки. \_ NewEnum                                          |
| [**вебвиевфолдерконтентс**](../lwef/webviewfoldercontents.md) | Не удается выполнить позднее связывание                                                                        |



 

### <a name="html-object-element"></a>HTML-элемент OBJECT

Элемент [**Object**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) можно также использовать для создания экземпляров объектов оболочки на HTML-странице. Для этого задайте для атрибута **ID** элемента **Object** имя переменной, которая будет использоваться в скриптах, и укажите объект, используя его зарегистрированный номер (ClassID). Следующий HTML-код создает экземпляр объекта [**шеллфолдеритем**](shellfolderitem-object.md) с помощью элемента **Object** .


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



В следующей таблице перечислены все объекты оболочки и соответствующие ИДЕНТИФИКАТОРы классов.



| Объект оболочки                                           | КЛАССА                              |
|--------------------------------------------------------|--------------------------------------|
| [**дидисккуотаусер**](didiskquotauser-object.md)       | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**дисккуотаконтрол**](diskquotacontrol-object.md)     | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**Folder**](folder.md)                                | BBCBDE60-C3FF-11CE-8350-444553540000 |
| [**Folder2**](folder2-object.md)                       | f0d2d8ef-3890-11d2-bf8b-00c04fb93661 |
| [**FolderItem**](folderitem.md)                        | 744129E0-CBE5-11CE-8350-444553540000 |
| [**фолдеритемс**](folderitems.md)                      | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems2**](folderitems2-object.md)             | C94F0AD0-F363-11d2-A327-00C04F8EEC7F |
| [**фолдеритемверб**](folderitemverb.md)                | 08EC3E00-50B0-11CF-960C-0080C7F4EE85 |
| [**фолдеритемвербс**](folderitemverbs.md)              | 1F8352C0-50B0-11CF-960C-0080C7F4EE85 |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | A4C6892C-3BA9-11d2-9DEA-00C04FB16162 |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | 317EE249-F12E-11d2-B1E4-00C04F8EEB3E |
| [**Shell**](shell.md)                                  | 13709620-C279-11CE-A49E-444553540000 |
| [**шеллфолдеритем**](shellfolderitem-object.md)       | 2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e |
| [**шеллфолдервиев**](shellfolderview.md)              | 62112AA1-EBE4-11cf-A5FB-0020AFE7292D |
| [**шеллфолдервиевок**](shellfolderviewoc-object.md)   | 4a3df050-23bd-11d2-939f-00a0c91eedba |
| [**шелллинкобжект**](shelllinkobject-object.md)       | 11219420-1768-11d1-95BE-00609797EA4F |
| [**шеллуихелпер**](shelluihelper.md)                  | 64AB4BB7-111E-11D1-8F79-00C04FC2FBE1 |
| [**шеллвиндовс**](shellwindows.md)                    | 9BA05972-F6A8-11CF-A442-00A0C90A8F39 |
| [**вебвиевфолдерконтентс**](../lwef/webviewfoldercontents.md) | 1820FED0-473E-11D0-A96C-00C04FD705A2 |



 

## <a name="shell-object"></a>Объект оболочки

Объект [**оболочки**](shell.md) представляет объекты в оболочке. Методы, предоставляемые объектом Shell, можно использовать для:

-   Открывать, изучать и просматривать папки;
-   Сократите, восстановите, каскадное или мозаичное открытие окон.
-   Запуск приложений панели управления.
-   Отображает системные диалоговые окна.

Пользователи, возможно, знакомы с командами, к которым они обращаются из меню « **Пуск** » и с контекстным меню панели задач. Контекстное меню панели задач появляется, когда пользователь правой кнопкой мыши щелкнул панель задач. Следующее HTML-приложение (HTA) создает начальную страницу с кнопками, которые реализуют многие методы объекта [**оболочки**](shell.md) . Некоторые из этих методов реализуют функции в меню « **Пуск** » и в контекстном меню панели задач.


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a>Безопасность

Как приложение, HTA выполняется с использованием другой модели безопасности, чем веб-страница. для взаимодействия с веб-страницей, реализующей функции объектов оболочки, пользователи должны включить **элементы управления "инициализация" и "скрипт ActiveX", не помеченные как "безопасный** " для зоны безопасности, в которой они просматривают страницу.

## <a name="folder-objects"></a>Объекты папки

Объект [**Folder**](folder.md) представляет папку оболочки. Методы, предоставляемые объектом Folder, можно использовать для:

-   Получение сведений о папке.
-   Создание вложенных папок.
-   Копирование и перемещение объектов File в папку.

Объект [**FolderItem**](folderitem.md) представляет элемент в папке оболочки. Его свойства позволяют получать сведения об элементе. Методы, предоставляемые этим объектом, можно использовать для выполнения глаголов элемента или для получения сведений об объекте [**фолдеритемвербс**](folderitemverbs.md) элемента.

Объект [**фолдеритемс**](folderitems.md) представляет коллекцию элементов в папке оболочки. Его методы и свойства позволяют получать сведения о коллекции.

в следующем Visual Basic примере показана связь между несколькими объектами папки и их совместное использование. Когда пользователь нажимает кнопку Command с именем **кмджетпас**, программа отображает диалоговое окно, позволяющее пользователю выбрать папку из **Мой компьютер**, где Ссфдривес — значение перечисления [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) для **Мой компьютер**. Когда пользователь выбирает папку, путь к папке отображается в текстовом поле с именем **ткстпас**.


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



В VBScript эта функция немного отличается, так как значения перечисления [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) недоступны в скрипте. В следующем примере показан пример VBScript, эквивалентный предыдущему примеру.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



в следующем JScript примере, который является прямым переводом предыдущего примера VBScript, обратите внимание на то, как пустые скобки "()" используются для вызова [**элементов**](folder-items.md) и методов [**элементов**](folderitems-item.md) .


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
