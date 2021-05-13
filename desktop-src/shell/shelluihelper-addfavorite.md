---
description: Отображает пользовательский интерфейс по умолчанию для создания элемента избранного. Пользовательский интерфейс инициализируется с указанными параметрами.
title: Шеллуихелпер. Аддфаворите, метод (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: 2ce6fa0a71bb2ab995e510f06b4403c78bebcc60
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842455"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="18bfb-104">Шеллуихелпер. Аддфаворите, метод</span><span class="sxs-lookup"><span data-stu-id="18bfb-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="18bfb-105">Отображает пользовательский интерфейс по умолчанию для создания элемента избранного.</span><span class="sxs-lookup"><span data-stu-id="18bfb-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="18bfb-106">Пользовательский интерфейс инициализируется с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="18bfb-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="18bfb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18bfb-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="18bfb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="18bfb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18bfb-109">*СУРЛ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="18bfb-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18bfb-110">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="18bfb-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="18bfb-111">**Строковое** значение, указывающее URL-адрес элемента, добавляемого в папку **"Избранное"** .</span><span class="sxs-lookup"><span data-stu-id="18bfb-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="18bfb-112">*втитле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="18bfb-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18bfb-113">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="18bfb-113">Type: **Variant\***</span></span>

<span data-ttu-id="18bfb-114">Значение **типа Variant** , указывающее имя элемента.</span><span class="sxs-lookup"><span data-stu-id="18bfb-114">A **Variant** value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="18bfb-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="18bfb-115">Examples</span></span>

<span data-ttu-id="18bfb-116">В следующем примере показано правильное использование этого метода для JScript Embedded в HTML и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="18bfb-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="18bfb-117">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="18bfb-117">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



<span data-ttu-id="18bfb-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="18bfb-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="18bfb-119">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="18bfb-119">Requirements</span></span>



| <span data-ttu-id="18bfb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="18bfb-120">Requirement</span></span> | <span data-ttu-id="18bfb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="18bfb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18bfb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18bfb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="18bfb-123">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="18bfb-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18bfb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18bfb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="18bfb-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="18bfb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="18bfb-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="18bfb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="18bfb-127"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="18bfb-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="18bfb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="18bfb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18bfb-129"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="18bfb-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
