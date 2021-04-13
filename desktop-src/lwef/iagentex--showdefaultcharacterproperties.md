---
title: Иажентекс Шовдефаултчарактерпропертиес
description: Иажентекс Шовдефаултчарактерпропертиес
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487692"
---
# <a name="iagentexshowdefaultcharacterproperties"></a><span data-ttu-id="4a346-103">Иажентекс:: Шовдефаултчарактерпропертиес</span><span class="sxs-lookup"><span data-stu-id="4a346-103">IAgentEx::ShowDefaultCharacterProperties</span></span>

<span data-ttu-id="4a346-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a346-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

<span data-ttu-id="4a346-105">Отображает окно свойств символов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4a346-105">Displays default character properties window.</span></span>

-   <span data-ttu-id="4a346-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4a346-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4a346-107"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="4a346-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="4a346-108">Координата x окна в пикселях относительно начала координат экрана (вверху слева).</span><span class="sxs-lookup"><span data-stu-id="4a346-108">The x-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="4a346-109"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="4a346-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="4a346-110">Координата по оси y окна в пикселях относительно начала координат экрана (вверху слева).</span><span class="sxs-lookup"><span data-stu-id="4a346-110">The y-coordinate of the window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="4a346-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*буседефаулт*</span><span class="sxs-lookup"><span data-stu-id="4a346-111"><span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*</span></span>
</dt> <dd>

<span data-ttu-id="4a346-112">Флаг расположения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4a346-112">Default position flag.</span></span> <span data-ttu-id="4a346-113">Если этот параметр имеет **значение true**, то Microsoft Agent отображает окно страницы свойств для символа по умолчанию в последнем расположении.</span><span class="sxs-lookup"><span data-stu-id="4a346-113">If this parameter is **True**, Microsoft Agent displays the property sheet window for the default character at the last location it appeared.</span></span>

> [!Note]  
> <span data-ttu-id="4a346-114">Для Windows 2000 может потребоваться вызвать новый API [**алловсетфореграундвиндов**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) , чтобы это окно стало передним планом.</span><span class="sxs-lookup"><span data-stu-id="4a346-114">For Windows 2000, it may be necessary to call the new [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) API to ensure that this window becomes the foreground window.</span></span> <span data-ttu-id="4a346-115">Дополнительные сведения о настройке окна переднего плана в Windows 2000 см. в документации по пакету SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="4a346-115">For more information about setting the foreground window under Windows 2000, see the Platform SDK documentation.</span></span>

 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="4a346-116">См. также:</span><span class="sxs-lookup"><span data-stu-id="4a346-116">See Also</span></span>

[<span data-ttu-id="4a346-117">**Иажентнотифисинкекс::D Ефаултчарактерчанже**</span><span class="sxs-lookup"><span data-stu-id="4a346-117">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 