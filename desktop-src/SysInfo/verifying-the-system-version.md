---
description: В нем содержатся примеры использования функции Верифиверсионинфо для определения того, работает ли приложение в определенной операционной системе.
ms.assetid: f39c35ae-9be5-4a03-9079-6fcc63387f6b
title: Проверка версии системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ddb3562230d0708ddc55d0f8214286ea6c3008
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264029"
---
# <a name="verifying-the-system-version"></a><span data-ttu-id="55a08-103">Проверка версии системы</span><span class="sxs-lookup"><span data-stu-id="55a08-103">Verifying the System Version</span></span>

<span data-ttu-id="55a08-104">\[ Использование функции [**верифиверсионинфо**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) для проверки текущей операционной системы не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="55a08-104">\[ Use of the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to verify the currently running operating system is not recommended.</span></span> <span data-ttu-id="55a08-105">Вместо этого используйте [ **API модуля поддержки версии** .](version-helper-apis.md)\]</span><span class="sxs-lookup"><span data-stu-id="55a08-105">Instead, use the [**Version Helper APIs**](version-helper-apis.md)\]</span></span>

<span data-ttu-id="55a08-106">В нем содержатся примеры использования функции [**верифиверсионинфо**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) для определения того, работает ли приложение в определенной операционной системе.</span><span class="sxs-lookup"><span data-stu-id="55a08-106">This contains examples that use the [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) function to determine whether the application is running on a specific operating system.</span></span>

<span data-ttu-id="55a08-107">Ниже приведены основные шаги в каждом примере.</span><span class="sxs-lookup"><span data-stu-id="55a08-107">The main steps in each example are as follows:</span></span>

1.  <span data-ttu-id="55a08-108">Задайте соответствующие значения в структуре [**осверсионинфоекс**](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="55a08-108">Set the appropriate values in the [**OSVERSIONINFOEX**](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa) structure.</span></span>
2.  <span data-ttu-id="55a08-109">Установите соответствующую маску условия с помощью макроса " [**\_ \_ условие набора ver**](/windows/desktop/api/Winnt/nf-winnt-ver_set_condition) ".</span><span class="sxs-lookup"><span data-stu-id="55a08-109">Set the appropriate condition mask using the [**VER\_SET\_CONDITION**](/windows/desktop/api/Winnt/nf-winnt-ver_set_condition) macro.</span></span>
3.  <span data-ttu-id="55a08-110">Вызовите [**верифиверсионинфо**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) , чтобы выполнить тест.</span><span class="sxs-lookup"><span data-stu-id="55a08-110">Call [**VerifyVersionInfo**](/windows/desktop/api/Winbase/nf-winbase-verifyversioninfoa) to perform the test.</span></span>

## <a name="example-1"></a><span data-ttu-id="55a08-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55a08-111">Example 1</span></span>

<span data-ttu-id="55a08-112">В следующем примере определяется, работает ли приложение в Windows XP с пакетом обновления 2 (SP2) или более поздней версии Windows, например Windows Server 2003 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="55a08-112">The following example determines whether the application is running on Windows XP with Service Pack 2 (SP2) or a later version of Windows, such as Windows Server 2003 or Windows Vista.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_WinXP_SP2_or_Later () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 1;
   osvi.wServicePackMajor = 2;
   osvi.wServicePackMinor = 0;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR,
      dwlConditionMask);
}

void main()
{
    if(Is_WinXP_SP2_or_Later())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



## <a name="example-2"></a><span data-ttu-id="55a08-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="55a08-113">Example 2</span></span>

<span data-ttu-id="55a08-114">Следующий код проверяет, что приложение работает на сервере Windows 2000 или более поздней версии, например Windows Server 2003 или Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="55a08-114">The following code verifies that the application is running on Windows 2000 Server or a later server, such as Windows Server 2003 or Windows Server 2008.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL Is_Win_Server() 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
   int op=VER_GREATER_EQUAL;

   // Initialize the OSVERSIONINFOEX structure.

   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.dwMinorVersion = 0;
   osvi.wServicePackMajor = 0;
   osvi.wServicePackMinor = 0;
   osvi.wProductType = VER_NT_SERVER;

   // Initialize the condition mask.

   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_MINORVERSION, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMAJOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_SERVICEPACKMINOR, op );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, VER_EQUAL );

   // Perform the test.

   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_MINORVERSION | 
      VER_SERVICEPACKMAJOR | VER_SERVICEPACKMINOR |
      VER_PRODUCT_TYPE,
      dwlConditionMask);
}

void main()
{
    if(Is_Win_Server())
        printf("The system meets the requirements.\n");
    else printf("The system does not meet the requirements.\n");
}
```



 

 



