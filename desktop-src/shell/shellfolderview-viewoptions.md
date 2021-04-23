---
description: Возвращает набор флагов, указывающих текущие параметры представления.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: Свойство Шеллфолдервиев. Виевоптионс (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997863"
---
# <a name="shellfolderviewviewoptions-property"></a><span data-ttu-id="c2e32-103">Шеллфолдервиев. Виевоптионс, свойство</span><span class="sxs-lookup"><span data-stu-id="c2e32-103">ShellFolderView.ViewOptions property</span></span>

<span data-ttu-id="c2e32-104">Возвращает набор флагов, указывающих текущие параметры представления.</span><span class="sxs-lookup"><span data-stu-id="c2e32-104">Gets a set of flags that indicate the current options of the view.</span></span>

<span data-ttu-id="c2e32-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c2e32-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e32-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2e32-106">Syntax</span></span>


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="c2e32-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c2e32-107">Property value</span></span>

<span data-ttu-id="c2e32-108">Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает объект параметров представления.</span><span class="sxs-lookup"><span data-stu-id="c2e32-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span> <span data-ttu-id="c2e32-109">Содержит одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c2e32-109">Contains one or more of the following values:</span></span>

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span data-ttu-id="c2e32-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**Сфвво \_ ШОВАЛЛОБЖЕКТС** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="c2e32-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="c2e32-111">Параметр " **Показывать все файлы** " включен.</span><span class="sxs-lookup"><span data-stu-id="c2e32-111">The **Show All Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span data-ttu-id="c2e32-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**Сфвво \_ ШОВЕКСТЕНСИОНС** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="c2e32-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="c2e32-113">Параметр **Скрыть расширения для известных типов файлов** отключен.</span><span class="sxs-lookup"><span data-stu-id="c2e32-113">The **Hide extensions for known file types** option is disabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span data-ttu-id="c2e32-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**Сфвво \_ ШОВКОМПКОЛОР** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="c2e32-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="c2e32-115">Параметр **Отображать сжатые файлы и папки с дополнительным цветом** включен.</span><span class="sxs-lookup"><span data-stu-id="c2e32-115">The **Display Compressed Files and Folders with Alternate Color** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span data-ttu-id="c2e32-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**Сфвво \_ ШОВСИСФИЛЕС** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="c2e32-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="c2e32-117">Параметр **не показывать скрытые файлы** включен.</span><span class="sxs-lookup"><span data-stu-id="c2e32-117">The **Do Not Show Hidden Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span data-ttu-id="c2e32-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**Сфвво \_ WIN95CLASSIC** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="c2e32-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO\_WIN95CLASSIC** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="c2e32-119">Включен параметр " **классический стиль** ".</span><span class="sxs-lookup"><span data-stu-id="c2e32-119">The **Classic Style** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span data-ttu-id="c2e32-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**Сфвво \_ ДАУБЛЕКЛИККИНВЕБВИЕВ** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="c2e32-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="c2e32-121">Параметр **двойной щелчок для открытия элемента** включен.</span><span class="sxs-lookup"><span data-stu-id="c2e32-121">The **Double-Click to Open an Item** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span data-ttu-id="c2e32-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**Сфвво \_ ДЕСКТОФТМЛ** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="c2e32-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="c2e32-123">Включен параметр " **Активный рабочий стол — Просмотр в виде веб-страницы** ".</span><span class="sxs-lookup"><span data-stu-id="c2e32-123">The **Active Desktop – View as Web Page** option is enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2e32-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="c2e32-124">Remarks</span></span>

<span data-ttu-id="c2e32-125">[**Фокуседитем**](shellfolderview-focuseditem.md) может быть вызван только в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="c2e32-125">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="c2e32-126">Он не будет работать при запуске на веб-странице по протоколу HTTP или UNC.</span><span class="sxs-lookup"><span data-stu-id="c2e32-126">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="c2e32-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="c2e32-127">Examples</span></span>

<span data-ttu-id="c2e32-128">В следующем примере показано правильное использование этого метода в JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="c2e32-128">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
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
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="c2e32-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c2e32-129">Requirements</span></span>



| <span data-ttu-id="c2e32-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c2e32-130">Requirement</span></span> | <span data-ttu-id="c2e32-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c2e32-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e32-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2e32-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e32-133">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c2e32-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c2e32-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2e32-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e32-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c2e32-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c2e32-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c2e32-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2e32-137"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e32-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c2e32-138">IDL</span><span class="sxs-lookup"><span data-stu-id="c2e32-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2e32-139"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2e32-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c2e32-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c2e32-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2e32-141"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e32-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
