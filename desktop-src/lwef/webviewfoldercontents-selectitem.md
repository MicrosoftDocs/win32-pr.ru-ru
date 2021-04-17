---
title: Вебвиевфолдерконтентс. Селектитем, метод (Шлдисп. h)
description: Задает состояние выбора элемента в представлении.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Устаревшие функции среды Windows в методе Селектитем
- Метод Селектитем устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Устаревшие функции среды Windows для объекта Вебвиевфолдерконтентс, метод Селектитем
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710444"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="952ef-106">Вебвиевфолдерконтентс. Селектитем, метод</span><span class="sxs-lookup"><span data-stu-id="952ef-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="952ef-107">Задает состояние выбора элемента в представлении.</span><span class="sxs-lookup"><span data-stu-id="952ef-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="952ef-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="952ef-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="952ef-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="952ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="952ef-110">*витем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="952ef-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952ef-111">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="952ef-111">Type: \**Variant\** _</span></span>

<span data-ttu-id="952ef-112">Объект [_ *FolderItem* \*](../shell/folderitem.md) , для которого будет задано состояние выбора.</span><span class="sxs-lookup"><span data-stu-id="952ef-112">The [_ *FolderItem*\*](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="952ef-113">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="952ef-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="952ef-114">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="952ef-114">Type: **Integer**</span></span>

<span data-ttu-id="952ef-115">Набор флагов, указывающих новое состояние выбора.</span><span class="sxs-lookup"><span data-stu-id="952ef-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="952ef-116">Это может быть одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="952ef-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="952ef-117"> (0)</span><span class="sxs-lookup"><span data-stu-id="952ef-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="952ef-118">Отмените выбор элемента.</span><span class="sxs-lookup"><span data-stu-id="952ef-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="952ef-119">(1)</span><span class="sxs-lookup"><span data-stu-id="952ef-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="952ef-120">Выберите элемент.</span><span class="sxs-lookup"><span data-stu-id="952ef-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="952ef-121">(3)</span><span class="sxs-lookup"><span data-stu-id="952ef-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="952ef-122">Перевести элемент в режим редактирования.</span><span class="sxs-lookup"><span data-stu-id="952ef-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="952ef-123">(4)</span><span class="sxs-lookup"><span data-stu-id="952ef-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="952ef-124">Отменить выбор всех элементов, кроме указанного.</span><span class="sxs-lookup"><span data-stu-id="952ef-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="952ef-125">(8)</span><span class="sxs-lookup"><span data-stu-id="952ef-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="952ef-126">Убедитесь, что элемент отображается в представлении.</span><span class="sxs-lookup"><span data-stu-id="952ef-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="952ef-127">(16)</span><span class="sxs-lookup"><span data-stu-id="952ef-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="952ef-128">Присвойте элементу фокус.</span><span class="sxs-lookup"><span data-stu-id="952ef-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="952ef-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="952ef-129">Return value</span></span>

<span data-ttu-id="952ef-130">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="952ef-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="952ef-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="952ef-131">Examples</span></span>

<span data-ttu-id="952ef-132">В следующем примере показано правильное использование этого метода для JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="952ef-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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



## <a name="requirements"></a><span data-ttu-id="952ef-133">Требования</span><span class="sxs-lookup"><span data-stu-id="952ef-133">Requirements</span></span>



| <span data-ttu-id="952ef-134">Требование</span><span class="sxs-lookup"><span data-stu-id="952ef-134">Requirement</span></span> | <span data-ttu-id="952ef-135">Значение</span><span class="sxs-lookup"><span data-stu-id="952ef-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="952ef-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="952ef-136">Minimum supported client</span></span><br/> | <span data-ttu-id="952ef-137">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="952ef-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="952ef-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="952ef-138">Minimum supported server</span></span><br/> | <span data-ttu-id="952ef-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="952ef-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="952ef-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="952ef-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="952ef-141"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="952ef-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="952ef-142">IDL</span><span class="sxs-lookup"><span data-stu-id="952ef-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="952ef-143"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="952ef-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="952ef-144">DLL</span><span class="sxs-lookup"><span data-stu-id="952ef-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="952ef-145"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="952ef-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

