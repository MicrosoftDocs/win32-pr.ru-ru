---
title: Свойство Вебвиевфолдерконтентс. Виевоптионс (Шлдисп. h)
description: Возвращает набор флагов Шеллфолдервиевоптионс, которые указывают текущие параметры представления.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Свойства Виевоптионс устаревшие функции среды Windows
- Свойства Виевоптионс устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Функции среды Windows для устаревшего объекта Вебвиевфолдерконтентс, свойство Виевоптионс
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071210"
---
# <a name="webviewfoldercontentsviewoptions-property"></a><span data-ttu-id="f2482-106">Вебвиевфолдерконтентс. Виевоптионс, свойство</span><span class="sxs-lookup"><span data-stu-id="f2482-106">WebViewFolderContents.ViewOptions property</span></span>

<span data-ttu-id="f2482-107">Возвращает набор флагов [**шеллфолдервиевоптионс**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) , которые указывают текущие параметры представления.</span><span class="sxs-lookup"><span data-stu-id="f2482-107">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span>

<span data-ttu-id="f2482-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f2482-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2482-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2482-109">Syntax</span></span>


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="f2482-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2482-110">Property value</span></span>

<span data-ttu-id="f2482-111">Переменная типа [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , которая получает объект параметров представления.</span><span class="sxs-lookup"><span data-stu-id="f2482-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span>

## <a name="examples"></a><span data-ttu-id="f2482-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="f2482-112">Examples</span></span>

<span data-ttu-id="f2482-113">В следующем примере показано правильное использование этого свойства в JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="f2482-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



## <a name="requirements"></a><span data-ttu-id="f2482-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f2482-114">Requirements</span></span>



| <span data-ttu-id="f2482-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f2482-115">Requirement</span></span> | <span data-ttu-id="f2482-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f2482-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2482-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2482-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f2482-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2482-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f2482-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2482-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f2482-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f2482-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f2482-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f2482-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2482-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2482-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f2482-123">IDL</span><span class="sxs-lookup"><span data-stu-id="f2482-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2482-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2482-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f2482-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f2482-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2482-126"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="f2482-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

