---
description: Указывает, подписан ли указанный URL-адрес на.
title: Метод Шеллуихелпер. Subscribe (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.IsSubscribed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: fcf23352-6603-4b17-9c3b-b353cca1c003
ms.openlocfilehash: 2085f38e5f91f13a2f67ff4f22b003b533249386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080947"
---
# <a name="shelluihelperissubscribed-method"></a><span data-ttu-id="25672-103">Шеллуихелпер. подписавший метод</span><span class="sxs-lookup"><span data-stu-id="25672-103">ShellUIHelper.IsSubscribed method</span></span>

<span data-ttu-id="25672-104">Указывает, подписан ли указанный URL-адрес на.</span><span class="sxs-lookup"><span data-stu-id="25672-104">Indicates whether a specified URL is subscribed to.</span></span>

## <a name="syntax"></a><span data-ttu-id="25672-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25672-105">Syntax</span></span>


```JScript
bRetVal = ShellUIHelper.IsSubscribed(
  sURL
)
```



## <a name="parameters"></a><span data-ttu-id="25672-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25672-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25672-107">*СУРЛ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25672-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25672-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="25672-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="25672-109">**Строковое** значение, указывающее URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="25672-109">A **String** value that specifies the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25672-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25672-110">Return value</span></span>

<span data-ttu-id="25672-111">Тип: \**Boolean \** _</span><span class="sxs-lookup"><span data-stu-id="25672-111">Type: \**Boolean\** _</span></span>

<span data-ttu-id="25672-112">_ *true*\* при наличии подписки на URL-адрес; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="25672-112">_ *true*\* if the URL is subscribed to; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="25672-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="25672-113">Examples</span></span>

<span data-ttu-id="25672-114">В следующем примере показано правильное использование этого метода для JScript Embedded в HTML и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="25672-114">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="25672-115">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="25672-115">JScript:</span></span>


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
    function fnShellUIHelperIsSubscribedJ()
    {
        var bReturn;
        
        bReturn = ShellUIHelper.IsSubscribed("https://www.microsoft.com/");
        alert(bReturn);
    }
</script>

</head>
<body onload=fnShellUIHelperIsSubscribedJ()>
</body>
</html>
```



<span data-ttu-id="25672-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="25672-116">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperIsSubscribedVB()
    Dim objShellUIHelper As ShellUIHelper
    Dim bReturn          As Boolean
    
    Set objShellUIHelper = New ShellUIHelper
        bReturn = objShellUIHelper.IsSubscribed("https://www.microsoft.com/")
        Debug.Print bReturn
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="25672-117">Требования</span><span class="sxs-lookup"><span data-stu-id="25672-117">Requirements</span></span>



| <span data-ttu-id="25672-118">Требование</span><span class="sxs-lookup"><span data-stu-id="25672-118">Requirement</span></span> | <span data-ttu-id="25672-119">Значение</span><span class="sxs-lookup"><span data-stu-id="25672-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25672-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25672-120">Minimum supported client</span></span><br/> | <span data-ttu-id="25672-121">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="25672-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="25672-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25672-122">Minimum supported server</span></span><br/> | <span data-ttu-id="25672-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="25672-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="25672-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="25672-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="25672-125"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="25672-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="25672-126">DLL</span><span class="sxs-lookup"><span data-stu-id="25672-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25672-127"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="25672-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
