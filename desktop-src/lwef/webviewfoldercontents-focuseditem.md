---
title: Свойство Вебвиевфолдерконтентс. Фокуседитем (Шлдисп. h)
description: Вебвиевфолдерконтентс. Фокуседитем Property — возвращает объект FolderItem, представляющий элемент, имеющий фокус ввода.
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Свойства Фокуседитем устаревшие функции среды Windows
- Свойства Фокуседитем устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Функции среды Windows для устаревшего объекта Вебвиевфолдерконтентс, свойство Фокуседитем
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724743b81f605dc9ba5794a4a796b8a0c4a2a03f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102732"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a><span data-ttu-id="52067-106">Вебвиевфолдерконтентс. Фокуседитем, свойство</span><span class="sxs-lookup"><span data-stu-id="52067-106">WebViewFolderContents.FocusedItem property</span></span>

<span data-ttu-id="52067-107">Возвращает объект [**FolderItem**](../shell/folderitem.md) , представляющий элемент, имеющий фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="52067-107">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="52067-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="52067-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52067-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52067-109">Syntax</span></span>


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="52067-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="52067-110">Property value</span></span>

<span data-ttu-id="52067-111">Переменная типа [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , получающая объект элемента с сортировкой.</span><span class="sxs-lookup"><span data-stu-id="52067-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="examples"></a><span data-ttu-id="52067-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="52067-112">Examples</span></span>

<span data-ttu-id="52067-113">В следующем примере показано правильное использование этого свойства в JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="52067-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
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



## <a name="requirements"></a><span data-ttu-id="52067-114">Требования</span><span class="sxs-lookup"><span data-stu-id="52067-114">Requirements</span></span>



| <span data-ttu-id="52067-115">Требование</span><span class="sxs-lookup"><span data-stu-id="52067-115">Requirement</span></span> | <span data-ttu-id="52067-116">Значение</span><span class="sxs-lookup"><span data-stu-id="52067-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52067-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="52067-117">Minimum supported client</span></span><br/> | <span data-ttu-id="52067-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="52067-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="52067-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="52067-119">Minimum supported server</span></span><br/> | <span data-ttu-id="52067-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="52067-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="52067-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="52067-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="52067-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="52067-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="52067-123">IDL</span><span class="sxs-lookup"><span data-stu-id="52067-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52067-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="52067-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="52067-125">DLL</span><span class="sxs-lookup"><span data-stu-id="52067-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52067-126"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="52067-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

