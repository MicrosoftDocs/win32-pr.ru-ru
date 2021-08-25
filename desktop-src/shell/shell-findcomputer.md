---
Описание: Shell. Финдкомпутер method-"отображает диалоговое окно" результаты поиска: компьютеры ". В диалоговом окне отображается результат поиска указанного компьютера.
MS. AssetID: 0304b955-afde-4de4-824a-9ec9c9530360 Title: метод Shell. Финдкомпутер (Шлдисп. h) MS. Topic: ссылка на MS. Date: 05/31/2018 topic_type: 
- апиреф
- api_name Кбсинтакс: 
- Api_type Shell. Финдкомпутер: 
- Api_location COM: 
- Shell32.dll
---

# <a name="shellfindcomputer-method"></a>Shell. Финдкомпутер, метод

Отображает диалоговое окно **Результаты поиска: компьютеры** . В диалоговом окне отображается результат поиска указанного компьютера.

## <a name="syntax"></a>Синтаксис


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="examples"></a>Примеры

В следующем примере показано использование **финдкомпутер** . Результат этого кода аналогичен нажатию кнопки " **Пуск** ", нажатия кнопки " **Поиск**", " **Принтеры", "компьютеры" или "люди** ", а затем выбора **компьютера в сети**. правильное использование отображается для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 




