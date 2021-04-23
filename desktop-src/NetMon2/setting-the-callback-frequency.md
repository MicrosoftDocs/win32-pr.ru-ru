---
description: Используйте следующий код, чтобы задать частоту обратного вызова.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Настройка частоты ответного вызова
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343865"
---
# <a name="setting-the-callback-frequency"></a><span data-ttu-id="c6005-103">Настройка частоты ответного вызова</span><span class="sxs-lookup"><span data-stu-id="c6005-103">Setting the Callback Frequency</span></span>

<span data-ttu-id="c6005-104">Используйте следующий код, чтобы задать частоту обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="c6005-104">Use the following code to set the callback frequency:</span></span>

<span data-ttu-id="c6005-105">**Параметр DWORD** Значение = 1;</span><span class="sxs-lookup"><span data-stu-id="c6005-105">**DWORD** Value = 1;</span></span>


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



<span data-ttu-id="c6005-106">Этот фрагмент кода задает частоту ответного вызова равным 1 секунде (минимальное значение).</span><span class="sxs-lookup"><span data-stu-id="c6005-106">This code fragment sets the callback frequency to 1 second (the minimum value).</span></span> <span data-ttu-id="c6005-107">Максимальное значение должно быть намного больше 1.</span><span class="sxs-lookup"><span data-stu-id="c6005-107">The maximum value must be much larger than 1.</span></span> <span data-ttu-id="c6005-108">Если буфер поставщика сетевых пакетов (НПП) полон, НПП вызывает монитор назад.</span><span class="sxs-lookup"><span data-stu-id="c6005-108">If the network packet provider (NPP) buffer is full, the NPP calls the monitor back sooner.</span></span>

 

 



