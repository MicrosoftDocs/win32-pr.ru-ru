---
description: Добавляет элемент в Microsoft Active Desktop.
title: Шеллуихелпер. Адддесктопкомпонент, метод (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: d5234a0b43ea25c8ac931dc14ec90f7a6696ddfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985956"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="53d0c-103">Шеллуихелпер. Адддесктопкомпонент, метод</span><span class="sxs-lookup"><span data-stu-id="53d0c-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="53d0c-104">Добавляет элемент в Microsoft Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="53d0c-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d0c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53d0c-105">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a><span data-ttu-id="53d0c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53d0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53d0c-107">*СУРЛ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53d0c-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d0c-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="53d0c-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="53d0c-109">**Строковое** значение, указывающее URL-адрес нового элемента избранного.</span><span class="sxs-lookup"><span data-stu-id="53d0c-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="53d0c-110">*Стипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53d0c-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53d0c-111">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="53d0c-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="53d0c-112">**Строковое** значение, указывающее тип добавляемого элемента.</span><span class="sxs-lookup"><span data-stu-id="53d0c-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="53d0c-113">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="53d0c-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="53d0c-114">Эскиз</span><span class="sxs-lookup"><span data-stu-id="53d0c-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="53d0c-115">Компонент является изображением.</span><span class="sxs-lookup"><span data-stu-id="53d0c-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="53d0c-116">веб</span><span class="sxs-lookup"><span data-stu-id="53d0c-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="53d0c-117">Компонент является веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="53d0c-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="53d0c-118">По *левому краю* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="53d0c-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53d0c-119">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="53d0c-119">Type: **Variant**</span></span>

<span data-ttu-id="53d0c-120">Расположение левого края компонента в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="53d0c-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="53d0c-121">В *Начало* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="53d0c-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53d0c-122">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="53d0c-122">Type: **Variant**</span></span>

<span data-ttu-id="53d0c-123">Расположение верхнего края компонента в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="53d0c-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="53d0c-124">*Ширина* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="53d0c-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53d0c-125">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="53d0c-125">Type: **Variant**</span></span>

<span data-ttu-id="53d0c-126">Ширина компонента в единицах экрана.</span><span class="sxs-lookup"><span data-stu-id="53d0c-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="53d0c-127">*Высота* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="53d0c-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53d0c-128">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="53d0c-128">Type: **Variant**</span></span>

<span data-ttu-id="53d0c-129">Высота компонента в единицах экрана.</span><span class="sxs-lookup"><span data-stu-id="53d0c-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="53d0c-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="53d0c-130">Examples</span></span>

<span data-ttu-id="53d0c-131">В следующем примере показано правильное использование этого метода для JScript Embedded в HTML и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="53d0c-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="53d0c-132">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="53d0c-132">JScript:</span></span>


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
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



<span data-ttu-id="53d0c-133">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="53d0c-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="53d0c-134">Требования</span><span class="sxs-lookup"><span data-stu-id="53d0c-134">Requirements</span></span>



| <span data-ttu-id="53d0c-135">Требование</span><span class="sxs-lookup"><span data-stu-id="53d0c-135">Requirement</span></span> | <span data-ttu-id="53d0c-136">Значение</span><span class="sxs-lookup"><span data-stu-id="53d0c-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53d0c-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53d0c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="53d0c-138">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="53d0c-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="53d0c-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53d0c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="53d0c-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53d0c-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53d0c-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="53d0c-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="53d0c-142"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="53d0c-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="53d0c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="53d0c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53d0c-144"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="53d0c-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
