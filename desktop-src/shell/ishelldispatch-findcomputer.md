---
Описание: Ишеллдиспатч. Финдкомпутер method-"отображает диалоговое окно" результаты поиска: компьютеры ". В диалоговом окне отображается результат поиска указанного компьютера.
MS. AssetID: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 Title: метод Ишеллдиспатч. Финдкомпутер (Шлдисп. h) MS. Topic: ссылка на MS. Date: 05/31/2018 topic_type: 
- апиреф
- api_name Кбсинтакс: 
- Api_type Ишеллдиспатч. Финдкомпутер: 
- Api_location COM: 
- Shell32.dll
---

# <a name="ishelldispatchfindcomputer-method"></a>Ишеллдиспатч. Финдкомпутер, метод

Отображает диалоговое окно **Результаты поиска: компьютеры** . В диалоговом окне отображается результат поиска указанного компьютера.

## <a name="syntax"></a>Синтаксис


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод реализован и доступен через метод [**Shell. финдкомпутер**](shell-findcomputer.md) .

## <a name="examples"></a>Примеры

в следующих примерах показано использование **финдкомпутер** в JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
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
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

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



 

 




