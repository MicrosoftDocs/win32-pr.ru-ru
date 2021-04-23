---
description: В следующем примере функция Верифиверсионинфо используется для определения того, установлены ли указанные наборы продуктов на локальном компьютере.
ms.assetid: 9f405e99-28f5-4415-a274-682b87ae6842
title: Обнаружение набора продуктов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594acbe22283e1c2a3be3ce60116076b2de6f3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664715"
---
# <a name="detecting-a-product-suite"></a><span data-ttu-id="63246-103">Обнаружение набора продуктов</span><span class="sxs-lookup"><span data-stu-id="63246-103">Detecting a Product Suite</span></span>

<span data-ttu-id="63246-104">В следующем примере функция [**верифиверсионинфо**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) используется для определения того, установлены ли указанные наборы продуктов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="63246-104">The following example uses the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to determine whether the specified product suite(s) are installed on the local computer.</span></span>

<span data-ttu-id="63246-105">В этом примере используется \_ флаг ver и.</span><span class="sxs-lookup"><span data-stu-id="63246-105">This example uses the VER\_AND flag.</span></span> <span data-ttu-id="63246-106">Если в маске набора указаны два флага, функция возвращает **значение true** только в случае наличия обоих наборов продуктов.</span><span class="sxs-lookup"><span data-stu-id="63246-106">If two flags are specified in the suite mask, the function returns **TRUE** only if both product suites are present.</span></span> <span data-ttu-id="63246-107">Если этот пример был изменен для использования версии \_ или флага, [**Верифиверсионинфо**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) возвратит **значение true** , если имеется один из наборов продуктов.</span><span class="sxs-lookup"><span data-stu-id="63246-107">If the example were changed to use the VER\_OR flag, [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) would return **TRUE** if either product suite were present.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CheckProductSuite ( WORD wSuite ) 
{
  OSVERSIONINFOEX osvi;
  DWORDLONG dwlConditionMask = 0;

  // Initialize the OSVERSIONINFOEX structure.

  ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
  osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
  osvi.wSuiteMask = wSuite;

  // Set up the condition mask.

  VER_SET_CONDITION( dwlConditionMask, 
          VER_SUITENAME, VER_AND );

  // Perform the test.

  return VerifyVersionInfo(
          &osvi, 
          VER_SUITENAME,
          dwlConditionMask);
}

void main()
{
    if( CheckProductSuite(VER_SUITE_ENTERPRISE) )
        printf( "The system meets the requirements.\n" );
    else printf( "The system does not meet the requirements.\n");
}
```



 

 



