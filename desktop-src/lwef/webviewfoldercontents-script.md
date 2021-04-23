---
title: Свойство Вебвиевфолдерконтентс. script (Шлдисп. h)
description: Возвращает объект скрипта для представления.
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- Свойства скрипта устаревшие возможности среды Windows
- Свойство скрипта устаревшие компоненты среды Windows, объект Вебвиевфолдерконтентс
- Устаревшие компоненты среды Windows для объекта Вебвиевфолдерконтентс, свойство script
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92133278d73851fa43353c116a2385da9b0fd3da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691912"
---
# <a name="webviewfoldercontentsscript-property"></a><span data-ttu-id="b9a2b-106">Вебвиевфолдерконтентс. script, свойство</span><span class="sxs-lookup"><span data-stu-id="b9a2b-106">WebViewFolderContents.Script property</span></span>

<span data-ttu-id="b9a2b-107">Возвращает объект скрипта для представления.</span><span class="sxs-lookup"><span data-stu-id="b9a2b-107">Gets the scripting object for the view.</span></span>

<span data-ttu-id="b9a2b-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b9a2b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9a2b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9a2b-109">Syntax</span></span>


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a><span data-ttu-id="b9a2b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b9a2b-110">Property value</span></span>

<span data-ttu-id="b9a2b-111">Переменная типа [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , которая получает объект скрипта.</span><span class="sxs-lookup"><span data-stu-id="b9a2b-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the scripting object.</span></span>

## <a name="examples"></a><span data-ttu-id="b9a2b-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="b9a2b-112">Examples</span></span>

<span data-ttu-id="b9a2b-113">В следующем примере показано правильное использование этого свойства в JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="b9a2b-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="b9a2b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b9a2b-114">Requirements</span></span>



| <span data-ttu-id="b9a2b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b9a2b-115">Requirement</span></span> | <span data-ttu-id="b9a2b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b9a2b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a2b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9a2b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a2b-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b9a2b-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b9a2b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9a2b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a2b-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9a2b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b9a2b-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b9a2b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9a2b-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9a2b-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b9a2b-123">IDL</span><span class="sxs-lookup"><span data-stu-id="b9a2b-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9a2b-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9a2b-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b9a2b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b9a2b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9a2b-126"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b9a2b-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

