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
ms.openlocfilehash: 93c62abd8f788f950e36bcfc5fa10f7c991a6410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997938"
---
# <a name="shelluihelperaddchannel-method"></a><span data-ttu-id="26c1d-103">Шеллуихелпер. Аддчаннел, метод</span><span class="sxs-lookup"><span data-stu-id="26c1d-103">ShellUIHelper.AddChannel method</span></span>

<span data-ttu-id="26c1d-104">Добавляет новый канал в список каналов в меню **Избранное** Windows Internet Explorer и на панель **каналов** на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="26c1d-104">Adds a new channel to the list of channels in the Windows Internet Explorer **Favorites** menu and to the **Channel** bar on the desktop.</span></span>

> [!Note]  
> <span data-ttu-id="26c1d-105">Этот метод больше не поддерживается в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="26c1d-105">This method is no longer supported under Windows Vista.</span></span> <span data-ttu-id="26c1d-106">В этой операционной системе возвращается E \_ нотимпл.</span><span class="sxs-lookup"><span data-stu-id="26c1d-106">Under that operating system, it returns E\_NOTIMPL.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="26c1d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26c1d-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="26c1d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="26c1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26c1d-109">*СУРЛ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="26c1d-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26c1d-110">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="26c1d-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="26c1d-111">**Строковое** значение, указывающее URL-адрес файла CDF.</span><span class="sxs-lookup"><span data-stu-id="26c1d-111">A **String** value that specifies the URL of the CDF file.</span></span>

> [!Note]  
> <span data-ttu-id="26c1d-112">Ссылки в файле CDF должны использовать протоколы HTTP, HTTPS или FTP.</span><span class="sxs-lookup"><span data-stu-id="26c1d-112">The links in the CDF file must use HTTP, HTTPS, or FTP protocols.</span></span> <span data-ttu-id="26c1d-113">Если в файле CDF содержится любой другой протокол, добавление канала завершается сбоем и диалоговое окно не появляется.</span><span class="sxs-lookup"><span data-stu-id="26c1d-113">If the CDF file contains any other protocol, the addition of the channel fails and no dialog box appears.</span></span>

 

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="26c1d-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="26c1d-114">Examples</span></span>

<span data-ttu-id="26c1d-115">В следующем примере показано правильное использование этого метода для JScript Embedded в HTML и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="26c1d-115">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="26c1d-116">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="26c1d-116">JScript:</span></span>


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



<span data-ttu-id="26c1d-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="26c1d-117">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="26c1d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="26c1d-118">Requirements</span></span>



| <span data-ttu-id="26c1d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="26c1d-119">Requirement</span></span> | <span data-ttu-id="26c1d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="26c1d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26c1d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26c1d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26c1d-122">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="26c1d-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="26c1d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26c1d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26c1d-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="26c1d-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="26c1d-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="26c1d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26c1d-126"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="26c1d-126"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="26c1d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="26c1d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26c1d-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="26c1d-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
