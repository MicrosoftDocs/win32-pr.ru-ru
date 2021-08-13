---
description: Возвращает значение свойства из набора свойств элемента. Свойство может быть задано либо по имени, либо идентификатором формата набора свойств (FMTID) и идентификатором свойства (PID).
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: Шеллфолдеритем. ExtendedProperty, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f5aa8ab3ba61d752cfe4d9f8ecd29bf4fcd06c3dbadde94e51ac9a05a8504b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452820"
---
# <a name="shellfolderitemextendedproperty-method"></a>Шеллфолдеритем. ExtendedProperty, метод

Возвращает значение свойства из набора свойств элемента. Свойство может быть задано либо по имени, либо идентификатором формата набора свойств (FMTID) и идентификатором свойства (PID).

## <a name="syntax"></a>Синтаксис


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*спропнаме* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строковое** значение, указывающее свойство. Подробные сведения см. в разделе "Заметки".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **Variant \***

При возврате из этого метода содержит значение свойства, если оно существует для указанного элемента. Значение будет иметь полную типизацию, например, даты возвращаются как даты, а не строки.

Этот метод возвращает строку нулевой длины, если свойство является допустимым, но не существует для указанного элемента, или код ошибки в противном случае.

## <a name="remarks"></a>Remarks

Задать свойство можно двумя способами. Первым является назначение известного имени свойства, например "author" или "Date", *спропнаме*. Однако каждое свойство является членом набора свойств модели COM, и его также можно определить, указав идентификатор формата (FMTID) и идентификатор свойства (PID). [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) — это идентификатор GUID, определяющий набор свойств, а [**идентификатор процесса**](../stg/structured-storage-serialized-property-set-format.md) — это целое число, которое определяет конкретное свойство в наборе свойств.

Указание свойства по его значениям FMTID и PID обычно более эффективно, чем использование его имени. Чтобы использовать значения FMTID или PID свойства с **ExtendedProperty**, их необходимо объединить в сЦид. СЦИД — это строка, содержащая значения FMTID/PID в формате "*FMTID * * PID*", где FMTID — это строка идентификатора GUID набора свойств. Например, СЦИД свойства Author набора свойств сводки имеет значение "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".

Список Фмтидс и идентификаторов PID, которые в настоящее время поддерживаются оболочкой, см. в разделе [**школумнид**](./objects.md).

## <a name="examples"></a>Примеры

В этом примере кода показано, как использовать **ExtendedProperty** для получения свойств "Title" и "author" из документа Word. После получения объекта [**шеллфолдеритем**](shellfolderitem-object.md) , связанного с файлом, *фиворддок* в этом примере извлеките значение свойства, передав его имя в **ExtendedProperty**.


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



Более быстрый и эффективный подход — передать СЦИД в **ExtendedProperty**.


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



в следующих примерах показано правильное использование этого метода для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderItem2ExtendedPropertyVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



 

 
