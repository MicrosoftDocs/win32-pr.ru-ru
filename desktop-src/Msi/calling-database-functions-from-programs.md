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
# <a name="calling-database-functions-from-programs"></a><span data-ttu-id="5e965-103">Вызов функций базы данных из программ</span><span class="sxs-lookup"><span data-stu-id="5e965-103">Calling Database Functions from Programs</span></span>

<span data-ttu-id="5e965-104">Перед вызовом любой из следующих [функций базы данных](database-functions.md) из программы, например настраиваемого действия или процесса автоматизации, установщик должен сначала выполнить [действие костинитиализе](costinitialize-action.md), [действие филекост](filecost-action.md)и [действие костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="5e965-104">Before calling any of the following [Database Functions](database-functions.md) from a program, such as a custom action or an automation process, the installer must first run the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="5e965-105">Ниже приведен список функций базы данных, используемых в установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="5e965-105">The following is a list of database functions used in Windows Installer:</span></span>

-   [<span data-ttu-id="5e965-106">**мсижеткомпонентстате**</span><span class="sxs-lookup"><span data-stu-id="5e965-106">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
-   [<span data-ttu-id="5e965-107">**мсижетфеатурекост**</span><span class="sxs-lookup"><span data-stu-id="5e965-107">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
-   [<span data-ttu-id="5e965-108">**мсижетфеатурестате**</span><span class="sxs-lookup"><span data-stu-id="5e965-108">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
-   [<span data-ttu-id="5e965-109">**мсижетфеатуревалидстатес**</span><span class="sxs-lookup"><span data-stu-id="5e965-109">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
-   [<span data-ttu-id="5e965-110">**мсижетсаурцепас**</span><span class="sxs-lookup"><span data-stu-id="5e965-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)
-   [<span data-ttu-id="5e965-111">**мсижеттаржетпас**</span><span class="sxs-lookup"><span data-stu-id="5e965-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)
-   [<span data-ttu-id="5e965-112">**мсисеткомпонентстате**</span><span class="sxs-lookup"><span data-stu-id="5e965-112">**MsiSetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)
-   [<span data-ttu-id="5e965-113">**мсисетфеатурестате**</span><span class="sxs-lookup"><span data-stu-id="5e965-113">**MsiSetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)
-   [<span data-ttu-id="5e965-114">**мсисетинсталллевел**</span><span class="sxs-lookup"><span data-stu-id="5e965-114">**MsiSetInstallLevel**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)
-   [<span data-ttu-id="5e965-115">**мсисеттаржетпас**</span><span class="sxs-lookup"><span data-stu-id="5e965-115">**MsiSetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)
-   [<span data-ttu-id="5e965-116">**мсиверифидискспаце**</span><span class="sxs-lookup"><span data-stu-id="5e965-116">**MsiVerifyDiskSpace**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)

<span data-ttu-id="5e965-117">Перед вызовом [**мсисетфеатуреаттрибутес**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) из программы установщик должен сначала запустить действие костинитиализе.</span><span class="sxs-lookup"><span data-stu-id="5e965-117">Before calling [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) from a program, the installer must first run the CostInitialize action.</span></span> <span data-ttu-id="5e965-118">Затем программа установки выполняет действие Костфинализе после **мсисетфеатуреаттрибутес**.</span><span class="sxs-lookup"><span data-stu-id="5e965-118">The installer then runs the CostFinalize action after **MsiSetFeatureAttributes**.</span></span>

<span data-ttu-id="5e965-119">В следующем примере показан порядок, в котором действия функции должны вызываться при использовании [**мсижеттаржетпас**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) в программе.</span><span class="sxs-lookup"><span data-stu-id="5e965-119">The following example illustrates the order in which function actions must be called when using [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) in a program.</span></span>


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



 

 



