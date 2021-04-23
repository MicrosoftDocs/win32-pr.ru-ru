---
description: Чтобы создать поставщик потребителей событий WMI, необходимо зарегистрировать \_ \_ экземпляр Win32Provider, представляющий поставщика, с помощью экземпляра \_ \_ евентконсумерпровидеррегистратион.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Регистрация поставщика событий-получателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812436"
---
# <a name="registering-an-event-consumer-provider"></a><span data-ttu-id="5505b-103">Регистрация поставщика событий-получателя</span><span class="sxs-lookup"><span data-stu-id="5505b-103">Registering an Event Consumer Provider</span></span>

<span data-ttu-id="5505b-104">Чтобы создать [*поставщик потребителей событий*](gloss-e.md) WMI, необходимо зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) , представляющий поставщика, с помощью экземпляра [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5505b-104">To create a WMI [*event consumer provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="5505b-105">В качестве COM-объекта поставщик должен зарегистрироваться в операционной системе и инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="5505b-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="5505b-106">В следующей процедуре предполагается, что вы уже реализовали процесс регистрации, как описано в статье [Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5505b-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="5505b-107">В следующей процедуре описывается, как зарегистрировать поставщик потребителей событий.</span><span class="sxs-lookup"><span data-stu-id="5505b-107">The following procedure describes how to register an event consumer provider.</span></span>

<span data-ttu-id="5505b-108">**Регистрация поставщика потребителей событий**</span><span class="sxs-lookup"><span data-stu-id="5505b-108">**To register an event consumer provider**</span></span>

1.  <span data-ttu-id="5505b-109">Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) , который описывает поставщик.</span><span class="sxs-lookup"><span data-stu-id="5505b-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="5505b-110">Создайте экземпляр класса [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md) , описывающий набор функций поставщика.</span><span class="sxs-lookup"><span data-stu-id="5505b-110">Create an instance of the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="5505b-111">Свойства, определяемые [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md) , включают путь к объекту поставщика и имена логических классов потребителей, которые поддерживает поставщик потребителей событий.</span><span class="sxs-lookup"><span data-stu-id="5505b-111">The properties that are defined by [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) include the object path to the provider and the names of the logical consumer classes that the event consumer provider supports.</span></span>

    <span data-ttu-id="5505b-112">Не забудьте пометить класс как как **динамический** , так и квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="5505b-112">Be sure to tag the class with both the **Dynamic** and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="5505b-113">**Динамический** квалификатор сигнализирует, что инструментарий WMI должен использовать поставщик для получения экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="5505b-113">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="5505b-114">Квалификатор **поставщика** указывает имя поставщика, который должен использовать WMI.</span><span class="sxs-lookup"><span data-stu-id="5505b-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="5505b-115">В следующем примере кода показано, как зарегистрировать поставщик потребителей событий.</span><span class="sxs-lookup"><span data-stu-id="5505b-115">The following code example shows how to register an event consumer provider.</span></span>

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

 

 



