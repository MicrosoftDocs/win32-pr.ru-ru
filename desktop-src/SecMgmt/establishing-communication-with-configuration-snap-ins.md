---
description: После того как расширение оснастки вложений будет добавлено в узел службы, оно должно установить связь с оснасткой настройки безопасности.
ms.assetid: 68a0e5a7-938f-45b7-90a3-8f35e5e6bbfb
title: Установка связи с оснастками конфигурации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fe9bcb80687fa50120d20594a81ea40b21c292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663918"
---
# <a name="establishing-communication-with-configuration-snap-ins"></a>Установка связи с оснастками конфигурации

После того как расширение оснастки вложений будет добавлено в узел службы, оно должно установить связь с оснасткой настройки безопасности. Это необходимо, так как расширение оснастки «вложение» получает данные, а также любые изменения, внесенные пользователем, из оснастки «Настройка безопасности». Это можно сделать, как описано в следующей процедуре.

**Установка связи с оснасткой «Настройка безопасности»**

1.  Получите имя файла конфигурации \_ \_ , используя формат буфера обмена вложений CCF сцесвк, который возвращает имя файла конфигурации в виде **пвстр**.

    Если вложение вставляется в узел типа конфигурации, то для вложения необходимо указать, какая конфигурация это такое. (Она передает эти сведения в оснастки настройки безопасности во время инициализации интерфейса.) В этом случае используйте следующий код.

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  Настройте контекст с помощью оснасток настройки безопасности. После того как имя конфигурации известно или узел службы является узлом анализа, расширение оснастки вложений должно вызвать [**исцесвкаттачментдата:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) , чтобы настроить контекст, как показано в следующем примере.

    ```C++
    LPSCESVCATTACHMENTPERSISTINFO pSceInfo;

        HRESULT hr = ((LPSCESVCATTACHMENTPERSISTINFO)this)->
                QueryInterface(IID_ISceSvcAttachmentPersistInfo,
                (void**)&pSceInfo);

        if ( SUCCEEDED(hr) )
        {

            hr = m_pSceData->Initialize(strServiceName, TemplateName,
                    pSceInfo, &ThisHandle);
            // Continue processing (not shown).
        }
    ```

    

> [!Note]  
> После завершения использования маркера, возвращенного [**исцесвкаттачментдата:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), закройте этот обработчик, вызвав функцию [**Исцесвкаттачментдата:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) . Обычно это делается, когда пользователь закрывает консоль MMC.

 

 

 



