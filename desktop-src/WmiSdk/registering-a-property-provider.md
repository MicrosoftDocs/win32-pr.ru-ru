---
description: Чтобы создать поставщик свойств WMI, необходимо зарегистрировать \_ \_ экземпляр Win32Provider, представляющий поставщика, с помощью экземпляра \_ \_ пропертипровидеррегистратион.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Регистрация поставщика свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263820"
---
# <a name="registering-a-property-provider"></a><span data-ttu-id="ccaf0-103">Регистрация поставщика свойств</span><span class="sxs-lookup"><span data-stu-id="ccaf0-103">Registering a Property Provider</span></span>

<span data-ttu-id="ccaf0-104">Чтобы создать [*поставщик свойств*](gloss-p.md) WMI, необходимо зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) , представляющий поставщика, с помощью экземпляра [**\_ \_ пропертипровидеррегистратион**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="ccaf0-104">To create a WMI [*property provider*](gloss-p.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span> <span data-ttu-id="ccaf0-105">В качестве COM-объекта поставщик должен зарегистрироваться в операционной системе и инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="ccaf0-106">В следующей процедуре предполагается, что вы уже реализовали процесс регистрации, как описано в статье [Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ccaf0-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="ccaf0-107">В следующей процедуре описывается регистрация поставщика свойств.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-107">The following procedure describes how to register a property provider.</span></span>

<span data-ttu-id="ccaf0-108">**Регистрация поставщика свойств**</span><span class="sxs-lookup"><span data-stu-id="ccaf0-108">**To register a property provider**</span></span>

1.  <span data-ttu-id="ccaf0-109">Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) , который описывает поставщик свойств.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the property provider.</span></span>

    <span data-ttu-id="ccaf0-110">Класс [**\_ \_ Win32Provider**](--win32provider.md) принимает значения по умолчанию для других свойств, например значение **true** для **чистого** свойства.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-110">The [**\_\_Win32Provider**](--win32provider.md) class accepts the default values for other properties, such as the **TRUE** value for the **Pure** property.</span></span> <span data-ttu-id="ccaf0-111">Дополнительные сведения см. в разделе [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="ccaf0-111">For more information, see [**\_\_Win32Provider**](--win32provider.md).</span></span>

2.  <span data-ttu-id="ccaf0-112">Создайте экземпляр класса [**\_ \_ пропертипровидеррегистратион**](--propertyproviderregistration.md) , описывающий набор функций поставщика.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-112">Create an instance of the [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="ccaf0-113">Класс [**\_ \_ пропертипровидеррегистратион**](--propertyproviderregistration.md) наследует многие свойства от родительского класса [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md) , который предоставляет логические значения, которые указывают на поддержку определенных функций, и массив строк для указания поддержки запросов.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-113">The [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="ccaf0-114">Не забудьте пометить класс как как [**динамический**](dynamic-qualifier.md) , так и квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="ccaf0-114">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="ccaf0-115">**Динамический** квалификатор сигнализирует, что инструментарий WMI должен использовать динамический поставщик для получения экземпляров класса, содержащих Поддерживаемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-115">The **Dynamic** qualifier signals that WMI should use a dynamic provider to retrieve the class instances that contain the supported properties.</span></span> <span data-ttu-id="ccaf0-116">Квалификатор **поставщика** указывает имя поставщика, который должен использовать WMI.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-116">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="ccaf0-117">Инструментарий WMI вызывает Невкуери в поставщике событий, когда потребитель клиента регистрирует запрос фильтра событий, содержащий ссылки на события, поддерживаемые этим поставщиком событий.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-117">WMI calls NewQuery on an event provider when a client consumer registers an event filter query that contains references to events supported by that event provider.</span></span> <span data-ttu-id="ccaf0-118">Поэтому поставщик событий, ответственный за события изменения экземпляра для класса Емаилкласс, можно настроить для создания уведомлений только для отправителя.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-118">So the event provider responsible for instance modification events for the EmailClass class can be set up to generate notifications only for sender.</span></span> <span data-ttu-id="ccaf0-119">Когда поставщик получает запрос, запрашивающий уведомления об изменениях свойства Subject, поставщик может приступить к формированию этих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-119">When the provider receives a query requesting notification of changes to the subject property, the provider can start generating those notifications.</span></span> <span data-ttu-id="ccaf0-120">В этом сценарии Инструментарий WMI не требуется для отмены уведомлений, которые только изменяют получатель отчета.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-120">In this scenario, WMI is not required to discard the notifications that report recipient changes only.</span></span>

<span data-ttu-id="ccaf0-121">В следующем примере кода MOF описываются экземпляры, которые можно использовать для регистрации поставщика свойств.</span><span class="sxs-lookup"><span data-stu-id="ccaf0-121">The following MOF code example describes instances that can be used to register a property provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> <span data-ttu-id="ccaf0-122">Только администраторы могут регистрировать или удалять поставщик свойств, создавая экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ пропертипровидеррегистратион**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="ccaf0-122">Only administrators can register or delete a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span>

 

 

 



