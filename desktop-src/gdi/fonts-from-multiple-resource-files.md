---
description: Шрифты из нескольких файлов ресурсов
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Шрифты из нескольких файлов ресурсов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/17/2021
ms.locfileid: "104998876"
---
# <a name="fonts-from-multiple-resource-files"></a><span data-ttu-id="9ff16-103">Шрифты из нескольких файлов ресурсов</span><span class="sxs-lookup"><span data-stu-id="9ff16-103">Fonts from Multiple Resource Files</span></span>

<span data-ttu-id="9ff16-104">Как правило, шрифт содержится в файле ресурсов одного шрифта.</span><span class="sxs-lookup"><span data-stu-id="9ff16-104">Typically, a font is contained in a single font resource file.</span></span> <span data-ttu-id="9ff16-105">Однако информация для некоторых шрифтов распределяется между несколькими файлами.</span><span class="sxs-lookup"><span data-stu-id="9ff16-105">However, the information for some fonts is spread among several files.</span></span> <span data-ttu-id="9ff16-106">Например, для одного из нескольких образцов шрифтов требуется два файла:</span><span class="sxs-lookup"><span data-stu-id="9ff16-106">For example, Type 1 multiple master fonts require two files:</span></span>

-   <span data-ttu-id="9ff16-107">. ПФМ для метрик шрифтов</span><span class="sxs-lookup"><span data-stu-id="9ff16-107">.pfm for the font metrics</span></span>
-   <span data-ttu-id="9ff16-108">. ПФБ для битов шрифта</span><span class="sxs-lookup"><span data-stu-id="9ff16-108">.pfb for the font bits</span></span>

<span data-ttu-id="9ff16-109">Чтобы добавить шрифт из нескольких файлов в систему, используйте функции [**аддфонтресаурце**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) или [**аддфонтресаурцеекс**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) .</span><span class="sxs-lookup"><span data-stu-id="9ff16-109">To add a font from multiple files to the system, use the [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) or [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) functions.</span></span> <span data-ttu-id="9ff16-110">Параметр *лпсзфиленаме* в этих функциях должен указывать на строку, содержащую имена файлов, разделенные вертикальной чертой или вертикальной линией ( \| ).</span><span class="sxs-lookup"><span data-stu-id="9ff16-110">The *lpszFilename* parameter in these functions must point to a string that contains the file names separated by the vertical bar or pipe ( \| ).</span></span> <span data-ttu-id="9ff16-111">Например, чтобы указать абккскскскскс. ПФМ и абккскскскскс. ПФБ для шрифта типа 1, используйте строку "абккскскскскс. ПФМ \| абккскскскскс. ПФБ.".</span><span class="sxs-lookup"><span data-stu-id="9ff16-111">For example, to specify abcxxxxx.pfm and abcxxxxx.pfb for a Type 1 font, use the string "abcxxxxx.pfm \| abcxxxxx.pfb."</span></span>

<span data-ttu-id="9ff16-112">[**Аддфонтресаурцеекс**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) отличается от [**аддфонтресаурце**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) тем, что приложение, вызывающее **аддфонтресаурцеекс** , может указать, что шрифт является частным для самого себя или не перечислимого.</span><span class="sxs-lookup"><span data-stu-id="9ff16-112">[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) differs from [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) in that the application calling **AddFontResourceEx** can specify the font as private to itself or non-enumerable.</span></span>

<span data-ttu-id="9ff16-113">Чтобы добавить шрифт из образа памяти, используйте [**аддфонтмемресаурцеекс**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="9ff16-113">To add a font from a memory image, use [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex).</span></span> <span data-ttu-id="9ff16-114">Это позволяет приложению использовать шрифт, внедренный в документ или веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="9ff16-114">This allows an application to use a font that is embedded in a document or a webpage.</span></span>

<span data-ttu-id="9ff16-115">Чтобы удалить шрифт, полученный из нескольких файлов ресурсов, вызовите [**ремовефонтресаурце**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) или [**ремовефонтресаурцеекс**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)в зависимости от функции, используемой для добавления шрифта.</span><span class="sxs-lookup"><span data-stu-id="9ff16-115">To remove a font that came from multiple resource files, call [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) or [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), depending on the function used to add the font.</span></span> <span data-ttu-id="9ff16-116">Необходимо указать те же флаги, которые использовались для добавления шрифта.</span><span class="sxs-lookup"><span data-stu-id="9ff16-116">You must specify the same flags that were used to add the font.</span></span> <span data-ttu-id="9ff16-117">Чтобы удалить шрифт, добавленный из образа памяти, используйте [**ремовефонтмемресаурцеекс**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span><span class="sxs-lookup"><span data-stu-id="9ff16-117">To remove a font that was added from a memory image, use [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).</span></span>

<span data-ttu-id="9ff16-118">Использование шрифта, поступающих из нескольких файлов ресурсов шрифтов, аналогично использованию шрифта из одного файла ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ff16-118">Using a font that comes from multiple font-resource files is identical to using a font from a single resource file.</span></span>

 

 
