---
description: Средство lodctr удаляет записи реестра, созданные lodctr.
ms.assetid: 83c0fb91-857c-40d9-8fb8-8734c1b573c4
title: Удаление имен и описаний счетчиков из реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ea8c0a8efbe9a798f980a061c6cfc65745b89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663158"
---
# <a name="removing-counter-names-and-descriptions-from-the-registry"></a><span data-ttu-id="e575b-103">Удаление имен и описаний счетчиков из реестра</span><span class="sxs-lookup"><span data-stu-id="e575b-103">Removing Counter Names and Descriptions from the Registry</span></span>

<span data-ttu-id="e575b-104">Средство **lodctr** удаляет записи реестра, созданные **lodctr**.</span><span class="sxs-lookup"><span data-stu-id="e575b-104">The **unlodctr** tool removes the registry entries created by **lodctr**.</span></span> <span data-ttu-id="e575b-105">Имя приложения, передаваемое в **lodctr** , должно соответствовать [имени ключа приложения](creating-the-applications-performance-key.md) , созданному в разделе **служб** .</span><span class="sxs-lookup"><span data-stu-id="e575b-105">The application name that you pass to **unlodctr** must match the [name of the application key](creating-the-applications-performance-key.md) that you created under the **Services** key.</span></span> <span data-ttu-id="e575b-106">Дополнительные сведения о запуске **lodctr** см. в центре справки и поддержки.</span><span class="sxs-lookup"><span data-stu-id="e575b-106">For details on running **unlodctr** see, Help and Support Center.</span></span>

## <a name="using-unlodctr"></a><span data-ttu-id="e575b-107">Использование lodctr</span><span class="sxs-lookup"><span data-stu-id="e575b-107">Using unlodctr</span></span>

<span data-ttu-id="e575b-108">Средство **lodctr** ищет первый и последний счетчики и помогает получить значения индексов, используя значения реестра Like, указанные в разделе с ключом **производительности** приложения.</span><span class="sxs-lookup"><span data-stu-id="e575b-108">The **unlodctr** tool looks up the first and last counter and help index values using the like named registry values under your application's **Performance** key.</span></span> <span data-ttu-id="e575b-109">Средство **lodctr** использует диапазон значений индекса для удаления текста из **счетчиков** и значений **справки** для каждого идентификатора языка.</span><span class="sxs-lookup"><span data-stu-id="e575b-109">The **unlodctr** tool uses the range of index values to remove the text from **Counters** and **Help** values for each language identifier.</span></span>

<span data-ttu-id="e575b-110">Используя значения индекса, **lodctr** вносит в реестр следующие изменения.</span><span class="sxs-lookup"><span data-stu-id="e575b-110">Using the index values, **unlodctr** makes the following changes to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = updated if changed
                  Last Help = updated if changed
                  \009
                     Counters = application text removed
                     Help = application text removed
                  \supported language, other than English
                     Counters = application text removed
                     Help = application text removed
```

<span data-ttu-id="e575b-111">Средство **lodctr** также удаляет **первый счетчик**, **последний счетчик**, **первую справку**, **последнюю справку** и значения **списка объектов** из ключа **производительности** приложения, расположенного в **hKey \_ локальный \_ компьютер** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ *имя приложения —* \\ **производительность**.</span><span class="sxs-lookup"><span data-stu-id="e575b-111">The **unlodctr** tool also removes the **First Counter**, **Last Counter**, **First Help**, **Last Help**, and **Object List** values from the application's **Performance** key located at **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\*application-name*\\**Performance**.</span></span>

> [!Note]  
> <span data-ttu-id="e575b-112">Функция выгрузки **lodctr**, [**унлоадперфкаунтертекстстрингс**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa)объявляется в LoadPerf. h и экспортируется из Loadperf.dll.</span><span class="sxs-lookup"><span data-stu-id="e575b-112">The unloading function of **unlodctr**, [**UnloadPerfCounterTextStrings**](/windows/desktop/api/Loadperf/nf-loadperf-unloadperfcountertextstringsa), is declared in Loadperf.h and exported from Loadperf.dll.</span></span> <span data-ttu-id="e575b-113">Это позволяет вызывать эту функцию непосредственно из программы удаления.</span><span class="sxs-lookup"><span data-stu-id="e575b-113">This allows you to call this function directly from your uninstall program.</span></span>

 

 

 



