---
description: В следующей таблице показаны различные методы, которые приложение может использовать для управления курсором, обоснованием и кластерами.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Работа со связями между позициями курсора, точками обоснования и кластерами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682720"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a><span data-ttu-id="675ce-103">Работа со связями между позициями курсора, точками обоснования и кластерами</span><span class="sxs-lookup"><span data-stu-id="675ce-103">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>

<span data-ttu-id="675ce-104">В следующей таблице показаны различные методы, которые приложение может использовать для управления курсором, обоснованием и кластерами.</span><span class="sxs-lookup"><span data-stu-id="675ce-104">The following table shows the various methods that the application can use to handle the caret, justification, and clusters.</span></span>



| <span data-ttu-id="675ce-105">Задача</span><span class="sxs-lookup"><span data-stu-id="675ce-105">Task</span></span>                             | <span data-ttu-id="675ce-106">Поддержка Uniscribe</span><span class="sxs-lookup"><span data-stu-id="675ce-106">Uniscribe support</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="675ce-107">Перемещение курсора по кластеру символов</span><span class="sxs-lookup"><span data-stu-id="675ce-107">Caret move by character cluster</span></span>  | <span data-ttu-id="675ce-108">Параметр *пвлогклуст* элемента [**скриптшапе**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) Функтионсе **фклустерстарт** в структуре [**script \_ висаттр**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="675ce-108">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="675ce-109">Элемент **фчарстоп** структуры [**скрипта \_ логаттр**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="675ce-109">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="675ce-110">Разрыв строки между символами</span><span class="sxs-lookup"><span data-stu-id="675ce-110">Line breaking between characters</span></span> | <span data-ttu-id="675ce-111">Параметр *пвлогклуст* элемента [**скриптшапе**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) Функтионсе **фклустерстарт** в структуре [**script \_ висаттр**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="675ce-111">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="675ce-112">Элемент **фчарстоп** структуры [**скрипта \_ логаттр**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="675ce-112">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="675ce-113">Курсор перемещается по слову</span><span class="sxs-lookup"><span data-stu-id="675ce-113">Caret move by word</span></span>               | <span data-ttu-id="675ce-114">Элемент **фвордстоп** структуры [**скрипта \_ логаттр**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="675ce-114">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="675ce-115">Разрыв строки между словами</span><span class="sxs-lookup"><span data-stu-id="675ce-115">Line breaking between words</span></span>      | <span data-ttu-id="675ce-116">Элемент **фвордстоп** структуры [**скрипта \_ логаттр**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="675ce-116">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="675ce-117">Обоснование</span><span class="sxs-lookup"><span data-stu-id="675ce-117">Justification</span></span>                    | <span data-ttu-id="675ce-118">Элемент **ужустификатион** структуры [**скрипта \_ висаттр**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="675ce-118">The **uJustification** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="675ce-119">См. также</span><span class="sxs-lookup"><span data-stu-id="675ce-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="675ce-120">Использование Uniscribe</span><span class="sxs-lookup"><span data-stu-id="675ce-120">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




