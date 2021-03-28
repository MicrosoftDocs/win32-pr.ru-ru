---
description: Выполняет поиск целевого объекта для ссылки на оболочку, даже если целевой объект был перемещен или переименован.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Метод Шелллинкобжект. Resolve (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b1cb0760f1ee19acfa10208711e73919fd084ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986060"
---
# <a name="shelllinkobjectresolve-method"></a>Шелллинкобжект. Resolve, метод

Выполняет поиск целевого объекта для ссылки на оболочку, даже если целевой объект был перемещен или переименован.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ффлагс* \[ окне\]
</dt> <dd>

Тип: **Integer**

Флаги, указывающие выполняемое действие. Это может быть сочетание следующих значений:

<dt>



 (1)


</dt> <dd>

Не выводите диалоговое окно, если ссылка не может быть разрешена. Если этот флаг установлен, в значении параметра *ффлагс* в высоком порядке указывается время ожидания в миллисекундах. Метод возвращает, если ссылка не может быть разрешена в течение времени ожидания. Если для слова с высоким порядковым значением установлено значение 0, то время ожидания по умолчанию составляет 3000 миллисекунд (3 секунды).

</dd> <dt>



 (4)


</dt> <dd>

Если ссылка изменилась, обновите ее путь и список идентификаторов.

</dd> <dt>



 (8)


</dt> <dd>

Не обновляйте сведения о ссылках.

</dd> <dt>



 (16)


</dt> <dd>

Не выполняйте эвристику поиска.

</dd> <dt>



 (32)


</dt> <dd>

Не используйте отслеживание распределенных ссылок.

</dd> <dt>



 (64)


</dt> <dd>

Отключение отслеживания распределенных ссылок. По умолчанию отслеживание распределенных ссылок отслеживает съемные носители на нескольких устройствах на основе имени тома. Он также использует UNC-путь для трассировки удаленных файловых систем, буква диска которых изменилась. Установка этого флага отключает оба типа отслеживания.

</dd> <dt>



 (128)


</dt> <dd>

Вызовите установщик Windows.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Примечания

Этот метод по сути идентичен функциональным возможностям для [**разрешения**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve). Дополнительные сведения о разрешении ссылок см. в разделе "Примечания" этой страницы.

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование этого метода для JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
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
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



 

 
