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
ms.openlocfilehash: a5c3cae52f0ad18c1f2ddf6cf91759d1c6daf6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986021"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="4d1bc-104">Шеллуихелпер. Аддфаворите, метод</span><span class="sxs-lookup"><span data-stu-id="4d1bc-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="4d1bc-105">Отображает пользовательский интерфейс по умолчанию для создания элемента избранного.</span><span class="sxs-lookup"><span data-stu-id="4d1bc-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="4d1bc-106">Пользовательский интерфейс инициализируется с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="4d1bc-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d1bc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d1bc-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="4d1bc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d1bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d1bc-109">*СУРЛ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d1bc-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d1bc-110">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4d1bc-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4d1bc-111">**Строковое** значение, указывающее URL-адрес элемента, добавляемого в папку **"Избранное"** .</span><span class="sxs-lookup"><span data-stu-id="4d1bc-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="4d1bc-112">*втитле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4d1bc-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d1bc-113">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="4d1bc-113">Type: \**Variant\** _</span></span>

<span data-ttu-id="4d1bc-114">Значение _ \*Variant\*\*, указывающее имя элемента.</span><span class="sxs-lookup"><span data-stu-id="4d1bc-114">A _ *Variant*\* value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4d1bc-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="4d1bc-115">Examples</span></span>

<span data-ttu-id="4d1bc-116">В следующем примере показано правильное использование этого метода для JScript Embedded в HTML и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4d1bc-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="4d1bc-117">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="4d1bc-117">JScript:</span></span>


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



<span data-ttu-id="4d1bc-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4d1bc-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4d1bc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4d1bc-119">Requirements</span></span>



| <span data-ttu-id="4d1bc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4d1bc-120">Requirement</span></span> | <span data-ttu-id="4d1bc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4d1bc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1bc-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d1bc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4d1bc-123">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4d1bc-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4d1bc-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d1bc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4d1bc-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4d1bc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4d1bc-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4d1bc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d1bc-127"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d1bc-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="4d1bc-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4d1bc-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d1bc-129"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="4d1bc-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
