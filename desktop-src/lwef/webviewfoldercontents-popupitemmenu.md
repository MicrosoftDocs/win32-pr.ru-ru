---
title: Вебвиевфолдерконтентс. Попупитеммену, метод (Шлдисп. h)
description: Создает контекстное меню для указанного элемента и возвращает выбранную командную строку.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Устаревшие функции среды Windows в методе Попупитеммену
- Метод Попупитеммену устаревшие функции среды Windows, объект Вебвиевфолдерконтентс
- Устаревшие функции среды Windows для объекта Вебвиевфолдерконтентс, метод Попупитеммену
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801246"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="4f94f-106">Вебвиевфолдерконтентс. Попупитеммену, метод</span><span class="sxs-lookup"><span data-stu-id="4f94f-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="4f94f-107">Создает контекстное меню для указанного элемента и возвращает выбранную командную строку.</span><span class="sxs-lookup"><span data-stu-id="4f94f-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f94f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f94f-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="4f94f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f94f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f94f-110">*витем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f94f-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f94f-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4f94f-111">Type: **Variant**</span></span>

<span data-ttu-id="4f94f-112">Объект [**FolderItem**](../shell/folderitem.md) , для которого будет создано контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="4f94f-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="4f94f-113">*VX* \[ в, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="4f94f-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f94f-114">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4f94f-114">Type: **Variant**</span></span>

<span data-ttu-id="4f94f-115">Горизонтальное расположение меню в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="4f94f-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="4f94f-116">*Ви* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4f94f-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f94f-117">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="4f94f-117">Type: **Variant**</span></span>

<span data-ttu-id="4f94f-118">Вертикальное расположение меню в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="4f94f-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f94f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f94f-119">Return value</span></span>

<span data-ttu-id="4f94f-120">Тип: \**[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="4f94f-120">Type: \**[BSTR](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="4f94f-121">При возврате из этого метода содержит командную строку.</span><span class="sxs-lookup"><span data-stu-id="4f94f-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="4f94f-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="4f94f-122">Examples</span></span>

<span data-ttu-id="4f94f-123">В следующем примере показано правильное использование _ *попупитеммену*\* для JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="4f94f-123">The following example shows the proper use of _ *PopupItemMenu*\* for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
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



## <a name="requirements"></a><span data-ttu-id="4f94f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4f94f-124">Requirements</span></span>



| <span data-ttu-id="4f94f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4f94f-125">Requirement</span></span> | <span data-ttu-id="4f94f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4f94f-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f94f-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f94f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4f94f-128">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4f94f-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4f94f-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f94f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4f94f-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4f94f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4f94f-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4f94f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f94f-132"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f94f-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4f94f-133">IDL</span><span class="sxs-lookup"><span data-stu-id="4f94f-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4f94f-134"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f94f-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4f94f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4f94f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f94f-136"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="4f94f-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

