---
description: Отображает диалоговое окно Поиск принтера.
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: IShellDispatch2. Финдпринтер, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 81124e3f0d04244b9b81e812e090bde25971c17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263351"
---
# <a name="ishelldispatch2findprinter-method"></a><span data-ttu-id="908f2-103">IShellDispatch2. Финдпринтер, метод</span><span class="sxs-lookup"><span data-stu-id="908f2-103">IShellDispatch2.FindPrinter method</span></span>

<span data-ttu-id="908f2-104">Отображает диалоговое окно **Поиск принтера** .</span><span class="sxs-lookup"><span data-stu-id="908f2-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="908f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="908f2-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="908f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="908f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="908f2-107">*sName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="908f2-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="908f2-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="908f2-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="908f2-109">**Строка** , содержащая имя принтера.</span><span class="sxs-lookup"><span data-stu-id="908f2-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="908f2-110">*слокатион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="908f2-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="908f2-111">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="908f2-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="908f2-112">**Строка** , содержащая расположение принтера.</span><span class="sxs-lookup"><span data-stu-id="908f2-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="908f2-113">*смодел* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="908f2-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="908f2-114">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="908f2-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="908f2-115">**Строка** , содержащая модель принтера.</span><span class="sxs-lookup"><span data-stu-id="908f2-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="908f2-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="908f2-116">Remarks</span></span>

<span data-ttu-id="908f2-117">Этот метод реализован и доступен через метод [**Shell. финдпринтер**](./shell-findprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="908f2-117">This method is implemented and accessed through the [**Shell.FindPrinter**](./shell-findprinter.md) method.</span></span>

<span data-ttu-id="908f2-118">Если вы назначаете строки одному или нескольким необязательным параметрам, они отображаются как значения по умолчанию в связанном элементе управления "поле ввода" при отображении диалогового окна " **Найти принтер** ".</span><span class="sxs-lookup"><span data-stu-id="908f2-118">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="908f2-119">Пользователь может либо принять, либо переопределить эти значения.</span><span class="sxs-lookup"><span data-stu-id="908f2-119">The user can either accept or override these values.</span></span> <span data-ttu-id="908f2-120">Если параметру не присвоено значение, соответствующее поле редактирования будет пустым и пользователь должен ввести значение.</span><span class="sxs-lookup"><span data-stu-id="908f2-120">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="908f2-121">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="908f2-121">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="908f2-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="908f2-122">Examples</span></span>

<span data-ttu-id="908f2-123">В следующих примерах показано использование **финдпринтер** для отображения диалогового окна **Найти принтер** для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="908f2-123">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="908f2-124">Сведения об использовании представлены для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="908f2-124">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="908f2-125">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="908f2-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="908f2-126">Сценариев</span><span class="sxs-lookup"><span data-stu-id="908f2-126">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="908f2-127">Требования</span><span class="sxs-lookup"><span data-stu-id="908f2-127">Requirements</span></span>



| <span data-ttu-id="908f2-128">Требование</span><span class="sxs-lookup"><span data-stu-id="908f2-128">Requirement</span></span> | <span data-ttu-id="908f2-129">Значение</span><span class="sxs-lookup"><span data-stu-id="908f2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="908f2-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="908f2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="908f2-131">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="908f2-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="908f2-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="908f2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="908f2-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="908f2-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="908f2-134">Header</span><span class="sxs-lookup"><span data-stu-id="908f2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="908f2-135"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="908f2-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="908f2-136">IDL</span><span class="sxs-lookup"><span data-stu-id="908f2-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="908f2-137"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="908f2-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="908f2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="908f2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="908f2-139"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="908f2-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
