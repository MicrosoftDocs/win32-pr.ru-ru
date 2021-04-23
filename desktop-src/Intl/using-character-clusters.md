---
description: Кластеры символов — это последовательности глифов, которые не могут быть разбиты между строками.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Использование кластеров символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819008"
---
# <a name="using-character-clusters"></a><span data-ttu-id="e9016-103">Использование кластеров символов</span><span class="sxs-lookup"><span data-stu-id="e9016-103">Using Character Clusters</span></span>

<span data-ttu-id="e9016-104">Кластеры символов — это последовательности глифов, которые не могут быть разбиты между строками.</span><span class="sxs-lookup"><span data-stu-id="e9016-104">Character clusters are glyph sequences that cannot be split between lines.</span></span> <span data-ttu-id="e9016-105">Некоторые языки, например тайский и индийские, ограничивают положение курсора точками между кластерами.</span><span class="sxs-lookup"><span data-stu-id="e9016-105">Some languages, for example Thai and Indic, restrict caret placement to points between clusters.</span></span> <span data-ttu-id="e9016-106">Это ограничение применяется к перемещению курсора с помощью клавиатуры или действий мыши (проверка нажатия).</span><span class="sxs-lookup"><span data-stu-id="e9016-106">This restriction applies to caret movement initiated with keyboard or mouse actions (hit testing).</span></span>

<span data-ttu-id="e9016-107">Uniscribe предоставляет сведения о кластере в визуальных атрибутах, содержащихся в структуре [**сценария \_ висаттр**](/windows/win32/api/usp10/ns-usp10-script_visattr) , и логические атрибуты, содержащиеся в структуре [**скрипта \_ логаттр**](/windows/win32/api/usp10/ns-usp10-script_logattr) .</span><span class="sxs-lookup"><span data-stu-id="e9016-107">Uniscribe provides cluster information in both the visual attributes contained in a [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure, and the logical attributes contained in a [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="e9016-108">После того как приложение вызовет [**скриптшапе**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), сведения о кластере представлены последовательностями одного значения в массиве **\_ Логаттр скриптов** и элементом **фклустерстарт** в массиве **\_ висаттр сценария** .</span><span class="sxs-lookup"><span data-stu-id="e9016-108">After the application calls [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), the cluster information is represented both by sequences of the same value in the **SCRIPT\_LOGATTR** array, and by the **fClusterStart** member in the **SCRIPT\_VISATTR** array.</span></span>

<span data-ttu-id="e9016-109">[**Скриптбреак**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) также получает элемент **фчарстоп** структуры [**script \_ логаттр**](/windows/win32/api/usp10/ns-usp10-script_logattr) для обнаружения позиций кластера.</span><span class="sxs-lookup"><span data-stu-id="e9016-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) also retrieves the **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure to identify cluster positions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9016-110">См. также</span><span class="sxs-lookup"><span data-stu-id="e9016-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9016-111">Использование Uniscribe</span><span class="sxs-lookup"><span data-stu-id="e9016-111">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



