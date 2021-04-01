---
description: После успешной фиксации очереди необходимо будет обновить данные реестра для устанавливаемого продукта.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Обновление сведений реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999201"
---
# <a name="updating-registry-information"></a><span data-ttu-id="53d47-103">Обновление сведений реестра</span><span class="sxs-lookup"><span data-stu-id="53d47-103">Updating Registry Information</span></span>

<span data-ttu-id="53d47-104">После успешной фиксации очереди необходимо будет обновить данные реестра для устанавливаемого продукта.</span><span class="sxs-lookup"><span data-stu-id="53d47-104">After the queue has successfully committed, you will need to update registry information for the product you are installing.</span></span> <span data-ttu-id="53d47-105">Перед изменением данных реестра рекомендуется дождаться успешного завершения всех необходимых операций копирования файлов.</span><span class="sxs-lookup"><span data-stu-id="53d47-105">It is recommended that you wait until all necessary file copy operations have been successfully completed before altering registry information.</span></span>

<span data-ttu-id="53d47-106">Одним из способов обновления реестра является вызов [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) с помощью регулятора \_ ИНИФИЛЕС, прокрутка \_ реестра или самого регулятора \_ INI2REG.</span><span class="sxs-lookup"><span data-stu-id="53d47-106">One way to update the registry is to call [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) with the SPINST\_INIFILES, SPINST\_REGISTRY, or SPINST\_INI2REG flags specified.</span></span> <span data-ttu-id="53d47-107">Эти флаги можно объединить в один вызов **сетупинсталлфроминфсектион**.</span><span class="sxs-lookup"><span data-stu-id="53d47-107">These flags can be combined in one call to **SetupInstallFromInfSection**.</span></span>

<span data-ttu-id="53d47-108">В следующем примере показано использование СЧЕТЧИКа \_ всех файлов ^ Spin \_ , чтобы указать, что функция должна обрабатывать все перечисленные операции, за исключением операций с файлами.</span><span class="sxs-lookup"><span data-stu-id="53d47-108">The following example uses SPINST\_ALL^SPINST\_FILES to indicate that the function should process all of the listed operations except file operations.</span></span> <span data-ttu-id="53d47-109">Так как в разделе **Install** перечислены только операции ini, Registry и File, это краткий метод указания функции, которая должна обрабатывать все операции ini и реестра.</span><span class="sxs-lookup"><span data-stu-id="53d47-109">Since only INI, registry, and file operations are listed in the **Install** section, this is a shorthand method of specifying the function should process all INI and registry operations.</span></span>

<span data-ttu-id="53d47-110">В следующем примере показано, как установить данные реестра с помощью функции **сетупинсталлфроминфсектион** .</span><span class="sxs-lookup"><span data-stu-id="53d47-110">The following example shows how to install registry information using the **SetupInstallFromINFSection** function.</span></span>

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

<span data-ttu-id="53d47-111">В этом примере *овнервиндов* имеет **значение NULL** , так как только операции с файлами создают диалоговые окна, и поэтому родительское окно не требуется.</span><span class="sxs-lookup"><span data-stu-id="53d47-111">In the example, *OwnerWindow* is **NULL** because only file operations generate dialog boxes, and thus a parent window is not needed.</span></span> <span data-ttu-id="53d47-112">"Минф" — это INF-файл, содержащий раздел для обработки.</span><span class="sxs-lookup"><span data-stu-id="53d47-112">"MyInf" is the INF file containing the section to process.</span></span> <span data-ttu-id="53d47-113">Параметр "Мисектион" указывает раздел для установки.</span><span class="sxs-lookup"><span data-stu-id="53d47-113">The parameter, "MySection", specifies the section to be installed.</span></span> <span data-ttu-id="53d47-114">Объединенные флаги, РЕГУЛЯТОРы \_ все ^ все \_ файлы, укажите, какие операции установки следует обработать, в данном случае все операции, за исключением операций с файлами.</span><span class="sxs-lookup"><span data-stu-id="53d47-114">The combined flags, SPINST\_ALL ^ SPINST\_FILES, specify which installation operations to process, in this case, all operations except file operations.</span></span> <span data-ttu-id="53d47-115">Корневой путь источника указан как "A: \\ ".</span><span class="sxs-lookup"><span data-stu-id="53d47-115">The source root path is specified as "A:\\".</span></span>

<span data-ttu-id="53d47-116">Так как операции копирования не обрабатываются, параметры *копифлагс*, *мсгхандлер*, *context*, *девицеинфосет* и *девицеинфодата* не указаны.</span><span class="sxs-lookup"><span data-stu-id="53d47-116">Since no copy operations are being processed, the *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet*, and *DeviceInfoData* parameters are not specified.</span></span>

 

 



