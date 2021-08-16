---
description: Чтобы создать поставщик потребителей событий WMI, необходимо зарегистрировать \_ \_ экземпляр Win32Provider, представляющий поставщика, с помощью экземпляра \_ \_ евентконсумерпровидеррегистратион.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Регистрация поставщика событий-получателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1922970838b99e2a4a371ed7b00ae0f506a0381f0018509bfd6874074e0dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992545"
---
# <a name="registering-an-event-consumer-provider"></a>Регистрация поставщика событий-получателя

Чтобы создать [*поставщик потребителей событий*](gloss-e.md) WMI, необходимо зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) , представляющий поставщика, с помощью экземпляра [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md). В качестве COM-объекта поставщик должен зарегистрироваться в операционной системе и инструментарии WMI. В следующей процедуре предполагается, что вы уже реализовали процесс регистрации, как описано в статье [Регистрация поставщика](registering-a-provider.md).

В следующей процедуре описывается, как зарегистрировать поставщик потребителей событий.

**Регистрация поставщика потребителей событий**

1.  Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) , который описывает поставщик.
2.  Создайте экземпляр класса [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md) , описывающий набор функций поставщика.

    Свойства, определяемые [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md) , включают путь к объекту поставщика и имена логических классов потребителей, которые поддерживает поставщик потребителей событий.

    Не забудьте пометить класс как как **динамический** , так и квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) . **Динамический** квалификатор сигнализирует, что инструментарий WMI должен использовать поставщик для получения экземпляров класса. Квалификатор **поставщика** указывает имя поставщика, который должен использовать WMI.

В следующем примере кода показано, как зарегистрировать поставщик потребителей событий.

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



