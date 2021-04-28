---
title: Метод WebViewFolderContents.SelectedItems (Shldisp.h)
description: Вебвиевфолдерконтентс. SelectedItems, метод возвращает объект Фолдеритемс, представляющий все выбранные элементы в представлении.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Устаревшие функции среды Windows в методе SelectedItems
- Метод SelectedItems устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Устаревшие функции среды Windows для объекта Вебвиевфолдерконтентс, метод SelectedItems
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a242991f6f9472610dffa20593f9cab5d8c310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102652"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="9f0a3-106">Вебвиевфолдерконтентс. SelectedItems, метод</span><span class="sxs-lookup"><span data-stu-id="9f0a3-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="9f0a3-107">Возвращает объект [**фолдеритемс**](../shell/folderitems.md) , представляющий все выбранные элементы в представлении.</span><span class="sxs-lookup"><span data-stu-id="9f0a3-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f0a3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f0a3-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="9f0a3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f0a3-109">Parameters</span></span>

<span data-ttu-id="9f0a3-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9f0a3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f0a3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f0a3-111">Return value</span></span>

<span data-ttu-id="9f0a3-112">Тип: **[ **фолдеритемс**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9f0a3-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="9f0a3-113">Ссылка на объект [**фолдеритемс**](../shell/folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="9f0a3-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="9f0a3-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="9f0a3-114">Examples</span></span>

<span data-ttu-id="9f0a3-115">В следующем примере показано правильное использование этого метода для JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="9f0a3-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



## <a name="requirements"></a><span data-ttu-id="9f0a3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9f0a3-116">Requirements</span></span>



| <span data-ttu-id="9f0a3-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9f0a3-117">Requirement</span></span> | <span data-ttu-id="9f0a3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9f0a3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f0a3-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f0a3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9f0a3-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9f0a3-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9f0a3-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f0a3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9f0a3-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9f0a3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f0a3-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9f0a3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f0a3-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f0a3-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9f0a3-125">IDL</span><span class="sxs-lookup"><span data-stu-id="9f0a3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f0a3-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f0a3-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9f0a3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9f0a3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f0a3-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="9f0a3-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

