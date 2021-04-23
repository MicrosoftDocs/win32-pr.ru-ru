---
description: Отображает диалоговое окно Поиск принтера.
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Метод Shell. Финдпринтер (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1286bb7247359ea91d29a53f8f0eaa13b55be5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985977"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="d2ca6-103">Shell. Финдпринтер, метод</span><span class="sxs-lookup"><span data-stu-id="d2ca6-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="d2ca6-104">Отображает диалоговое окно **Поиск принтера** .</span><span class="sxs-lookup"><span data-stu-id="d2ca6-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ca6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2ca6-105">Syntax</span></span>


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="d2ca6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2ca6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ca6-107">*sName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d2ca6-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ca6-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d2ca6-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d2ca6-109">**Строка** , содержащая имя принтера.</span><span class="sxs-lookup"><span data-stu-id="d2ca6-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="d2ca6-110">*слокатион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d2ca6-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ca6-111">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d2ca6-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d2ca6-112">**Строка** , содержащая расположение принтера.</span><span class="sxs-lookup"><span data-stu-id="d2ca6-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="d2ca6-113">*смодел* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d2ca6-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ca6-114">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d2ca6-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d2ca6-115">**Строка** , содержащая модель принтера.</span><span class="sxs-lookup"><span data-stu-id="d2ca6-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2ca6-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d2ca6-116">Remarks</span></span>

<span data-ttu-id="d2ca6-117">Если вы назначаете строки одному или нескольким необязательным параметрам, они отображаются как значения по умолчанию в связанном элементе управления "поле ввода" при отображении диалогового окна " **Найти принтер** ".</span><span class="sxs-lookup"><span data-stu-id="d2ca6-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="d2ca6-118">Пользователь может либо принять, либо переопределить эти значения.</span><span class="sxs-lookup"><span data-stu-id="d2ca6-118">The user can either accept or override these values.</span></span> <span data-ttu-id="d2ca6-119">Если параметру не присвоено значение, соответствующее поле редактирования будет пустым и пользователь должен ввести значение.</span><span class="sxs-lookup"><span data-stu-id="d2ca6-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="d2ca6-120">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d2ca6-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="d2ca6-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="d2ca6-121">Examples</span></span>

<span data-ttu-id="d2ca6-122">В следующих примерах показано использование **финдпринтер** для отображения диалогового окна **Найти принтер** для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="d2ca6-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="d2ca6-123">Сведения об использовании представлены для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d2ca6-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d2ca6-124">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="d2ca6-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="d2ca6-125">Сценариев</span><span class="sxs-lookup"><span data-stu-id="d2ca6-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="d2ca6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d2ca6-126">Requirements</span></span>



| <span data-ttu-id="d2ca6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d2ca6-127">Requirement</span></span> | <span data-ttu-id="d2ca6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d2ca6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ca6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2ca6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ca6-130">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d2ca6-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2ca6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2ca6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ca6-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2ca6-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d2ca6-133">Header</span><span class="sxs-lookup"><span data-stu-id="d2ca6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2ca6-134"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2ca6-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d2ca6-135">IDL</span><span class="sxs-lookup"><span data-stu-id="d2ca6-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2ca6-136"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2ca6-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d2ca6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ca6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2ca6-138"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="d2ca6-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
