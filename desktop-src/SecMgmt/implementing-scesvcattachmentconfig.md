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
# <a name="implementing-scesvcattachmentconfig"></a>Реализация Сцесвкаттачментконфиг

Функция [**сцесвкаттачментконфиг**](scesvcattachmentconfig.md) должна получать сведения из базы данных безопасности, а затем использовать эти сведения для настройки службы.

При реализации [**сцесвкаттачментконфиг**](scesvcattachmentconfig.md)можно либо извлечь всю информацию, а затем настроить службу, либо получить и настроить службу на шаге. Следующий алгоритм извлекает все сведения, а затем настраивает службу.

**Реализация Сцесвкаттачментконфиг**

1.  Определите переменные, необходимые для получения информации и кодов возврата.
2.  Вызовите функцию обратного вызова Пфкуеринфо в структуре обратного вызова, чтобы получить сведения о конфигурации из базы данных безопасности.
3.  Настройте систему с помощью возвращенных сведений.
4.  Вызовите функцию обратного вызова Пффриинфо в структуре обратного вызова, чтобы освободить память, используемую для возвращаемых данных.
5.  Если имеется сообщение о том, что расширение нужно добавить в файл журнала анализа, вызовите функцию обратного вызова Пфлогинфо в структуре обратного вызова.
6.  Возврат соответствующих кодов **сцестатус** .

В следующем примере показана одна возможная реализация [**сцесвкаттачментконфиг**](scesvcattachmentconfig.md). Обратите внимание, что в этом примере функция Процессконфигуратионлине задает конфигурацию службы. Реализация этой функции не показана.


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



 

 



