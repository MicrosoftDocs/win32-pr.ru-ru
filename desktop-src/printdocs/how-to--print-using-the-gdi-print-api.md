---
description: В этом разделе рассказывается, как выполнять печать из собственной программы Windows с помощью GDI&\# 160; Печать&\# 160; API.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: Инструкции. печать с помощью API печати GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913152"
---
# <a name="how-to-print-using-the-gdi-print-api"></a><span data-ttu-id="cbb11-103">Инструкции. печать с помощью API печати GDI</span><span class="sxs-lookup"><span data-stu-id="cbb11-103">How To: Print Using the GDI Print API</span></span>

<span data-ttu-id="cbb11-104">В этом разделе рассказывается, как выполнять печать из собственной программы Windows с помощью [API печати GDI](gdi-printing.md).</span><span class="sxs-lookup"><span data-stu-id="cbb11-104">This topic introduces how to print from a native Windows program using the [GDI Print API](gdi-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="cbb11-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="cbb11-105">Overview</span></span>

<span data-ttu-id="cbb11-106">Печать обычно является неотъемлемой частью собственной программы Windows, поэтому она не является функцией, которую можно легко добавить после написания программы.</span><span class="sxs-lookup"><span data-stu-id="cbb11-106">Printing is usually an integral part of a native Windows program, so it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="cbb11-107">При проектировании программы для Windows 7 следует рассмотреть возможность использования [API печати XPS](xps-printing.md) для предоставления функций печати, так как он обеспечивает наиболее актуальную совместимость в будущем.</span><span class="sxs-lookup"><span data-stu-id="cbb11-107">When designing a program for Windows 7, you should consider using the [XPS Print API](xps-printing.md) to provide the printing functionality because it provides the most compatibility for the future.</span></span> <span data-ttu-id="cbb11-108">Программы, которые должны работать в Windows Vista и более ранних версиях Windows, скорее всего, будут использовать [API печати GDI](gdi-printing.md) для предоставления функций печати.</span><span class="sxs-lookup"><span data-stu-id="cbb11-108">Programs that must run on Windows Vista and earlier versions of Windows will most likely use the [GDI Print API](gdi-printing.md) to provide printing functionality.</span></span> <span data-ttu-id="cbb11-109">API печати GDI также поддерживается в Windows 7, но он более ограничен, чем API печати XPS.</span><span class="sxs-lookup"><span data-stu-id="cbb11-109">The GDI Print API is also supported in Windows 7, but it is more limited than the XPS Print API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbb11-110">См. также</span><span class="sxs-lookup"><span data-stu-id="cbb11-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbb11-111">Использование печати</span><span class="sxs-lookup"><span data-stu-id="cbb11-111">Using Printing</span></span>](using-printing.md)
</dt> <dt>

[<span data-ttu-id="cbb11-112">Печать из приложения Windows</span><span class="sxs-lookup"><span data-stu-id="cbb11-112">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



