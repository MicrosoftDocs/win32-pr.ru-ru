---
description: Задает состояние выбора элемента в представлении.
title: Шеллфолдервиев. Селектитем, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: d44633983075cdf22581bce05cfb7c073f422084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266169"
---
# <a name="shellfolderviewselectitem-method"></a><span data-ttu-id="12a16-103">Шеллфолдервиев. Селектитем, метод</span><span class="sxs-lookup"><span data-stu-id="12a16-103">ShellFolderView.SelectItem method</span></span>

<span data-ttu-id="12a16-104">Задает состояние выбора элемента в представлении.</span><span class="sxs-lookup"><span data-stu-id="12a16-104">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a16-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12a16-105">Syntax</span></span>


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="12a16-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="12a16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12a16-107">*витем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12a16-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12a16-108">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="12a16-108">Type: \**Variant\** _</span></span>

<span data-ttu-id="12a16-109">Объект [_ *FolderItem* \*](folderitem.md) , для которого будет задано состояние выбора.</span><span class="sxs-lookup"><span data-stu-id="12a16-109">The [_ *FolderItem*\*](folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="12a16-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12a16-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12a16-111">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="12a16-111">Type: **Integer**</span></span>

<span data-ttu-id="12a16-112">Набор флагов, указывающих новое состояние выбора.</span><span class="sxs-lookup"><span data-stu-id="12a16-112">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="12a16-113">Это может быть одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="12a16-113">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="12a16-114"> (0)</span><span class="sxs-lookup"><span data-stu-id="12a16-114">(0)</span></span>


</dt> <dd>

<span data-ttu-id="12a16-115">Отмените выбор элемента.</span><span class="sxs-lookup"><span data-stu-id="12a16-115">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="12a16-116">(1)</span><span class="sxs-lookup"><span data-stu-id="12a16-116">(1)</span></span>


</dt> <dd>

<span data-ttu-id="12a16-117">Выберите элемент.</span><span class="sxs-lookup"><span data-stu-id="12a16-117">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="12a16-118">(3)</span><span class="sxs-lookup"><span data-stu-id="12a16-118">(3)</span></span>


</dt> <dd>

<span data-ttu-id="12a16-119">Перевести элемент в режим редактирования.</span><span class="sxs-lookup"><span data-stu-id="12a16-119">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="12a16-120">(4)</span><span class="sxs-lookup"><span data-stu-id="12a16-120">(4)</span></span>


</dt> <dd>

<span data-ttu-id="12a16-121">Отменить выбор всех элементов, кроме указанного.</span><span class="sxs-lookup"><span data-stu-id="12a16-121">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="12a16-122">(8)</span><span class="sxs-lookup"><span data-stu-id="12a16-122">(8)</span></span>


</dt> <dd>

<span data-ttu-id="12a16-123">Убедитесь, что элемент отображается в представлении.</span><span class="sxs-lookup"><span data-stu-id="12a16-123">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="12a16-124">(16)</span><span class="sxs-lookup"><span data-stu-id="12a16-124">(16)</span></span>


</dt> <dd>

<span data-ttu-id="12a16-125">Присвойте элементу фокус.</span><span class="sxs-lookup"><span data-stu-id="12a16-125">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12a16-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12a16-126">Return value</span></span>

<span data-ttu-id="12a16-127">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="12a16-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12a16-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="12a16-128">Remarks</span></span>

<span data-ttu-id="12a16-129">[**Фокуседитем**](shellfolderview-focuseditem.md) может быть вызван только в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="12a16-129">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="12a16-130">Он не будет работать при запуске на веб-странице по протоколу HTTP или UNC.</span><span class="sxs-lookup"><span data-stu-id="12a16-130">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="12a16-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="12a16-131">Examples</span></span>

<span data-ttu-id="12a16-132">В следующем примере показано правильное использование этого метода в JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="12a16-132">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="12a16-133">Требования</span><span class="sxs-lookup"><span data-stu-id="12a16-133">Requirements</span></span>



| <span data-ttu-id="12a16-134">Требование</span><span class="sxs-lookup"><span data-stu-id="12a16-134">Requirement</span></span> | <span data-ttu-id="12a16-135">Значение</span><span class="sxs-lookup"><span data-stu-id="12a16-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12a16-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12a16-136">Minimum supported client</span></span><br/> | <span data-ttu-id="12a16-137">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="12a16-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="12a16-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12a16-138">Minimum supported server</span></span><br/> | <span data-ttu-id="12a16-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="12a16-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12a16-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="12a16-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="12a16-141"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="12a16-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="12a16-142">IDL</span><span class="sxs-lookup"><span data-stu-id="12a16-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12a16-143"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12a16-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="12a16-144">DLL</span><span class="sxs-lookup"><span data-stu-id="12a16-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12a16-145"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="12a16-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




