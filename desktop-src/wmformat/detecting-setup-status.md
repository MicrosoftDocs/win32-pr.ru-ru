---
title: Определение состояния установки
description: Определение состояния установки
ms.assetid: d502a5d6-798b-4269-aef3-1412fc379819
keywords:
- Windows Media Format SDK, повторное распространение программного обеспечения
- Расширенный формат систем (ASF), повторное распространение программного обеспечения
- ASF (Расширенный системный формат), повторное распространение программного обеспечения
- Пакет SDK для Windows Media Format, повторное распространение
- Расширенный формат систем (ASF), распространение
- ASF (Расширенный системный формат), повторное распространение
- повторное распространение программного обеспечения, обнаружение состояния установки
- повторное распространение, обнаружение состояния установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6add696f2b2989de1e77d48504a1d540634213d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779754"
---
# <a name="detecting-setup-status"></a><span data-ttu-id="d8650-111">Определение состояния установки</span><span class="sxs-lookup"><span data-stu-id="d8650-111">Detecting Setup Status</span></span>

<span data-ttu-id="d8650-112">Когда исполняемый файл повторного распространения запускается на компьютере, он записывает свое состояние установки в реестре как значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8650-112">When the redistribution executable runs on a computer, it records its installation status in the registry as an **HRESULT** value.</span></span> <span data-ttu-id="d8650-113">Состояние установки хранится в записи реестра **инсталлресулт** в следующем подразделе:</span><span class="sxs-lookup"><span data-stu-id="d8650-113">The installation status is stored in the **InstallResult** registry entry under the following subkey:</span></span>

<span data-ttu-id="d8650-114">**\_Программа hKey текущее \_ пользовательское \\ по \\ Microsoft \\ MediaPlayer \\ Setup**</span><span class="sxs-lookup"><span data-stu-id="d8650-114">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Setup**</span></span>

<span data-ttu-id="d8650-115">Запись реестра **инсталлресулт** имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="d8650-115">The **InstallResult** registry entry has the following form.</span></span>



| <span data-ttu-id="d8650-116">Имя</span><span class="sxs-lookup"><span data-stu-id="d8650-116">Name</span></span>              | <span data-ttu-id="d8650-117">Тип</span><span class="sxs-lookup"><span data-stu-id="d8650-117">Type</span></span>           | <span data-ttu-id="d8650-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d8650-118">Value</span></span>                                                                                                                   |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8650-119">**инсталлресулт**</span><span class="sxs-lookup"><span data-stu-id="d8650-119">**InstallResult**</span></span> | <span data-ttu-id="d8650-120">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8650-120">**REG\_DWORD**</span></span> | <span data-ttu-id="d8650-121">**Значение HRESULT** , указывающее, была ли установка проигрывателя Windows Media выполнена успешно и требуется ли перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="d8650-121">An **HRESULT** that indicates whether Windows Media Player installation was successful and whether a restart is needed.</span></span> |



 

<span data-ttu-id="d8650-122">Следующий код задает для переменных *фсуцесс* и *фребутнидед* значение **true** или **false**(в зависимости от значения **HRESULT** , записанного программой установки Windows Media в пакете перераспределения компонентов).</span><span class="sxs-lookup"><span data-stu-id="d8650-122">The following code will set the *fSucess* and *fRebootNeeded* variables to **True** or **False**, as appropriate, based on the **HRESULT** value written by Windows Media setup in the component redistribution package.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

// If NS_S_REBOOT_REQUIRED is undefined, use 0xD2AF9.
#ifndef NS_S_REBOOT_REQUIRED
#define NS_S_REBOOT_REQUIRED       0xd2af9
#endif
  
int main( void )
{
    HKEY hKey = NULL;
    BOOL fSuccess = FALSE;
    BOOL fRebootNeeded = FALSE;

    LONG lResult = RegOpenKeyEx( 
        HKEY_CURRENT_USER, 
        TEXT("Software\\Microsoft\\MediaPlayer\\Setup"), 
        0, 
        KEY_QUERY_VALUE, 
        &hKey 
        );

    if ( lResult == ERROR_SUCCESS )
    {
        DWORD dwRegType = 0;   // Registry value type.
        DWORD dwValue = 0;     // Registry value.
        DWORD cbValue = sizeof( dwValue );  // Size of the value in bytes.

        lResult = RegQueryValueEx( 
            hKey, 
            TEXT("InstallResult"), 
            NULL, 
            &dwRegType, 
            (LPBYTE)&dwValue, 
            &cbValue
            );

        if( lResult == ERROR_SUCCESS )
        {
            if (dwRegType == REG_DWORD)
            {
                fSuccess = SUCCEEDED( dwValue );
                fRebootNeeded = ( NS_S_REBOOT_REQUIRED == dwValue );
            }
        }

        RegCloseKey( hKey );
    }

    if( fSuccess )
    {
        printf( "Setup succeeded." );
    }
    else
    {
        printf( "Setup failed." );
    }

    if( fRebootNeeded )
    {
        printf( "A reboot IS required.\n" );
    }
    else
    {
        printf( "A reboot IS NOT required.\n" );
    }
 
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="d8650-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d8650-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8650-124">**Повторное распространение программного обеспечения**</span><span class="sxs-lookup"><span data-stu-id="d8650-124">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




