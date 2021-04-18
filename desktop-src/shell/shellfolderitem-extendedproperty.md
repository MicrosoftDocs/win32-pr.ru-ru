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
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985880"
---
# <a name="shellfolderitemextendedproperty-method"></a><span data-ttu-id="52f54-104">Шеллфолдеритем. ExtendedProperty, метод</span><span class="sxs-lookup"><span data-stu-id="52f54-104">ShellFolderItem.ExtendedProperty method</span></span>

<span data-ttu-id="52f54-105">Возвращает значение свойства из набора свойств элемента.</span><span class="sxs-lookup"><span data-stu-id="52f54-105">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="52f54-106">Свойство может быть задано либо по имени, либо идентификатором формата набора свойств (FMTID) и идентификатором свойства (PID).</span><span class="sxs-lookup"><span data-stu-id="52f54-106">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span>

## <a name="syntax"></a><span data-ttu-id="52f54-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52f54-107">Syntax</span></span>


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a><span data-ttu-id="52f54-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="52f54-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52f54-109">*спропнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="52f54-109">*sPropName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52f54-110">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="52f54-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="52f54-111">**Строковое** значение, указывающее свойство.</span><span class="sxs-lookup"><span data-stu-id="52f54-111">A **String** value that specifies the property.</span></span> <span data-ttu-id="52f54-112">Подробные сведения см. в разделе "Заметки".</span><span class="sxs-lookup"><span data-stu-id="52f54-112">See the Remarks section for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52f54-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="52f54-113">Return value</span></span>

<span data-ttu-id="52f54-114">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="52f54-114">Type: \**Variant\** _</span></span>

<span data-ttu-id="52f54-115">При возврате из этого метода содержит значение свойства, если оно существует для указанного элемента.</span><span class="sxs-lookup"><span data-stu-id="52f54-115">When this method returns, contains the value of the property, if it exists for the specified item.</span></span> <span data-ttu-id="52f54-116">Значение будет иметь полную типизацию, например, даты возвращаются как даты, а не строки.</span><span class="sxs-lookup"><span data-stu-id="52f54-116">The value will have full typing—for example, dates are returned as dates, not strings.</span></span>

<span data-ttu-id="52f54-117">Этот метод возвращает строку нулевой длины, если свойство является допустимым, но не существует для указанного элемента, или код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="52f54-117">This method returns a zero-length string if the property is valid but does not exist for the specified item, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="52f54-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="52f54-118">Remarks</span></span>

<span data-ttu-id="52f54-119">Задать свойство можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="52f54-119">There are two ways to specify a property.</span></span> <span data-ttu-id="52f54-120">Первым является присвоение известного имени свойства, например "author" или "Date", _sPropName \*.</span><span class="sxs-lookup"><span data-stu-id="52f54-120">The first is to assign the property's well-known name, such as "Author" or "Date", to _sPropName\*.</span></span> <span data-ttu-id="52f54-121">Однако каждое свойство является членом набора свойств модели COM, и его также можно определить, указав идентификатор формата (FMTID) и идентификатор свойства (PID).</span><span class="sxs-lookup"><span data-stu-id="52f54-121">However, each property is a member of a Component Object Model (COM) property set and can also be identified by specifying its format ID (FMTID) and property ID (PID).</span></span> <span data-ttu-id="52f54-122">[**FMTID**](../stg/structured-storage-serialized-property-set-format.md) — это идентификатор GUID, определяющий набор свойств, а [**идентификатор процесса**](../stg/structured-storage-serialized-property-set-format.md) — это целое число, которое определяет конкретное свойство в наборе свойств.</span><span class="sxs-lookup"><span data-stu-id="52f54-122">An [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) is a GUID that identifies the property set, and a [**PID**](../stg/structured-storage-serialized-property-set-format.md) is an integer that identifies a particular property within the property set.</span></span>

<span data-ttu-id="52f54-123">Указание свойства по его значениям FMTID и PID обычно более эффективно, чем использование его имени.</span><span class="sxs-lookup"><span data-stu-id="52f54-123">Specifying a property by its FMTID/PID values is usually more efficient than using its name.</span></span> <span data-ttu-id="52f54-124">Чтобы использовать значения FMTID или PID свойства с **ExtendedProperty**, их необходимо объединить в сЦид.</span><span class="sxs-lookup"><span data-stu-id="52f54-124">To use a property's FMTID/PID values with **ExtendedProperty**, they must be combined into an SCID.</span></span> <span data-ttu-id="52f54-125">СЦИД — это строка, содержащая значения FMTID/PID в формате "*FMTID \* \* PID*", где FMTID — это строка идентификатора GUID набора свойств.</span><span class="sxs-lookup"><span data-stu-id="52f54-125">An SCID is a string that contains the FMTID/PID values in the form "*FMTID\*\*PID*", where the FMTID is the string form of the property set's GUID.</span></span> <span data-ttu-id="52f54-126">Например, СЦИД свойства Author набора свойств сводки имеет значение "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span><span class="sxs-lookup"><span data-stu-id="52f54-126">For example, the SCID of the summary information property set's author property is "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span></span>

<span data-ttu-id="52f54-127">Список Фмтидс и идентификаторов PID, которые в настоящее время поддерживаются оболочкой, см. в разделе [**школумнид**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="52f54-127">For a list of FMTIDs and PIDs that are currently supported by the Shell, see [**SHCOLUMNID**](./objects.md).</span></span>

## <a name="examples"></a><span data-ttu-id="52f54-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="52f54-128">Examples</span></span>

<span data-ttu-id="52f54-129">В этом примере кода показано, как использовать **ExtendedProperty** для получения свойств "Title" и "author" из документа Word.</span><span class="sxs-lookup"><span data-stu-id="52f54-129">This sample code illustrates how to use **ExtendedProperty** to retrieve the "Title" and "Author" properties from a Word document.</span></span> <span data-ttu-id="52f54-130">После получения объекта [**шеллфолдеритем**](shellfolderitem-object.md) , связанного с файлом, *фиворддок* в этом примере извлеките значение свойства, передав его имя в **ExtendedProperty**.</span><span class="sxs-lookup"><span data-stu-id="52f54-130">Once you have the [**ShellFolderItem**](shellfolderitem-object.md) object associated with the file, *fiWordDoc* in this example, retrieve the property's value by passing its name to **ExtendedProperty**.</span></span>


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



<span data-ttu-id="52f54-131">Более быстрый и эффективный подход — передать СЦИД в **ExtendedProperty**.</span><span class="sxs-lookup"><span data-stu-id="52f54-131">A faster and more efficient approach is to pass an SCID to **ExtendedProperty**.</span></span>


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



<span data-ttu-id="52f54-132">В следующих примерах показано правильное использование этого метода для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="52f54-132">The following examples show the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="52f54-133">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="52f54-133">JScript:</span></span>


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



<span data-ttu-id="52f54-134">Сценариев</span><span class="sxs-lookup"><span data-stu-id="52f54-134">VBScript:</span></span>


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



<span data-ttu-id="52f54-135">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="52f54-135">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="52f54-136">Требования</span><span class="sxs-lookup"><span data-stu-id="52f54-136">Requirements</span></span>



| <span data-ttu-id="52f54-137">Требование</span><span class="sxs-lookup"><span data-stu-id="52f54-137">Requirement</span></span> | <span data-ttu-id="52f54-138">Значение</span><span class="sxs-lookup"><span data-stu-id="52f54-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f54-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52f54-139">Minimum supported client</span></span><br/> | <span data-ttu-id="52f54-140">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52f54-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52f54-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52f54-141">Minimum supported server</span></span><br/> | <span data-ttu-id="52f54-142">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52f54-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="52f54-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="52f54-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="52f54-144"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f54-144"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="52f54-145">IDL</span><span class="sxs-lookup"><span data-stu-id="52f54-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52f54-146"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="52f54-146"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="52f54-147">DLL</span><span class="sxs-lookup"><span data-stu-id="52f54-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52f54-148"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="52f54-148"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
