---
description: 'в следующем примере используется метод Windowsного получения изображений (wia) 1,0 ивиадевмгр:: регистеревенткаллбаккклсид, который регистрируется для получения уведомлений при подключении к системе любого устройства Windowsного получения изображений (WIA).'
ms.assetid: 1f2c7bc9-876a-4693-9439-52735e4b9d5f
title: Регистрация в событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7a72614533ccc7c2f72bb4f2cf105107cc88ef8030cf306d31d6d9ffa5b4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965553"
---
# <a name="registering-for-events"></a>Регистрация в событиях

в следующем примере используется метод Windowsного получения изображений (wia) 1,0 [**ивиадевмгр:: регистеревенткаллбаккклсид**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) , который регистрируется для получения уведомлений при подключении к системе любого устройства Windowsного получения изображений (WIA). Приложения также могут использовать WIA 1,0 [**ивиадевмгр:: регистеревенткаллбаккинтерфаце**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) и WIA 1,0 [**Ивиадевмгр:: регистеревенткаллбаккпрограм**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) для регистрации событий. в Windows Vista и более поздних версиях можно использовать методы Windowsного получения изображений (WIA) 2,0 [**IWiaDevMgr2:: регистеревенткаллбаккклсид**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2:: регистеревенткаллбаккинтерфаце**](-wia-iwiadevmgr2-registereventcallbackinterface.md)или [**IWiaDevMgr2:: регистеревенткаллбаккпрограм**](-wia-iwiadevmgr2-registereventcallbackprogram.md) для регистрации событий.

Предполагается, что пример взят из приложения, зарегистрированного как объект COM-сервера вне процесса.

Вызов [**ивиадевмгр:: регистеревенткаллбаккклсид**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) (или [**IWiaDevMgr2:: регистеревенткаллбаккклсид**](-wia-iwiadevmgr2-registereventcallbackclsid.md)) выглядит следующим образом:


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



В приведенном выше коде **пвиадевмгр** является допустимым указателем на интерфейс [**Ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (или [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)), \_ \_ \_ функция обратного вызова события регистрации WIA — это константа, указывающая, что этот вызов регистрируется для события в отличие от отмены регистрации для события, \_ \_ \_ подключенное устройство WIA — это константа, указывающая, что приложение регистрируется для получения уведомлений при каждом подключении устройства к компьютеру пользователя. **пклсид** — это указатель на зарегистрированный идентификатор CLSID приложения, **bstrName** — это имя приложения, **bstrDescription** — текстовое описание приложения, а **бстрикон** — имя файла изображения, используемого для значка приложения, регистрируемого для события.

После этого приложение должно реализовать метод [**ивиаевенткаллбакк:: имажеевенткаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) , который вызывается каждый раз, когда происходит событие, для которого зарегистрировано приложение.

Приложение может использовать метод [**ивиаитем:: енумрегистеревентинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) (или [**IWiaItem2:: енумрегистеревентинфо**](-wia-iwiaitem2-enumregistereventinfo.md)) для перечисления сведений о событиях, для которых он зарегистрирован.

 

 



