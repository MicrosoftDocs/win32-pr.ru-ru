---
description: Извлекает объект InternetExplorer, представляющий окно оболочки.
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: Метод Шеллвиндовс. Item (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264896"
---
# <a name="shellwindowsitem-method"></a><span data-ttu-id="1b5e8-103">Шеллвиндовс. Item, метод</span><span class="sxs-lookup"><span data-stu-id="1b5e8-103">ShellWindows.Item method</span></span>

<span data-ttu-id="1b5e8-104">Извлекает объект [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) , представляющий окно оболочки.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-104">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b5e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b5e8-105">Syntax</span></span>


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="1b5e8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b5e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b5e8-107">*ииндекс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1b5e8-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1b5e8-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="1b5e8-108">Type: **Variant**</span></span>

<span data-ttu-id="1b5e8-109">Начинающийся с нуля индекс извлекаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="1b5e8-110">Это значение должно быть меньше значения свойства [**Count**](shellwindows-count.md) .</span><span class="sxs-lookup"><span data-stu-id="1b5e8-110">This value must be less than the value of the [**Count**](shellwindows-count.md) property.</span></span> <span data-ttu-id="1b5e8-111">Если это значение не указано, используется значение по умолчанию 0.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-111">If this value is omitted, a default value of 0 is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b5e8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b5e8-112">Return value</span></span>

<span data-ttu-id="1b5e8-113">Тип: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="1b5e8-113">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="1b5e8-114">Ссылка на объект [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) , представляющий окно оболочки.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-114">An object reference to the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="examples"></a><span data-ttu-id="1b5e8-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="1b5e8-115">Examples</span></span>

<span data-ttu-id="1b5e8-116">В следующем примере [**элемент**](folderitemverbs-item.md) используется для извлечения объекта [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) , представляющего первый элемент окна оболочки.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-116">The following example uses [**Item**](folderitemverbs-item.md) to retrieve the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the first Shell window item.</span></span> <span data-ttu-id="1b5e8-117">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1b5e8-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1b5e8-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="1b5e8-118">JScript:</span></span>


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



<span data-ttu-id="1b5e8-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="1b5e8-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1b5e8-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1b5e8-120">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1b5e8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1b5e8-121">Requirements</span></span>



| <span data-ttu-id="1b5e8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1b5e8-122">Requirement</span></span> | <span data-ttu-id="1b5e8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1b5e8-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b5e8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b5e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1b5e8-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1b5e8-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1b5e8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b5e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1b5e8-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1b5e8-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1b5e8-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1b5e8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b5e8-129"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b5e8-129"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="1b5e8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1b5e8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b5e8-131"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="1b5e8-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
