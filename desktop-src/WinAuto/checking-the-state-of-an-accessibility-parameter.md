---
title: Проверка состояния параметра специальных возможностей
description: В следующем фрагменте кода используется функция Жетсистемметрикс для проверки параметра субтитров. Если Жетсистемметрикс возвращает значение TRUE, приложение должно представлять всю важную информацию в визуальной форме.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75409f5af96f83bf13f4834f83503579862caa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070095"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a><span data-ttu-id="67a05-104">Проверка состояния параметра специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="67a05-104">Checking the State of an Accessibility Parameter</span></span>

<span data-ttu-id="67a05-105">В следующем фрагменте кода используется функция [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) для проверки параметра субтитров.</span><span class="sxs-lookup"><span data-stu-id="67a05-105">The following code fragment uses the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function to check the ShowSounds parameter.</span></span> <span data-ttu-id="67a05-106">Если **жетсистемметрикс** возвращает **значение true**, приложение должно представлять всю важную информацию в визуальной форме.</span><span class="sxs-lookup"><span data-stu-id="67a05-106">If **GetSystemMetrics** returns **TRUE**, the application should present all important information in visual form.</span></span>


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 