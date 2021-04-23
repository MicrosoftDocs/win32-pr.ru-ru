---
title: Свойство WebViewFolderContents.Folder (Shldisp.h)
description: Возвращает объект Folder, представляющий представление.
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Свойства папки устаревшие возможности среды Windows
- Свойство папки устаревшие компоненты среды Windows, объект Вебвиевфолдерконтентс
- Объекты Вебвиевфолдерконтентс устаревшие компоненты среды Windows, свойство Folder
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0640d4e29b903b32a6c9ed1e0b1de9f458b132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489315"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="875a6-106">Вебвиевфолдерконтентс. Folder, свойство</span><span class="sxs-lookup"><span data-stu-id="875a6-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="875a6-107">Возвращает объект [**Folder**](../shell/folder.md) , представляющий представление.</span><span class="sxs-lookup"><span data-stu-id="875a6-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="875a6-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="875a6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="875a6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="875a6-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="875a6-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="875a6-110">Property value</span></span>

<span data-ttu-id="875a6-111">Объект, получающий объект [**Folder**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="875a6-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="875a6-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="875a6-112">Examples</span></span>

<span data-ttu-id="875a6-113">В следующем примере показано правильное использование этого свойства в JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="875a6-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
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



## <a name="requirements"></a><span data-ttu-id="875a6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="875a6-114">Requirements</span></span>



| <span data-ttu-id="875a6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="875a6-115">Requirement</span></span> | <span data-ttu-id="875a6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="875a6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="875a6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="875a6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="875a6-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="875a6-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="875a6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="875a6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="875a6-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="875a6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="875a6-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="875a6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="875a6-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="875a6-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="875a6-123">IDL</span><span class="sxs-lookup"><span data-stu-id="875a6-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="875a6-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="875a6-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="875a6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="875a6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="875a6-126"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="875a6-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

