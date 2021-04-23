---
description: Необходимо получить сведения из базы данных безопасности, а затем использовать эти сведения для настройки службы.
ms.assetid: c0c1c1e4-de5b-405d-abe8-33a985ce98e5
title: Реализация Сцесвкаттачментконфиг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98eb519e6422e3036ddfb203811322befd2713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999015"
---
# <a name="implementing-scesvcattachmentconfig"></a><span data-ttu-id="150ad-103">Реализация Сцесвкаттачментконфиг</span><span class="sxs-lookup"><span data-stu-id="150ad-103">Implementing SceSvcAttachmentConfig</span></span>

<span data-ttu-id="150ad-104">Функция [**сцесвкаттачментконфиг**](scesvcattachmentconfig.md) должна получать сведения из базы данных безопасности, а затем использовать эти сведения для настройки службы.</span><span class="sxs-lookup"><span data-stu-id="150ad-104">The [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md) function must retrieve information from the security database and then use that information to configure the service.</span></span>

<span data-ttu-id="150ad-105">При реализации [**сцесвкаттачментконфиг**](scesvcattachmentconfig.md)можно либо извлечь всю информацию, а затем настроить службу, либо получить и настроить службу на шаге.</span><span class="sxs-lookup"><span data-stu-id="150ad-105">When implementing [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md), you can either retrieve all of the information and then configure the service, or retrieve and configure the service in steps.</span></span> <span data-ttu-id="150ad-106">Следующий алгоритм извлекает все сведения, а затем настраивает службу.</span><span class="sxs-lookup"><span data-stu-id="150ad-106">The following algorithm retrieves all of the information and then configures the service.</span></span>

<span data-ttu-id="150ad-107">**Реализация Сцесвкаттачментконфиг**</span><span class="sxs-lookup"><span data-stu-id="150ad-107">**To implement SceSvcAttachmentConfig**</span></span>

1.  <span data-ttu-id="150ad-108">Определите переменные, необходимые для получения информации и кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="150ad-108">Define the variables needed to retrieve information and return codes.</span></span>
2.  <span data-ttu-id="150ad-109">Вызовите функцию обратного вызова Пфкуеринфо в структуре обратного вызова, чтобы получить сведения о конфигурации из базы данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="150ad-109">Call the pfQueryInfo callback function in the callback structure to retrieve configuration information from the security database.</span></span>
3.  <span data-ttu-id="150ad-110">Настройте систему с помощью возвращенных сведений.</span><span class="sxs-lookup"><span data-stu-id="150ad-110">Configure the system with the returned information.</span></span>
4.  <span data-ttu-id="150ad-111">Вызовите функцию обратного вызова Пффриинфо в структуре обратного вызова, чтобы освободить память, используемую для возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="150ad-111">Call the pfFreeInfo callback function in the callback structure to free memory used for returned information.</span></span>
5.  <span data-ttu-id="150ad-112">Если имеется сообщение о том, что расширение нужно добавить в файл журнала анализа, вызовите функцию обратного вызова Пфлогинфо в структуре обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="150ad-112">If there is any message that the extension wants to add to the analysis log file, call the pfLogInfo callback function in the callback structure.</span></span>
6.  <span data-ttu-id="150ad-113">Возврат соответствующих кодов **сцестатус** .</span><span class="sxs-lookup"><span data-stu-id="150ad-113">Return the appropriate **SCESTATUS** codes.</span></span>

<span data-ttu-id="150ad-114">В следующем примере показана одна возможная реализация [**сцесвкаттачментконфиг**](scesvcattachmentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="150ad-114">The following example shows one possible implementation of [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md).</span></span> <span data-ttu-id="150ad-115">Обратите внимание, что в этом примере функция Процессконфигуратионлине задает конфигурацию службы.</span><span class="sxs-lookup"><span data-stu-id="150ad-115">Note that in this example, the function ProcessConfigurationLine sets the service configuration.</span></span> <span data-ttu-id="150ad-116">Реализация этой функции не показана.</span><span class="sxs-lookup"><span data-stu-id="150ad-116">The implementation of this function is not shown.</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig (
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
      // Retrieve configuration information and configure
      // system. 
      ////////////////////////////////////////////////////
      do
      {
            retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                  SceSvcConfigurationInfo,
                                  NULL,
                                  FALSE,
                                  (PVOID *)&pConfigInfo,
                                  &EnumContext
                                 );
            if (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
            {
              ULONG i:
              //////////////////////////////////////////////////
              // Configure system.
              /////////////////////////////////////////////////
              for(i = 0; < pConfigInfo->Count; i++)
              {
                if(pConfigInfo->Line[i].Key == NULL) 
                    continue;
                ProcessConfigurationLine(pConfigInfo->Line[i]);
              }
      
      
              //////////////////////////////////////////////////
              // Free data returned.
              /////////////////////////////////////////////////
              (*(pSceCbInfo->pfFreeInfo)) ((PVOPID)pConfigInfo);
              pConfigInfo = NULL;
            }
        } while (retCode == SCESTATUS_SUCCESS && CountReturned > 0);
  
  
  ////////////////////////////////////////////////////
  // Add code for other return codes if retCode is 
  // not SCESTATUS_SUCCESS.
  ///////////////////////////////////////////////////
  return retCode;
}
```



 

 



