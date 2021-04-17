---
description: После создания обработчика для INF-файла можно получить сведения из него различными способами. Такие функции, как Сетупжетинфинформатион, Сетупкуеринффилеинформатион и Сетупкуеринфверсионинформатион, извлекают сведения о самом INF-файле.
ms.assetid: e64c9576-ad62-4ebd-8d30-4e4e0da3b8c5
title: Получение сведений из INF-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cfb1a52fd004b1d812e4a01320a5bdd2bbeca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663423"
---
# <a name="retrieving-information-from-an-inf-file"></a><span data-ttu-id="c8090-104">Получение сведений из INF-файла</span><span class="sxs-lookup"><span data-stu-id="c8090-104">Retrieving Information From an INF File</span></span>

<span data-ttu-id="c8090-105">После создания обработчика для INF-файла можно получить сведения из него различными способами.</span><span class="sxs-lookup"><span data-stu-id="c8090-105">After you have a handle to an INF file, you can retrieve information from it in a variety of ways.</span></span> <span data-ttu-id="c8090-106">Такие функции, как [**сетупжетинфинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**сетупкуеринффилеинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)и [**сетупкуеринфверсионинформатион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) , извлекают сведения о самом INF-файле.</span><span class="sxs-lookup"><span data-stu-id="c8090-106">Functions such as [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa), [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa), and [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa) retrieve information about the INF file itself.</span></span>

<span data-ttu-id="c8090-107">Другие функции, такие как [**сетупжетсаурцеинфо**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) и [**сетупжеттаржетпас**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) , получают сведения о исходных файлах и целевых каталогах.</span><span class="sxs-lookup"><span data-stu-id="c8090-107">Other functions such as [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) and [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha) acquire information about the source files and target directories.</span></span>

<span data-ttu-id="c8090-108">Низкоуровневые функции, такие как [**сетупжетлинетекст**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) и [**сетупжетстрингфиелд**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) , позволяют напрямую обращаться к информации, хранящейся в строке или поле INF-файла.</span><span class="sxs-lookup"><span data-stu-id="c8090-108">Low-level functions like [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta) and [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda) enable you to directly access information stored in a line or field of an INF file.</span></span> <span data-ttu-id="c8090-109">Эти функции используются внутренне функциями более высокого уровня, но также доступны для доступа к информации INF на уровне строки или поля.</span><span class="sxs-lookup"><span data-stu-id="c8090-109">These functions are used internally by the higher-level functions, but are also available should you need to access INF information at the line or field level.</span></span>

 

 



