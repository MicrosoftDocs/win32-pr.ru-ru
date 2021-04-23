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
# <a name="shelllinkobjectresolve-method"></a><span data-ttu-id="87748-103">Шелллинкобжект. Resolve, метод</span><span class="sxs-lookup"><span data-stu-id="87748-103">ShellLinkObject.Resolve method</span></span>

<span data-ttu-id="87748-104">Выполняет поиск целевого объекта для ссылки на оболочку, даже если целевой объект был перемещен или переименован.</span><span class="sxs-lookup"><span data-stu-id="87748-104">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span>

## <a name="syntax"></a><span data-ttu-id="87748-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87748-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a><span data-ttu-id="87748-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87748-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87748-107">*ффлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87748-107">*fFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87748-108">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="87748-108">Type: **Integer**</span></span>

<span data-ttu-id="87748-109">Флаги, указывающие выполняемое действие.</span><span class="sxs-lookup"><span data-stu-id="87748-109">Flags that specify the action to be taken.</span></span> <span data-ttu-id="87748-110">Это может быть сочетание следующих значений:</span><span class="sxs-lookup"><span data-stu-id="87748-110">This can be a combination of the following values:</span></span>

<dt>



 <span data-ttu-id="87748-111">(1)</span><span class="sxs-lookup"><span data-stu-id="87748-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="87748-112">Не выводите диалоговое окно, если ссылка не может быть разрешена.</span><span class="sxs-lookup"><span data-stu-id="87748-112">Do not display a dialog box if the link cannot be resolved.</span></span> <span data-ttu-id="87748-113">Если этот флаг установлен, в значении параметра *ффлагс* в высоком порядке указывается время ожидания в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="87748-113">When this flag is set, the high-order word of *fFlags* specifies a time-out duration, in milliseconds.</span></span> <span data-ttu-id="87748-114">Метод возвращает, если ссылка не может быть разрешена в течение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="87748-114">The method returns if the link cannot be resolved within the time-out duration.</span></span> <span data-ttu-id="87748-115">Если для слова с высоким порядковым значением установлено значение 0, то время ожидания по умолчанию составляет 3000 миллисекунд (3 секунды).</span><span class="sxs-lookup"><span data-stu-id="87748-115">If the high-order word is set to zero, the time-out duration defaults to 3000 milliseconds (3 seconds).</span></span>

</dd> <dt>



 <span data-ttu-id="87748-116">(4)</span><span class="sxs-lookup"><span data-stu-id="87748-116">(4)</span></span>


</dt> <dd>

<span data-ttu-id="87748-117">Если ссылка изменилась, обновите ее путь и список идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="87748-117">If the link has changed, update its path and list of identifiers.</span></span>

</dd> <dt>



 <span data-ttu-id="87748-118">(8)</span><span class="sxs-lookup"><span data-stu-id="87748-118">(8)</span></span>


</dt> <dd>

<span data-ttu-id="87748-119">Не обновляйте сведения о ссылках.</span><span class="sxs-lookup"><span data-stu-id="87748-119">Do not update the link information.</span></span>

</dd> <dt>



 <span data-ttu-id="87748-120">(16)</span><span class="sxs-lookup"><span data-stu-id="87748-120">(16)</span></span>


</dt> <dd>

<span data-ttu-id="87748-121">Не выполняйте эвристику поиска.</span><span class="sxs-lookup"><span data-stu-id="87748-121">Do not execute the search heuristics.</span></span>

</dd> <dt>



 <span data-ttu-id="87748-122">(32)</span><span class="sxs-lookup"><span data-stu-id="87748-122">(32)</span></span>


</dt> <dd>

<span data-ttu-id="87748-123">Не используйте отслеживание распределенных ссылок.</span><span class="sxs-lookup"><span data-stu-id="87748-123">Do not use distributed link tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="87748-124">(64)</span><span class="sxs-lookup"><span data-stu-id="87748-124">(64)</span></span>


</dt> <dd>

<span data-ttu-id="87748-125">Отключение отслеживания распределенных ссылок.</span><span class="sxs-lookup"><span data-stu-id="87748-125">Disable distributed link tracking.</span></span> <span data-ttu-id="87748-126">По умолчанию отслеживание распределенных ссылок отслеживает съемные носители на нескольких устройствах на основе имени тома.</span><span class="sxs-lookup"><span data-stu-id="87748-126">By default, distributed link tracking tracks removable media across multiple devices based on the volume name.</span></span> <span data-ttu-id="87748-127">Он также использует UNC-путь для трассировки удаленных файловых систем, буква диска которых изменилась.</span><span class="sxs-lookup"><span data-stu-id="87748-127">It also uses the UNC path to track remote file systems whose drive letter has changed.</span></span> <span data-ttu-id="87748-128">Установка этого флага отключает оба типа отслеживания.</span><span class="sxs-lookup"><span data-stu-id="87748-128">Setting this flag disables both types of tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="87748-129">(128)</span><span class="sxs-lookup"><span data-stu-id="87748-129">(128)</span></span>


</dt> <dd>

<span data-ttu-id="87748-130">Вызовите установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="87748-130">Call the Windows Installer.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87748-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="87748-131">Remarks</span></span>

<span data-ttu-id="87748-132">Этот метод по сути идентичен функциональным возможностям для [**разрешения**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span><span class="sxs-lookup"><span data-stu-id="87748-132">This method is essentially identical in functionality to [**Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span> <span data-ttu-id="87748-133">Дополнительные сведения о разрешении ссылок см. в разделе "Примечания" этой страницы.</span><span class="sxs-lookup"><span data-stu-id="87748-133">For further discussion of link resolution, see the Remarks section of that page.</span></span>

## <a name="examples"></a><span data-ttu-id="87748-134">Примеры</span><span class="sxs-lookup"><span data-stu-id="87748-134">Examples</span></span>

<span data-ttu-id="87748-135">В следующем примере показано правильное использование этого метода для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="87748-135">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="87748-136">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="87748-136">JScript:</span></span>


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



<span data-ttu-id="87748-137">Сценариев</span><span class="sxs-lookup"><span data-stu-id="87748-137">VBScript:</span></span>


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



<span data-ttu-id="87748-138">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="87748-138">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="87748-139">Требования</span><span class="sxs-lookup"><span data-stu-id="87748-139">Requirements</span></span>



| <span data-ttu-id="87748-140">Требование</span><span class="sxs-lookup"><span data-stu-id="87748-140">Requirement</span></span> | <span data-ttu-id="87748-141">Значение</span><span class="sxs-lookup"><span data-stu-id="87748-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87748-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87748-142">Minimum supported client</span></span><br/> | <span data-ttu-id="87748-143">Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87748-143">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="87748-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87748-144">Minimum supported server</span></span><br/> | <span data-ttu-id="87748-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87748-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="87748-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="87748-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="87748-147"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="87748-147"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="87748-148">IDL</span><span class="sxs-lookup"><span data-stu-id="87748-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87748-149"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87748-149"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="87748-150">DLL</span><span class="sxs-lookup"><span data-stu-id="87748-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87748-151"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="87748-151"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
