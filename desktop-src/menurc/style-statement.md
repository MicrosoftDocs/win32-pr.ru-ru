---
title: Оператор STYLE
description: Определяет стиль окна для диалогового окна. Стиль окна определяет, является ли поле всплывающим или дочерним окном.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Меню инструкций стилей и другие ресурсы
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412901"
---
# <a name="style-statement"></a><span data-ttu-id="5a278-105">Оператор STYLE</span><span class="sxs-lookup"><span data-stu-id="5a278-105">STYLE statement</span></span>

<span data-ttu-id="5a278-106">Определяет стиль окна для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5a278-106">Defines the window style of the dialog box.</span></span> <span data-ttu-id="5a278-107">Стиль окна определяет, является ли поле всплывающим или дочерним окном.</span><span class="sxs-lookup"><span data-stu-id="5a278-107">The window style specifies whether the box is a pop-up or a child window.</span></span>

``` syntax
STYLE style
```

<dl> <dt>

<span data-ttu-id="5a278-108"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="5a278-108"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="5a278-109">Стиль окна.</span><span class="sxs-lookup"><span data-stu-id="5a278-109">The window style.</span></span> <span data-ttu-id="5a278-110">Этот параметр может быть целым числом или сочетанием значений стиля окна (например, **WS \_ Caption** и **WS \_ сисмену**) и значениями стиля диалогового окна (например, **\_ центра DS**).</span><span class="sxs-lookup"><span data-stu-id="5a278-110">This parameter can be an integer value or a combination of window style values (such as **WS\_CAPTION** and **WS\_SYSMENU**) and dialog box style values (such as **DS\_CENTER**).</span></span>

</dd> </dl>

<span data-ttu-id="5a278-111">Список стилей окна см. в разделе [стили окон](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="5a278-111">For a list of window styles, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span> <span data-ttu-id="5a278-112">Список стилей диалоговых окон см. в разделе [стили шаблонов диалоговых окон](../dlgbox/about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="5a278-112">For a list of dialog box styles, see [Dialog Box Template Styles](../dlgbox/about-dialog-boxes.md).</span></span> <span data-ttu-id="5a278-113">При использовании значений стиля окна или диалогового окна необходимо включить Windows. h.</span><span class="sxs-lookup"><span data-stu-id="5a278-113">If you use the window or dialog box style values, you must include Windows.h.</span></span>

 

 