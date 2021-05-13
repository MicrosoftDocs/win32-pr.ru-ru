---
description: Добавляет новый канал в список каналов в меню Избранное Windows Internet Explorer и на панель каналов на рабочем столе.
title: Шеллуихелпер. Аддчаннел, метод (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: d08c1360cb2a96fbc7b87daecb650bbf46aa6ad9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841205"
---
# <a name="shelluihelperaddchannel-method"></a><span data-ttu-id="23662-103">Шеллуихелпер. Аддчаннел, метод</span><span class="sxs-lookup"><span data-stu-id="23662-103">ShellUIHelper.AddChannel method</span></span>

<span data-ttu-id="23662-104">Добавляет новый канал в список каналов в меню **Избранное** Windows Internet Explorer и на панель **каналов** на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="23662-104">Adds a new channel to the list of channels in the Windows Internet Explorer **Favorites** menu and to the **Channel** bar on the desktop.</span></span>

> [!Note]  
> <span data-ttu-id="23662-105">Этот метод больше не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="23662-105">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="23662-106">В этой операционной системе возвращается E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="23662-106">Under that operating system, it returns E\_NOTIMPL.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="23662-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23662-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="23662-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="23662-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23662-109">*СУРЛ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23662-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23662-110">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="23662-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="23662-111">**Строковое** значение, указывающее URL-адрес файла CDF.</span><span class="sxs-lookup"><span data-stu-id="23662-111">A **String** value that specifies the URL of the CDF file.</span></span>

> [!Note]  
> <span data-ttu-id="23662-112">Ссылки в файле CDF должны использовать протоколы HTTP, HTTPS или FTP.</span><span class="sxs-lookup"><span data-stu-id="23662-112">The links in the CDF file must use HTTP, HTTPS, or FTP protocols.</span></span> <span data-ttu-id="23662-113">Если в файле CDF содержится любой другой протокол, добавление канала завершается сбоем и диалоговое окно не появляется.</span><span class="sxs-lookup"><span data-stu-id="23662-113">If the CDF file contains any other protocol, the addition of the channel fails and no dialog box appears.</span></span>

 

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="23662-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="23662-114">Examples</span></span>

<span data-ttu-id="23662-115">В следующем примере показано правильное использование этого метода для JScript Embedded в HTML и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="23662-115">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="23662-116">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="23662-116">JScript:</span></span>


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
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



<span data-ttu-id="23662-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="23662-117">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="23662-118">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="23662-118">Requirements</span></span>



| <span data-ttu-id="23662-119">Требование</span><span class="sxs-lookup"><span data-stu-id="23662-119">Requirement</span></span> | <span data-ttu-id="23662-120">Значение</span><span class="sxs-lookup"><span data-stu-id="23662-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23662-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23662-121">Minimum supported client</span></span><br/> | <span data-ttu-id="23662-122">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="23662-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="23662-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23662-123">Minimum supported server</span></span><br/> | <span data-ttu-id="23662-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="23662-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="23662-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="23662-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="23662-126"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="23662-126"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="23662-127">DLL</span><span class="sxs-lookup"><span data-stu-id="23662-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23662-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="23662-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
