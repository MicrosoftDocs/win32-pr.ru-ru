---
description: Пользовательские действия вызываются так же, как стандартные действия, либо путем явного вызова, либо во время выполнения таблицы последовательности.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Вызов настраиваемых действий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684448"
---
# <a name="invoking-custom-actions"></a><span data-ttu-id="f3678-103">Вызов настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="f3678-103">Invoking Custom Actions</span></span>

<span data-ttu-id="f3678-104">Пользовательские действия вызываются так же, как стандартные действия, либо путем явного вызова, либо во время выполнения таблицы последовательности.</span><span class="sxs-lookup"><span data-stu-id="f3678-104">Custom actions are invoked in the same manner as standard actions, either by explicit invocation or during the execution of a sequence table.</span></span> <span data-ttu-id="f3678-105">Существует два метода вызова действий:</span><span class="sxs-lookup"><span data-stu-id="f3678-105">There are two methods for calling actions:</span></span>

-   <span data-ttu-id="f3678-106">Вы вызываете указанное действие непосредственно с помощью функции [**мсидоактион**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) .</span><span class="sxs-lookup"><span data-stu-id="f3678-106">You call the specified action directly with the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function.</span></span>
-   <span data-ttu-id="f3678-107">Действие верхнего уровня вызывает таблицу последовательности, содержащую настраиваемое действие.</span><span class="sxs-lookup"><span data-stu-id="f3678-107">A top-level action calls the sequence table containing the custom action.</span></span> <span data-ttu-id="f3678-108">Дополнительные сведения о планировании настраиваемого действия в таблице последовательности см. в разделе [виртуализация настраиваемых действий](sequencing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f3678-108">For more information about scheduling a custom action in a sequence table, see [Sequencing Custom Actions](sequencing-custom-actions.md).</span></span>

<span data-ttu-id="f3678-109">Когда установщик получает имя действия из функции [**мсидоактион**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) или из таблицы последовательности, сначала выполняется поиск стандартного действия этого имени.</span><span class="sxs-lookup"><span data-stu-id="f3678-109">When the installer obtains an action name from the [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) function, or from a sequence table, it first searches for a standard action of that name.</span></span> <span data-ttu-id="f3678-110">Если не удается найти стандартное действие, установщик запрашивает [таблицу CustomAction](customaction-table.md) , чтобы проверить, является ли указанное действие пользовательским действием.</span><span class="sxs-lookup"><span data-stu-id="f3678-110">If it cannot find the standard action, then the installer queries the [CustomAction table](customaction-table.md) to check if the specified action is a custom action.</span></span> <span data-ttu-id="f3678-111">Если указанное действие не является пользовательским действием, установщик запрашивает в диалоговом окне [таблицу диалогового](dialog-table.md) окна.</span><span class="sxs-lookup"><span data-stu-id="f3678-111">If the specified action is not a custom action, then the installer queries the [Dialog table](dialog-table.md) for a dialog box.</span></span>

 

 



