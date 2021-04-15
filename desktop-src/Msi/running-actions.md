---
description: Функции установщика можно использовать для выполнения определенных действий или последовательностей действий.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Выполняемые действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662702"
---
# <a name="running-actions"></a><span data-ttu-id="c50f9-103">Выполняемые действия</span><span class="sxs-lookup"><span data-stu-id="c50f9-103">Running Actions</span></span>

<span data-ttu-id="c50f9-104">Функции установщика можно использовать для выполнения определенных действий или последовательностей действий.</span><span class="sxs-lookup"><span data-stu-id="c50f9-104">The installer functions can be used to run specific actions or action sequences.</span></span> <span data-ttu-id="c50f9-105">Эти действия могут быть либо [стандартными](standard-actions.md) , либо [настраиваемыми](custom-actions.md) действиями.</span><span class="sxs-lookup"><span data-stu-id="c50f9-105">These actions can either be [standard](standard-actions.md) or [custom](custom-actions.md) actions.</span></span> <span data-ttu-id="c50f9-106">В следующей процедуре описывается выполнение действий.</span><span class="sxs-lookup"><span data-stu-id="c50f9-106">The following procedure describes how to run actions:</span></span>

<span data-ttu-id="c50f9-107">**Выполнение последовательности действий**</span><span class="sxs-lookup"><span data-stu-id="c50f9-107">**To run an action sequence**</span></span>

1.  <span data-ttu-id="c50f9-108">Выполните последовательность действий, определенных в таблице, вызвав функцию [**мсисекуенце**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) .</span><span class="sxs-lookup"><span data-stu-id="c50f9-108">Run a sequence of actions defined in a table by calling the [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) function.</span></span>

    <span data-ttu-id="c50f9-109">Установщик запрашивает указанную таблицу и выполняет каждое действие, если его условное выражение принимает значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="c50f9-109">The installer queries the indicated table and runs each action if its conditional expression evaluates to TRUE.</span></span>

2.  <span data-ttu-id="c50f9-110">Проверьте условные выражения, вызвав функцию [**мсиевалуатекондитион**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="c50f9-110">Check conditional expressions by calling the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>
3.  <span data-ttu-id="c50f9-111">Выполните действие, вызвав функцию [**мсидоактион**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="c50f9-111">Run the action by calling the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span> <span data-ttu-id="c50f9-112">Действие может быть стандартным действием, пользовательским действием или диалоговым окном пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c50f9-112">The action can be a standard action, a custom action, or a user interface dialog box.</span></span>
4.  <span data-ttu-id="c50f9-113">Если во время выполнения этого действия произошла ошибка, вызовите функцию [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="c50f9-113">If an error occurred during the execution of this action, call the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="c50f9-114">Установщик обработает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c50f9-114">The installer will process the error.</span></span>

 

 



