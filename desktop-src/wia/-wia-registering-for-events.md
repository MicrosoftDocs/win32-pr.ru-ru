---
description: 'В следующем примере используется метод получения образа Windows (WIA) 1,0 Ивиадевмгр:: Регистеревенткаллбаккклсид, который регистрируется для получения уведомлений при подключении к системе любого устройства, использующего Windows Image (WIA).'
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Регистрация в событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40fe29be23bda4a3094ff8bcf90ae1ca677e858d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145376"
---
# <a name="registering-for-events"></a><span data-ttu-id="e1733-103">Регистрация в событиях</span><span class="sxs-lookup"><span data-stu-id="e1733-103">Registering for Events</span></span>

<span data-ttu-id="e1733-104">В следующем примере используется метод получения образа Windows (WIA) 1,0 [**ивиадевмгр:: регистеревенткаллбаккклсид**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) , который регистрируется для получения уведомлений при подключении к системе любого устройства, использующего Windows Image (WIA).</span><span class="sxs-lookup"><span data-stu-id="e1733-104">The following example uses the Windows Image Acquisition (WIA) 1.0 [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) method to register for notification when any Windows Image Acquisition (WIA) device is connected to the system.</span></span> <span data-ttu-id="e1733-105">Приложения также могут использовать WIA 1,0 [**ивиадевмгр:: регистеревенткаллбаккинтерфаце**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) и WIA 1,0 [**Ивиадевмгр:: регистеревенткаллбаккпрограм**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="e1733-105">Applications can also use WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) and WIA 1.0 [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) to register for events.</span></span> <span data-ttu-id="e1733-106">В Windows Vista и более поздних версиях можно использовать методы получения образа Windows (WIA) 2,0 [**IWiaDevMgr2:: регистеревенткаллбаккклсид**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2:: регистеревенткаллбаккинтерфаце**](-wia-iwiadevmgr2-registereventcallbackinterface.md)или [**IWiaDevMgr2:: регистеревенткаллбаккпрограм**](-wia-iwiadevmgr2-registereventcallbackprogram.md) для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="e1733-106">With Windows Vista and later, you can use the Windows Image Acquisition (WIA) 2.0 [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md), or [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) methods to register for events.</span></span>

<span data-ttu-id="e1733-107">Предполагается, что пример взят из приложения, зарегистрированного как объект COM-сервера вне процесса.</span><span class="sxs-lookup"><span data-stu-id="e1733-107">It is assumed that the example is taken from an application that is registered as a Component Object Model (COM) out-of-process server object.</span></span>

<span data-ttu-id="e1733-108">Вызов [**ивиадевмгр:: регистеревенткаллбаккклсид**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (или [**IWiaDevMgr2:: регистеревенткаллбаккклсид**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e1733-108">The call to [**IWiaDevMgr::RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (or [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) is as follows:</span></span>


```
    pWiaDevMgr->RegisterEventCallbackCLSID( WIA_REGISTER_EVENT_CALLBACK,
                                            NULL,
                                            WIA_EVENT_DEVICE_CONNECTED,
                                            pCLSID,
                                            bstrName,
                                            bstrDescription,
                                            bstrIcon
                                            );
```



<span data-ttu-id="e1733-109">В приведенном выше коде **пвиадевмгр** является допустимым указателем на интерфейс [**Ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)), \_ \_ \_ функция обратного вызова события регистрации WIA — это константа, указывающая, что этот вызов регистрируется для события в отличие от отмены регистрации для события, \_ \_ \_ подключенное устройство WIA — это константа, указывающая, что приложение регистрируется для получения уведомлений при каждом подключении устройства к компьютеру пользователя. **пклсид** — это указатель на зарегистрированный идентификатор CLSID приложения, **bstrName** — это имя приложения, **bstrDescription** — текстовое описание приложения, а **бстрикон** — имя файла изображения, используемого для значка приложения, регистрируемого для события.</span><span class="sxs-lookup"><span data-stu-id="e1733-109">In the previous code, **pWiaDevMgr** is a valid pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface, WIA\_REGISTER\_EVENT\_CALLBACK is a constant that specifies that this call is to register for the event as opposed to unregistering for the event, WIA\_EVENT\_DEVICE\_CONNECTED is a constant that specifies that the application is registering to be notified whenever a device is connected to the user's computer, **pCLSID** is a pointer to the registered CLSID of the application, **bstrName** is the name of the application, **bstrDescription** is a text description of the application, and **bstrIcon** is the name of an image file to be used for the icon for the application registering for the event.</span></span>

<span data-ttu-id="e1733-110">После этого приложение должно реализовать метод [**ивиаевенткаллбакк:: имажеевенткаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) , который вызывается каждый раз, когда происходит событие, для которого зарегистрировано приложение.</span><span class="sxs-lookup"><span data-stu-id="e1733-110">The application must then implement the [**IWiaEventCallback::ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) method, which is called whenever an event occurs for which the application is registered.</span></span>

<span data-ttu-id="e1733-111">Приложение может использовать метод [**ивиаитем:: енумрегистеревентинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (или [**IWiaItem2:: енумрегистеревентинфо**](-wia-iwiaitem2-enumregistereventinfo.md)) для перечисления сведений о событиях, для которых он зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="e1733-111">An application can use the [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)) method to enumerate the information about events for which it is registered.</span></span>

 

 



