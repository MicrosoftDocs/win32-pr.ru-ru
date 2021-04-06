---
description: Перед вызовом любой из следующих функций базы данных из программы, например настраиваемого действия или процесса автоматизации, установщик должен сначала выполнить действие Костинитиализе, действие Филекост и действие Костфинализе.
ms.assetid: b9795825-41fa-474b-a0c5-06770aa99bc1
title: Вызов функций базы данных из программ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2adeab5570bc6786439d5de509f03ab906a0c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909039"
---
# <a name="calling-database-functions-from-programs"></a>Вызов функций базы данных из программ

Перед вызовом любой из следующих [функций базы данных](database-functions.md) из программы, например настраиваемого действия или процесса автоматизации, установщик должен сначала выполнить [действие костинитиализе](costinitialize-action.md), [действие филекост](filecost-action.md)и [действие костфинализе](costfinalize-action.md).

Ниже приведен список функций базы данных, используемых в установщик Windows.

-   [**мсижеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
-   [**мсижетфеатурекост**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
-   [**мсижетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
-   [**мсижетфеатуревалидстатес**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
-   [**мсижетсаурцепас**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)
-   [**мсижеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)
-   [**мсисеткомпонентстате**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)
-   [**мсисетфеатурестате**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)
-   [**мсисетинсталллевел**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)
-   [**мсисеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)
-   [**мсиверифидискспаце**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)

Перед вызовом [**мсисетфеатуреаттрибутес**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) из программы установщик должен сначала запустить действие костинитиализе. Затем программа установки выполняет действие Костфинализе после **мсисетфеатуреаттрибутес**.

В следующем примере показан порядок, в котором действия функции должны вызываться при использовании [**мсижеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) в программе.


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib") 

int main()  
{ 

MSIHANDLE hInstall;
TCHAR *szBuf;
DWORD cch  = 0 ;
 
if(MsiOpenPackage(_T("PathToPackage...."), &hInstall) == ERROR_SUCCESS)
{
    if(MsiDoAction(hInstall, _T("CostInitialize"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("FileCost"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("CostFinalize"))==ERROR_SUCCESS)   
    { 
        if(MsiGetTargetPath(hInstall, _T("FolderName"), _T(""),&cch)==ERROR_MORE_DATA)
        { 
            cch++; // add 1 to include null terminator since MsiGetTargetPath does not include it on return 
            szBuf = (TCHAR *) malloc(cch*sizeof(TCHAR));
            if(szBuf)
            {
                if(MsiGetTargetPath(hInstall, _T("FolderName"), szBuf,&cch)==ERROR_SUCCESS)
                {
                    // Add code to use szBuf here
                }
                free(szBuf);
            }
        } 
    } 
    MsiCloseHandle(hInstall);
}

return 0;  
}
```



 

 



