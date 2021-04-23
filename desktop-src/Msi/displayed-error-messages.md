---
description: Функция установщика может выводить сообщение об ошибке, возвращая одну из следующих ошибок. Окно ошибки отображается только в том случае, если уровень пользовательского интерфейса находится на уровне Full, Reduced или Basic. Дополнительные сведения см. в разделе уровни пользовательского интерфейса.
ms.assetid: 0153a21f-9b26-4088-b12b-96c9e6918cc3
title: Отображаемые сообщения об ошибках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d85417da7e2f8a01be5492560e83cd97bbc0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650654"
---
# <a name="displayed-error-messages"></a><span data-ttu-id="610f3-105">Отображаемые сообщения об ошибках</span><span class="sxs-lookup"><span data-stu-id="610f3-105">Displayed Error Messages</span></span>

<span data-ttu-id="610f3-106">[Функция установщика](installer-function-reference.md) может выводить сообщение об ошибке, возвращая одну из следующих ошибок.</span><span class="sxs-lookup"><span data-stu-id="610f3-106">An [installer function](installer-function-reference.md) may display an error message dialog box returning any of the following errors.</span></span> <span data-ttu-id="610f3-107">Окно ошибки отображается только в том случае, если уровень пользовательского интерфейса находится на уровне Full, Reduced или Basic.</span><span class="sxs-lookup"><span data-stu-id="610f3-107">An error box is displayed only if the user interface level is at the full, reduced, or basic level.</span></span> <span data-ttu-id="610f3-108">Дополнительные сведения см. в разделе [уровни пользовательского интерфейса](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="610f3-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="610f3-109">Функции установщика отображают только сообщения об ошибках, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="610f3-109">The installer functions only display error messages that are in the following table.</span></span> <span data-ttu-id="610f3-110">Для ошибок, не приводимых в этом списке, вызывающая функция отвечает за обработку сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="610f3-110">For errors not in this list, the caller of the function is responsible for handling the display of error messages.</span></span>



| <span data-ttu-id="610f3-111">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="610f3-111">Error code</span></span>               | <span data-ttu-id="610f3-112">Ошибка</span><span class="sxs-lookup"><span data-stu-id="610f3-112">Error</span></span>                        |
|--------------------------|------------------------------|
| <span data-ttu-id="610f3-113">Ошибка при \_ установке \_ приостановки</span><span class="sxs-lookup"><span data-stu-id="610f3-113">ERROR\_INSTALL\_SUSPEND</span></span>  | <span data-ttu-id="610f3-114">Установка была приостановлена.</span><span class="sxs-lookup"><span data-stu-id="610f3-114">The install was suspended.</span></span>   |
| <span data-ttu-id="610f3-115">Ошибка при \_ установке \_ усерексит</span><span class="sxs-lookup"><span data-stu-id="610f3-115">ERROR\_INSTALL\_USEREXIT</span></span> | <span data-ttu-id="610f3-116">Пользователь завершил установку.</span><span class="sxs-lookup"><span data-stu-id="610f3-116">The user exited the install.</span></span> |
| <span data-ttu-id="610f3-117">Ошибка \_ \_ при установке</span><span class="sxs-lookup"><span data-stu-id="610f3-117">ERROR\_INSTALL\_FAILURE</span></span>  | <span data-ttu-id="610f3-118">Сбой установки.</span><span class="sxs-lookup"><span data-stu-id="610f3-118">Install failed.</span></span>              |



 

 

 



