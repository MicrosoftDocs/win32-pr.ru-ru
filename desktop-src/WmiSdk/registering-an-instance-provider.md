---
description: Чтобы создать поставщик экземпляров WMI, необходимо зарегистрировать \_ \_ экземпляр Win32Provider, представляющий поставщика, с помощью экземпляра \_ \_ инстанцепровидеррегистратион.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Регистрация поставщика экземпляра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544695"
---
# <a name="registering-an-instance-provider"></a><span data-ttu-id="d33ee-103">Регистрация поставщика экземпляра</span><span class="sxs-lookup"><span data-stu-id="d33ee-103">Registering an Instance Provider</span></span>

<span data-ttu-id="d33ee-104">Чтобы создать [*поставщик экземпляров*](gloss-i.md) WMI, необходимо зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) , представляющий поставщика, с помощью экземпляра [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="d33ee-104">To create a WMI [*instance provider*](gloss-i.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="d33ee-105">В качестве COM-объекта поставщик должен зарегистрироваться в операционной системе и инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="d33ee-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="d33ee-106">В следующей процедуре предполагается, что вы уже реализовали процесс регистрации, как описано в статье [Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d33ee-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="d33ee-107">В следующей процедуре описывается регистрация поставщика экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d33ee-107">The following procedure describes how to register an instance provider.</span></span>

<span data-ttu-id="d33ee-108">**Регистрация поставщика экземпляров**</span><span class="sxs-lookup"><span data-stu-id="d33ee-108">**To register an instance provider**</span></span>

1.  <span data-ttu-id="d33ee-109">Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) , который описывает поставщик.</span><span class="sxs-lookup"><span data-stu-id="d33ee-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="d33ee-110">Создайте экземпляр класса [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) , описывающий набор функций поставщика.</span><span class="sxs-lookup"><span data-stu-id="d33ee-110">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="d33ee-111">Класс [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) наследует многие свойства от родительского класса [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md) , который предоставляет логические значения, которые указывают на поддержку определенных функций, и массив строк для указания поддержки запросов.</span><span class="sxs-lookup"><span data-stu-id="d33ee-111">The [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="d33ee-112">Не забудьте пометить класс как как [**динамический**](standard-wmi-qualifiers.md) , так и квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="d33ee-112">Be sure to tag the class with both the [**Dynamic**](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="d33ee-113">Квалификатор сигнализирует, что WMI должен использовать **динамический** поставщик для получения экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="d33ee-113">The qualifier signals that WMI should use a **Dynamic** provider to retrieve the class instances.</span></span> <span data-ttu-id="d33ee-114">Квалификатор **поставщика** указывает имя поставщика, который должен использовать WMI.</span><span class="sxs-lookup"><span data-stu-id="d33ee-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="d33ee-115">В следующем примере кода показано, как зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="d33ee-115">The following code example describes how to register a [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) instance.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



