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
# <a name="implementing-scesvcattachmentanalyze"></a>Реализация Сцесвкаттачментанализе

Функция [**сцесвкаттачментанализе**](scesvcattachmentanalyze.md) должна получать сведения о конфигурации из базы данных безопасности и службы, сравнивать два набора данных, а затем обновлять раздел анализа базы данных безопасности с любыми различиями. Это можно проверить с помощью следующего алгоритма.

**Реализация Сцесвкаттачментанализе**

1.  Определите переменные, необходимые для получения и задания сведений о безопасности и кодов возврата.
2.  Вызовите функцию обратного вызова Пфкуеринфо в структуре обратного вызова, чтобы получить сведения о конфигурации из базы данных безопасности.
3.  Получите соответствующую информацию из службы.
4.  Сравните данные конфигурации, полученные из службы, с данными, полученными из базы данных безопасности.
5.  Если сведения не совпадают, вызовите функцию обратного вызова Пфсетинфо в структуре обратного вызова, чтобы обновить базу данных.
6.  Освободите все буферы, используемые для получения информации. Вызовите функцию обратного вызова Пффриинфо в структуре обратного вызова, чтобы освободить память, используемую для возвращаемых сведений о базе данных.
7.  Если имеется сообщение о том, что расширение нужно добавить в файл журнала анализа, вызовите функцию обратного вызова Пфлогинфо в структуре обратного вызова.
8.  Возврат соответствующих кодов **сцестатус** .

В следующем примере показана одна возможная реализация [**сцесвкаттачментанализе**](scesvcattachmentanalyze.md). Обратите внимание, что в этом примере функции Куериконфигуратионлине и Компаревалуе соответственно запрашивают информацию из службы и сравнивают эти значения с данными, полученными из базы данных безопасности. Реализация этих функций не показана.


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



 

 



