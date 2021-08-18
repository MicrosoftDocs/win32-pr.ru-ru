---
description: IShellDispatch4. метод задания — получает параметр глобальной оболочки.
ms.assetid: b9b1542c-8e25-4966-b3df-13bfbd9b28aa
title: Метод IShellDispatch4.-Setting (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ec31516f88dc9b79169a0272cfca735080e28aaebc81ac49cc7a8b083bc9377e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720858"
---
# <a name="ishelldispatch4getsetting-method"></a>IShellDispatch4. метод задания

Извлекает параметр глобальной оболочки.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = IShellDispatch4.GetSetting(
  lSetting
)
```


```VB

IShellDispatch4.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*лсеттинг* \[ окне\]
</dt> <dd>

Тип: **Long**

Значение типа, указывающее текущий параметр оболочки для извлечения. В каждом вызове можно получить только один параметр. Этот метод распознает следующие значения.

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**ССФ \_ АУТОЧЕККСЕЛЕКТ** (0x00800000)


</dt> <dd>

**Windows Vista и более поздних версий**. Состояние флажков " **использовать" для выбора элементов** . Этот параметр включается автоматически, если в системе настроено устройство ввода с помощью пера.

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**ССФ \_ ДЕСКТОФТМЛ** (0x00000200)


</dt> <dd>

Не используется.

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**ССФ \_ ДОНТПРЕТТИПАС** (0x00000800)


</dt> <dd>

Состояние параметра **Разрешить все прописные имена** . начиная с Windows Vista этот параметр папки больше не доступен.

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**ССФ \_ ДАУБЛЕКЛИККИНВЕБВИЕВ** (0x00000080)


</dt> <dd>

Состояние **двойного щелчка для открытия элемента (одиночный щелчок для выбора)** .

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>**ССФ \_ ФИЛЬТР** (0x00010000)


</dt> <dd>

Не используется.

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**ССФ \_ ХИДДЕНФИЛИКСТС** (0x00000004)


</dt> <dd>

Не используется.

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**ССФ \_ ХИДЕИКОНС** (0x00004000)


</dt> <dd>

состояние значка отображается в представлении списка проводника Windows. Если этот параметр активен, значки в представлении списка не отображаются.

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**ССФ \_ ИКОНСОНЛИ** (0x01000000)


</dt> <dd>

**Windows Vista и более поздних версий**. состояние отображаемого имени отображается в представлении списка проводника Windows. Если этот параметр активен, значки отображаются в представлении списка, а отображаемые имена — нет.

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**ССФ \_ МАПНЕТДРВБУТТОН** (0x00001000)


</dt> <dd>

Состояние **кнопки показывать сетевой диск в параметре панели инструментов** . начиная с Windows Vista этот параметр больше не доступен.

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**ССФ \_ НОКОНФИРМРЕЦИКЛЕ** (0x00008000)


</dt> <dd>

Состояние параметра **диалогового окна подтверждения удаления** из корзины.

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**ССФ \_ НОНЕТКРАВЛИНГ** (0x00100000)


</dt> <dd>

Состояние параметра **автоматически искать сетевые папки и принтеры** . начиная с Windows Vista этот параметр больше не доступен.

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**ССФ \_ СЕППРОЦЕСС** (0x00080000)


</dt> <dd>

Состояние **окна запуска папки в отдельном** параметре обработки.

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**ССФ \_ СЕРВЕРАДМИНУИ** (0x00000004)


</dt> <dd>

Не используется.

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**ССФ \_ ШОВАЛЛОБЖЕКТС** (0x00000001)


</dt> <dd>

Состояние параметра **скрытые файлы и папки** .

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**ССФ \_ ШОВАТТРИБКОЛ** (0x00000100)


</dt> <dd>

Состояние параметра **Показать атрибуты файла в подробном представлении** . начиная с Windows Vista этот параметр больше не доступен.

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**ССФ \_ ШОВКОМПКОЛОР** (0x00000008)


</dt> <dd>

Состояние параметра **Показывать зашифрованные или сжатые файлы NTFS в цвете** .

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**ССФ \_ ШОВЕКСТЕНСИОНС** (0x00000002)


</dt> <dd>

Состояние параметра **Скрывать расширения для известных типов файлов** .

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**ССФ \_ ШОВИНФОТИП** (0x00002000)


</dt> <dd>

Состояние параметра **Показать всплывающее описание для папок и элементов рабочего стола** .

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**ССФ \_ ШОВСТАРТПАЖЕ** (0x00400000)


</dt> <dd>

Не используется.

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**ССФ \_ ШОВСУПЕРХИДДЕН** (0x00040000)


</dt> <dd>

Состояние параметра **Скрывать защищенные системные файлы** .

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**ССФ \_ ШОВСИСФИЛЕС** (0x00000020)


</dt> <dd>

Состояние параметра **скрытые файлы и папки** . в Windows Vista и более поздних версий это эквивалентно ссф \_ шоваллобжектс. в версиях Windows до Windows Vista это значение указывает на состояние параметра не **показывать скрытые файлы и папки** .

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**ССФ \_ ШОВТИПЕОВЕРЛАЙ** (0x02000000)


</dt> <dd>

**Windows Vista и более поздних версий**. Состояние **значка отображаемого файла в параметре эскизов** . Если этот параметр активен, то при указании файла в виде эскиза применяется наложение типа файла.

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**ССФ \_ СОРТКОЛУМНС** (0x00000010)


</dt> <dd>

Не используется.

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**ССФ \_ СТАРТПАНЕЛОН** (0x00200000)


</dt> <dd>

состояние параметра отображения Windows XP, которое выбирает между стилем Windows XP и классическим стилем. начиная с Windows Vista этот параметр больше не доступен.

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**ССФ \_ WEBVIEW** (0x00020000)


</dt> <dd>

Состояние **отображения в виде веб-представления**. начиная с Windows Vista этот параметр больше не доступен.

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**ССФ \_ WIN95CLASSIC** (0x00000400)


</dt> <dd>

Состояние параметра **классического стиля** . начиная с Windows Vista этот параметр больше не доступен.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **Variant \_ bool \***

Задайте значение **true** , если параметр существует. в противном случае — **значение false**.

### <a name="vb"></a>VB

Тип: **Variant \_ bool \***

Задайте значение **true** , если параметр существует. в противном случае — **значение false**.

## <a name="examples"></a>Примеры

в следующих примерах показано использование **параметра** JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 6,0 или более поздняя)</dt> </dl> |



 

 




