---
description: Необходимо получить сведения о конфигурации из базы данных безопасности и службы, сравнить два набора данных, а затем обновить раздел анализа в базе данных безопасности с любыми различиями.
ms.assetid: f8420dde-55a2-40a0-b10d-140c28c0e9e4
title: Реализация Сцесвкаттачментанализе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f8501be2caac84c3dc96363eb85a8bc787d2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265628"
---
# <a name="implementing-scesvcattachmentanalyze"></a><span data-ttu-id="d6ae8-103">Реализация Сцесвкаттачментанализе</span><span class="sxs-lookup"><span data-stu-id="d6ae8-103">Implementing SceSvcAttachmentAnalyze</span></span>

<span data-ttu-id="d6ae8-104">Функция [**сцесвкаттачментанализе**](scesvcattachmentanalyze.md) должна получать сведения о конфигурации из базы данных безопасности и службы, сравнивать два набора данных, а затем обновлять раздел анализа базы данных безопасности с любыми различиями.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-104">The [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md) function must retrieve configuration information from the security database and the service, compare the two sets of information, and then update the analysis section of the security database with any differences.</span></span> <span data-ttu-id="d6ae8-105">Это можно проверить с помощью следующего алгоритма.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-105">You can ensure this by using the following algorithm.</span></span>

<span data-ttu-id="d6ae8-106">**Реализация Сцесвкаттачментанализе**</span><span class="sxs-lookup"><span data-stu-id="d6ae8-106">**To implement SceSvcAttachmentAnalyze**</span></span>

1.  <span data-ttu-id="d6ae8-107">Определите переменные, необходимые для получения и задания сведений о безопасности и кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-107">Define the variables needed to retrieve and set the security information and return codes.</span></span>
2.  <span data-ttu-id="d6ae8-108">Вызовите функцию обратного вызова Пфкуеринфо в структуре обратного вызова, чтобы получить сведения о конфигурации из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-108">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="d6ae8-109">Получите соответствующую информацию из службы.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-109">Retrieve the corresponding information from the service.</span></span>
4.  <span data-ttu-id="d6ae8-110">Сравните данные конфигурации, полученные из службы, с данными, полученными из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-110">Compare the configuration data retrieved from the service with that retrieved from the security database.</span></span>
5.  <span data-ttu-id="d6ae8-111">Если сведения не совпадают, вызовите функцию обратного вызова Пфсетинфо в структуре обратного вызова, чтобы обновить базу данных.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-111">If the information is not the same, call the pfSetInfo callback function in the callback structure to update the database.</span></span>
6.  <span data-ttu-id="d6ae8-112">Освободите все буферы, используемые для получения информации.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-112">Free all buffers used to retrieve information.</span></span> <span data-ttu-id="d6ae8-113">Вызовите функцию обратного вызова Пффриинфо в структуре обратного вызова, чтобы освободить память, используемую для возвращаемых сведений о базе данных.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-113">Call the pfFreeInfo callback function in the callback structure to free memory used for returned database information.</span></span>
7.  <span data-ttu-id="d6ae8-114">Если имеется сообщение о том, что расширение нужно добавить в файл журнала анализа, вызовите функцию обратного вызова Пфлогинфо в структуре обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-114">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
8.  <span data-ttu-id="d6ae8-115">Возврат соответствующих кодов **сцестатус** .</span><span class="sxs-lookup"><span data-stu-id="d6ae8-115">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="d6ae8-116">В следующем примере показана одна возможная реализация [**сцесвкаттачментанализе**](scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="d6ae8-116">The following example shows one possible implementation of [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md).</span></span> <span data-ttu-id="d6ae8-117">Обратите внимание, что в этом примере функции Куериконфигуратионлине и Компаревалуе соответственно запрашивают информацию из службы и сравнивают эти значения с данными, полученными из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-117">Note that in this example, the functions QueryConfigurationLine and CompareValue respectively query information from the service and compare those values with those retrieved from the security database.</span></span> <span data-ttu-id="d6ae8-118">Реализация этих функций не показана.</span><span class="sxs-lookup"><span data-stu-id="d6ae8-118">The implementation of these functions is not shown.</span></span>


```C++
#include <windows.h>

SCESTATUS WINAPI SceSvcAttachmentAnalyze (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo
)
{
  
    ////////////////////////////////////////////////////
    // Define variables.
    ////////////////////////////////////////////////////
    PSCESVC_CONFIGURATION_INFO     pConfigInfo = NULL;
    SCESTATUS                      retCode;
    SCE_ENUMERATION_CONTEXT        EnumContext = 0;
  
  

    if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ) 
    {
        return(SCESTATUS_INVALID_PARAMETER);
    }


  ////////////////////////////////////////////////////
  // Retrieve information from security database.
  ///////////////////////////////////////////////////
    do
    {
        retCode =  (*(pSceCbInfo->pfQueryInfo))(
                              pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              NULL,
                              FALSE,
                              &pConfigInfo,
                              &EnumContext
                              );
        if(retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
        {
          ULONG i;
          for(i = 0;i < pConfigInfo->Count; i++)
          {
            if(pConfigInfo->Line[I].Key == NULL) 
                continue;
        
        //////////////////////////////////////////////
        // Query service for corresponding key.
        //////////////////////////////////////////////
            QueryConfigurationLine(
                               pConfigInfo->Line[i].Key,
                               &SystemValue);
        
        //////////////////////////////////////////////
        // Compare values.
        //////////////////////////////////////////////
            CompareValue(
                     pConfigInfo->Line[i].Key,
                     SystemValue,
                     pConfigInfo->Line[i].Value,
                     &Result);
        
        //////////////////////////////////////////////
        // Write to security database if values are 
        // not equal.
        //////////////////////////////////////////////
            if(Result != NULL)
            {
              retCode =  (*(pSceCbInfo->pfSetInfo))(pSceCbInfo->sceHandle,
                                      SceSvcAnalysisInfo,
                                      pConfigInfo->Line[i].Key,
                                      TRUE,
                                      Result);
              if(retCode != SCESTATUS_SUCCESS)
              {
                //////////////////////////////////////////
                // Add code to handle other return codes.
                //////////////////////////////////////////
              }
            }
        }
      
          //////////////////////////////////////////////
          // Free all buffers used to retrieve 
          // SceSvcFree frees memory allocated by call 
          // to SceSvcQueryQueryInfo. 
          /////////////////////////////////////////
        (*(pSceCbInfo->pfFreeInfo)) (PVOID)pConfigInfo);
          pConfigInfo = NULL;
    }
  } while (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL);
  
  
  //////////////////////////////////////////////////
  // If the return code is not SCESTATUS_SUCCESS, add code to 
  // set error message appropriately.
  //////////////////////////////////////////////////
  return retCode;
}
```



 

 



