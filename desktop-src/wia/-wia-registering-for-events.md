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
# <a name="registering-for-events"></a>Регистрация в событиях

В следующем примере используется метод получения образа Windows (WIA) 1,0 [**ивиадевмгр:: регистеревенткаллбаккклсид**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) , который регистрируется для получения уведомлений при подключении к системе любого устройства, использующего Windows Image (WIA). Приложения также могут использовать WIA 1,0 [**ивиадевмгр:: регистеревенткаллбаккинтерфаце**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) и WIA 1,0 [**Ивиадевмгр:: регистеревенткаллбаккпрограм**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) для регистрации событий. В Windows Vista и более поздних версиях можно использовать методы получения образа Windows (WIA) 2,0 [**IWiaDevMgr2:: регистеревенткаллбаккклсид**](-wia-iwiadevmgr2-registereventcallbackclsid.md), [**IWiaDevMgr2:: регистеревенткаллбаккинтерфаце**](-wia-iwiadevmgr2-registereventcallbackinterface.md)или [**IWiaDevMgr2:: регистеревенткаллбаккпрограм**](-wia-iwiadevmgr2-registereventcallbackprogram.md) для регистрации событий.

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

 

 



