---
description: Извлекает сведения об элементе в папке. Например, его размер, тип или время последнего изменения.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Метод Folder. Жетдетаилсоф (Шлобж \_ Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ab89f00f254778a2417644d894f1e9e81eb43cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990830"
---
# <a name="foldergetdetailsof-method"></a>Folder. Жетдетаилсоф, метод

Извлекает сведения об элементе в папке. Например, его размер, тип или время последнего изменения.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*витем* 
</dt> <dd>

Тип: **Variant**

Элемент, для которого необходимо получить сведения. Это должен быть объект [**FolderItem**](folderitem.md) .

</dd> <dt>

*иколумн* 
</dt> <dd>

Тип: **Integer**

**Целочисленное** значение, указывающее извлекаемую информацию. Сведения, доступные для элемента, зависят от папки, в которой он отображается. Это значение соответствует номеру столбца, начинающегося с нуля, который отображается в представлении оболочки. Для элемента в файловой системе это может быть одно из следующих значений:

<dt>



  (0)


</dt> <dd>

Возвращает имя элемента.

</dd> <dt>



 (1)


</dt> <dd>

Возвращает размер элемента.

</dd> <dt>



 (2)


</dt> <dd>

Возвращает тип элемента.

</dd> <dt>



 (3)


</dt> <dd>

Извлекает дату и время последнего изменения элемента.

</dd> <dt>



 (4)


</dt> <dd>

Извлекает атрибуты элемента.

</dd> <dt>



 (-1)


</dt> <dd>

Извлекает сведения о подсказке для элемента.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

Строка, содержащая извлеченные сведения.

## <a name="remarks"></a>Примечания

> [!Note]  
> Не все методы реализуются для всех папок. Например, метод [_ *PARSENAME* *](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID). При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).

 

## <a name="examples"></a>Примеры

В следующем примере **жетдетаилсоф** используется для получения типа файла с именем Clock.avi. Правильное использование показано в JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
            end if
            
            set objFolderItem = nothing
        end if
        
        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
    End If
    
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлобж \_ Core. h (включение шлдисп. h)</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
