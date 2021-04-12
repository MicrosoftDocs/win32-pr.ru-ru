---
title: Аутопопупмену, свойство
description: Аутопопупмену, свойство
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331531"
---
# <a name="autopopupmenu-property"></a><span data-ttu-id="a1543-103">Аутопопупмену, свойство</span><span class="sxs-lookup"><span data-stu-id="a1543-103">AutoPopupMenu Property</span></span>

<span data-ttu-id="a1543-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a1543-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a1543-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="a1543-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a1543-106">Возвращает или задает значение, указывающее, отображается ли всплывающее меню символа при щелчке символа правой кнопкой мыши или его значка на панели задач.</span><span class="sxs-lookup"><span data-stu-id="a1543-106">Returns or sets whether right-clicking the character or its taskbar icon automatically displays the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="a1543-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="a1543-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a1543-108">\*агент. ***Символы \* \* \* \* ("*** чарактерид \* \* *"). Аутопопупмену* \*  \[  =  *Boolean*\]</span><span class="sxs-lookup"><span data-stu-id="a1543-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").AutoPopupMenu** \[ = *boolean*\]</span></span>



| <span data-ttu-id="a1543-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="a1543-109">Part</span></span>      | <span data-ttu-id="a1543-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a1543-110">Description</span></span>                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1543-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="a1543-111">*boolean*</span></span> | <span data-ttu-id="a1543-112">Логическое выражение, указывающее, будет ли сервер автоматически отображать всплывающее меню символа щелчком правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="a1543-112">A Boolean expression specifying whether the server automatically displays the character's pop-up menu on right-click.</span></span> <span data-ttu-id="a1543-113">**True** (по умолчанию) — отображение меню щелчком правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="a1543-113">**True** (Default) Displays the menu on right-click.</span></span> <br/> <span data-ttu-id="a1543-114">**Значение false** Не отображает меню щелчком правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="a1543-114">**False** Does not display the menu on right-click.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1543-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1543-115">Remarks</span></span>

<span data-ttu-id="a1543-116">Если задать для этого свойства **значение false**, можно создать собственное поведение при обработке меню.</span><span class="sxs-lookup"><span data-stu-id="a1543-116">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="a1543-117">Чтобы отобразить меню после присвоения этому свойству значения **false**, используйте метод [**шовпопупмену**](showpopupmenu-method.md) .</span><span class="sxs-lookup"><span data-stu-id="a1543-117">To display the menu after setting this property to **False**, use the [**ShowPopupMenu**](showpopupmenu-method.md) method.</span></span>

<span data-ttu-id="a1543-118">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="a1543-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1543-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="a1543-119">See Also</span></span>

[<span data-ttu-id="a1543-120">**Метод Шовпопупмену**</span><span class="sxs-lookup"><span data-stu-id="a1543-120">**ShowPopupMenu method**</span></span>](showpopupmenu-method.md)


 

 





