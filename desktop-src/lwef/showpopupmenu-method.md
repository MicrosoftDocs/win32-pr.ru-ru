---
title: Метод Шовпопупмену
description: Метод Шовпопупмену
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700489"
---
# <a name="showpopupmenu-method"></a><span data-ttu-id="80548-103">Метод Шовпопупмену</span><span class="sxs-lookup"><span data-stu-id="80548-103">ShowPopupMenu Method</span></span>

<span data-ttu-id="80548-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="80548-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="80548-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="80548-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="80548-106">Отображает всплывающее меню символа в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="80548-106">Displays the character's pop-up menu at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="80548-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="80548-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="80548-108">*Субагент. ***Символы ("*** чарактерид ***"). Шовпопупмену*** x, y*</span><span class="sxs-lookup"><span data-stu-id="80548-108">*agent.\*\*\*Characters("*\*\* CharacterID ***").ShowPopupMenu*** x, y\*</span></span>



| <span data-ttu-id="80548-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="80548-109">Part</span></span> | <span data-ttu-id="80548-110">Описание</span><span class="sxs-lookup"><span data-stu-id="80548-110">Description</span></span>                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80548-111">*x*</span><span class="sxs-lookup"><span data-stu-id="80548-111">*x*</span></span>  | <span data-ttu-id="80548-112">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="80548-112">Required.</span></span> <span data-ttu-id="80548-113">Целочисленное значение, указывающее горизонтальную (*x*) координату экрана для отображения меню.</span><span class="sxs-lookup"><span data-stu-id="80548-113">An integer value that indicates the horizontal (*x*) screen coordinate to display the menu.</span></span> <span data-ttu-id="80548-114">Эти координаты должны быть указаны в пикселях.</span><span class="sxs-lookup"><span data-stu-id="80548-114">These coordinates must be specified in pixels.</span></span> |
| <span data-ttu-id="80548-115">*y*</span><span class="sxs-lookup"><span data-stu-id="80548-115">*y*</span></span>  | <span data-ttu-id="80548-116">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="80548-116">Required.</span></span> <span data-ttu-id="80548-117">Целочисленное значение, указывающее координату вертикального экрана (*y*) для отображения меню.</span><span class="sxs-lookup"><span data-stu-id="80548-117">An integer value that indicates the vertical (*y*) screen coordinate to display the menu.</span></span> <span data-ttu-id="80548-118">Эти координаты должны быть указаны в пикселях.</span><span class="sxs-lookup"><span data-stu-id="80548-118">These coordinates must be specified in pixels.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80548-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80548-119">Remarks</span></span>

<span data-ttu-id="80548-120">Агент автоматически отображает всплывающее меню символа, когда пользователь щелкает правой кнопкой мыши символ.</span><span class="sxs-lookup"><span data-stu-id="80548-120">Agent automatically displays the character's pop-up menu when the user right-clicks the character.</span></span> <span data-ttu-id="80548-121">Если для [**аутопопупмену**](autopopupmenu-property.md) задано **значение false**, можно использовать этот метод для вывода меню.</span><span class="sxs-lookup"><span data-stu-id="80548-121">If you set [**AutoPopupMenu**](autopopupmenu-property.md) to **False**, you can use this method to display the menu.</span></span>

<span data-ttu-id="80548-122">Меню остается отображаемым до тех пор, пока пользователь не выберет команду или не отобразит другое меню.</span><span class="sxs-lookup"><span data-stu-id="80548-122">The menu remains displayed until the user selects a command or displays another menu.</span></span> <span data-ttu-id="80548-123">В каждый момент времени может отображаться только одно всплывающее меню; Поэтому вызовы этого метода будут отменяться (удалить) из предыдущего меню.</span><span class="sxs-lookup"><span data-stu-id="80548-123">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="80548-124">Этот метод следует вызывать только в том случае, если клиентское приложение является активным клиентом символа. в противном случае произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="80548-124">This method should be called only when your client application is the active client of the character; otherwise it fails.</span></span> <span data-ttu-id="80548-125">Чтобы определить успешность этого метода, можно вызвать его как функцию, и она возвратит логическое значение, указывающее, успешно ли выполнен метод.</span><span class="sxs-lookup"><span data-stu-id="80548-125">To determine the success of this method you can call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a><span data-ttu-id="80548-126">См. также:</span><span class="sxs-lookup"><span data-stu-id="80548-126">See Also</span></span>

[<span data-ttu-id="80548-127">**Аутопопупмену, свойство**</span><span class="sxs-lookup"><span data-stu-id="80548-127">**AutoPopupMenu property**</span></span>](autopopupmenu-property.md)


 

 




