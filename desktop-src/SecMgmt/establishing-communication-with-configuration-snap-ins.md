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
# <a name="establishing-communication-with-configuration-snap-ins"></a><span data-ttu-id="97f8d-103">Установка связи с оснастками конфигурации</span><span class="sxs-lookup"><span data-stu-id="97f8d-103">Establishing Communication with Configuration Snap-ins</span></span>

<span data-ttu-id="97f8d-104">После того как расширение оснастки вложений будет добавлено в узел службы, оно должно установить связь с оснасткой настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="97f8d-104">After your attachment snap-in extension has added itself to the Services node, it should establish communication with the Security Configuration snap-in.</span></span> <span data-ttu-id="97f8d-105">Это необходимо, так как расширение оснастки «вложение» получает данные, а также любые изменения, внесенные пользователем, из оснастки «Настройка безопасности».</span><span class="sxs-lookup"><span data-stu-id="97f8d-105">This is necessary because the attachment snap-in extension gets its data, as well as any changes made by the user, from the Security Configuration snap-in.</span></span> <span data-ttu-id="97f8d-106">Это можно сделать, как описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="97f8d-106">This can be done as described in the following procedure.</span></span>

<span data-ttu-id="97f8d-107">**Установка связи с оснасткой «Настройка безопасности»**</span><span class="sxs-lookup"><span data-stu-id="97f8d-107">**To establish communication with the Security Configuration snap-ins**</span></span>

1.  <span data-ttu-id="97f8d-108">Получите имя файла конфигурации \_ \_ , используя формат буфера обмена вложений CCF сцесвк, который возвращает имя файла конфигурации в виде **пвстр**.</span><span class="sxs-lookup"><span data-stu-id="97f8d-108">Obtain the configuration file name using the CCF\_SCESVC\_ATTACHMENT clipboard format, which returns the configuration file name as a **PWSTR**.</span></span>

    <span data-ttu-id="97f8d-109">Если вложение вставляется в узел типа конфигурации, то для вложения необходимо указать, какая конфигурация это такое.</span><span class="sxs-lookup"><span data-stu-id="97f8d-109">If the attachment is inserted under a configuration type node, the attachment needs to know which configuration it is.</span></span> <span data-ttu-id="97f8d-110">(Она передает эти сведения в оснастки настройки безопасности во время инициализации интерфейса.) В этом случае используйте следующий код.</span><span class="sxs-lookup"><span data-stu-id="97f8d-110">(It communicates this information to the Security Configuration snap-ins during interface initialization.) In this case, use the following code.</span></span>

    ```C++
    PWSTR * TemplateName = ExtractTemplateFromDataObject(lpDataObject);
    ```

    

2.  <span data-ttu-id="97f8d-111">Настройте контекст с помощью оснасток настройки безопасности. После того как имя конфигурации известно или узел службы является узлом анализа, расширение оснастки вложений должно вызвать [**исцесвкаттачментдата:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) , чтобы настроить контекст, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="97f8d-111">Set up the context with the Security Configuration snap-ins. After the configuration name is known, or if the service node is an analysis node, the attachment snap-in extension must call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to set up the context, as shown in the following example.</span></span>

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
> <span data-ttu-id="97f8d-112">После завершения использования маркера, возвращенного [**исцесвкаттачментдата:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), закройте этот обработчик, вызвав функцию [**Исцесвкаттачментдата:: CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="97f8d-112">When you have finished using the handle returned by [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize), close the handle by calling the [**ISceSvcAttachmentData::CloseHandle**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-closehandle) function.</span></span> <span data-ttu-id="97f8d-113">Обычно это делается, когда пользователь закрывает консоль MMC.</span><span class="sxs-lookup"><span data-stu-id="97f8d-113">This is typically done when the user closes the MMC console.</span></span>

 

 

 



