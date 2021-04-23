---
description: Ниже приведены некоторые общие экземпляры условных операторов. Дополнительные сведения см. в разделе Синтаксис условных инструкций.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Примеры синтаксиса условных операторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991625"
---
# <a name="examples-of-conditional-statement-syntax"></a><span data-ttu-id="e6452-104">Примеры синтаксиса условных операторов</span><span class="sxs-lookup"><span data-stu-id="e6452-104">Examples of Conditional Statement Syntax</span></span>

<span data-ttu-id="e6452-105">Ниже приведены некоторые общие экземпляры условных операторов.</span><span class="sxs-lookup"><span data-stu-id="e6452-105">The following provides some common instances of conditional statements.</span></span> <span data-ttu-id="e6452-106">Дополнительные сведения см. в разделе [Синтаксис условных инструкций](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="e6452-106">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

## <a name="run-action-on-removal"></a><span data-ttu-id="e6452-107">Выполнить действие при удалении.</span><span class="sxs-lookup"><span data-stu-id="e6452-107">Run action on removal.</span></span>

<span data-ttu-id="e6452-108">Дополнительные сведения см. [в разделе действия по обработке условий, выполняемые во время удаления](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="e6452-108">For information, see [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span>

## <a name="run-action-only-if-the-product-has-not-been-installed"></a><span data-ttu-id="e6452-109">Выполнить действие, только если продукт не был установлен.</span><span class="sxs-lookup"><span data-stu-id="e6452-109">Run action only if the product has not been installed.</span></span>

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a><span data-ttu-id="e6452-110">Выполнить действие, только если продукт будет установлен локально.</span><span class="sxs-lookup"><span data-stu-id="e6452-110">Run action only if the product will be installed local.</span></span> <span data-ttu-id="e6452-111">Не выполнять действие при повторной установке.</span><span class="sxs-lookup"><span data-stu-id="e6452-111">Do not run action on a reinstallation.</span></span>

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

<span data-ttu-id="e6452-112">Термин "&FeatureName = 3" означает, что действием является установка локального компонента.</span><span class="sxs-lookup"><span data-stu-id="e6452-112">The term "&FeatureName=3" means the action is to install the feature local.</span></span> <span data-ttu-id="e6452-113">Термин «не (! FeatureName = 3) "означает, что эта функция не установлена локально.</span><span class="sxs-lookup"><span data-stu-id="e6452-113">The term "NOT(!FeatureName=3)" means the feature is not installed local.</span></span>

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a><span data-ttu-id="e6452-114">Выполнить действие, только если компонент будет удален.</span><span class="sxs-lookup"><span data-stu-id="e6452-114">Run action only if the feature will be uninstalled.</span></span>

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

<span data-ttu-id="e6452-115">Это условие проверяет только переход компонента из установленного состояния local в состояние отсутствия.</span><span class="sxs-lookup"><span data-stu-id="e6452-115">This condition only checks for a transition of the feature from an installed state of local to the absent state.</span></span>

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a><span data-ttu-id="e6452-116">Выполнить действие только в том случае, если компонент был установлен локально, но переходит из состояния.</span><span class="sxs-lookup"><span data-stu-id="e6452-116">Run action only if the component was installed local, but is transitioning out of state.</span></span>

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

<span data-ttu-id="e6452-117">Термин "? Компонетнаме = 3 означает, что компонент установлен локально.</span><span class="sxs-lookup"><span data-stu-id="e6452-117">The term "?ComponetName=3" means the component is installed local.</span></span> <span data-ttu-id="e6452-118">Термин "$ComponentName = 2" означает, что состояние действия в компоненте отсутствует.</span><span class="sxs-lookup"><span data-stu-id="e6452-118">The term "$ComponentName=2" means that the action state on the component is Absent.</span></span> <span data-ttu-id="e6452-119">Термин "$ComponentName = 4" означает, что состояние действия в компоненте запускается из источника.</span><span class="sxs-lookup"><span data-stu-id="e6452-119">The term "$ComponentName=4" means that the action state on the component is run from source.</span></span> <span data-ttu-id="e6452-120">Обратите внимание, что состояние действия объявления не является допустимым для компонента.</span><span class="sxs-lookup"><span data-stu-id="e6452-120">Note that an action state of advertise is not valid for a component.</span></span>

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a><span data-ttu-id="e6452-121">Выполнить действие только при переустановке компонента.</span><span class="sxs-lookup"><span data-stu-id="e6452-121">Run action only on the reinstallation of a component.</span></span>

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a><span data-ttu-id="e6452-122">Выполнить действие только при применении конкретного исправления.</span><span class="sxs-lookup"><span data-stu-id="e6452-122">Run action only when a particular patch is applied.</span></span>

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

<span data-ttu-id="e6452-123">Дополнительные сведения см. в разделе "Примечания" на странице свойств [**исправления**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="e6452-123">For more information, see the Remarks section on the [**PATCH**](patch.md) property page.</span></span>

 

 



