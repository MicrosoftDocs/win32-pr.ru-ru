---
description: Shell. Финдпринтер-метод — отображает диалоговое окно Поиск принтера.
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
ms.openlocfilehash: 17d04b60de2b52ca3d2f17fbdccf7de93ac095b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104312"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="42336-103">Shell. Финдпринтер, метод</span><span class="sxs-lookup"><span data-stu-id="42336-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="42336-104">Отображает диалоговое окно **Поиск принтера** .</span><span class="sxs-lookup"><span data-stu-id="42336-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="42336-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42336-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="42336-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42336-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42336-107">*sName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="42336-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42336-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="42336-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="42336-109">**Строка** , содержащая имя принтера.</span><span class="sxs-lookup"><span data-stu-id="42336-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="42336-110">*слокатион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="42336-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42336-111">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="42336-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="42336-112">**Строка** , содержащая расположение принтера.</span><span class="sxs-lookup"><span data-stu-id="42336-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="42336-113">*смодел* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="42336-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="42336-114">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="42336-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="42336-115">**Строка** , содержащая модель принтера.</span><span class="sxs-lookup"><span data-stu-id="42336-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42336-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="42336-116">Remarks</span></span>

<span data-ttu-id="42336-117">Если вы назначаете строки одному или нескольким необязательным параметрам, они отображаются как значения по умолчанию в связанном элементе управления "поле ввода" при отображении диалогового окна " **Найти принтер** ".</span><span class="sxs-lookup"><span data-stu-id="42336-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="42336-118">Пользователь может либо принять, либо переопределить эти значения.</span><span class="sxs-lookup"><span data-stu-id="42336-118">The user can either accept or override these values.</span></span> <span data-ttu-id="42336-119">Если параметру не присвоено значение, соответствующее поле редактирования будет пустым и пользователь должен ввести значение.</span><span class="sxs-lookup"><span data-stu-id="42336-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="42336-120">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="42336-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="42336-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="42336-121">Examples</span></span>

<span data-ttu-id="42336-122">В следующих примерах показано использование **финдпринтер** для отображения диалогового окна **Найти принтер** для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="42336-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="42336-123">Сведения об использовании представлены для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="42336-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="42336-124">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="42336-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="42336-125">Сценариев</span><span class="sxs-lookup"><span data-stu-id="42336-125">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="42336-126">Требования</span><span class="sxs-lookup"><span data-stu-id="42336-126">Requirements</span></span>



| <span data-ttu-id="42336-127">Требование</span><span class="sxs-lookup"><span data-stu-id="42336-127">Requirement</span></span> | <span data-ttu-id="42336-128">Значение</span><span class="sxs-lookup"><span data-stu-id="42336-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42336-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42336-129">Minimum supported client</span></span><br/> | <span data-ttu-id="42336-130">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="42336-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42336-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42336-131">Minimum supported server</span></span><br/> | <span data-ttu-id="42336-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42336-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="42336-133">Header</span><span class="sxs-lookup"><span data-stu-id="42336-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="42336-134"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="42336-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="42336-135">IDL</span><span class="sxs-lookup"><span data-stu-id="42336-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42336-136"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42336-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="42336-137">DLL</span><span class="sxs-lookup"><span data-stu-id="42336-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42336-138"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="42336-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
