---
description: Чтобы создать поставщик методов WMI, необходимо зарегистрировать \_ \_ экземпляр Win32Provider, представляющий поставщика, с помощью экземпляра \_ \_ месодпровидеррегистратион.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Регистрация поставщика методов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265370"
---
# <a name="registering-a-method-provider"></a><span data-ttu-id="7ff4f-103">Регистрация поставщика методов</span><span class="sxs-lookup"><span data-stu-id="7ff4f-103">Registering a Method Provider</span></span>

<span data-ttu-id="7ff4f-104">Чтобы создать [*поставщик методов*](gloss-m.md) WMI, необходимо зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) , представляющий поставщика, с помощью экземпляра [**\_ \_ месодпровидеррегистратион**](--methodproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="7ff4f-104">To create a WMI [*method provider*](gloss-m.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_MethodProviderRegistration**](--methodproviderregistration.md).</span></span> <span data-ttu-id="7ff4f-105">После создания экземпляра [**\_ \_ Win32Provider**](--win32provider.md)необходимо зарегистрировать этот поставщик в WMI.</span><span class="sxs-lookup"><span data-stu-id="7ff4f-105">After creating an instance of [**\_\_Win32Provider**](--win32provider.md), you must register that provider with WMI.</span></span> <span data-ttu-id="7ff4f-106">В качестве COM-объекта поставщик должен зарегистрироваться в операционной системе и инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="7ff4f-106">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="7ff4f-107">В следующей процедуре предполагается, что вы уже реализовали процесс регистрации, как описано в статье [Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7ff4f-107">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="7ff4f-108">В следующей процедуре описывается регистрация поставщика методов.</span><span class="sxs-lookup"><span data-stu-id="7ff4f-108">The following procedure describes how to register a method provider.</span></span>

<span data-ttu-id="7ff4f-109">**Регистрация поставщика методов**</span><span class="sxs-lookup"><span data-stu-id="7ff4f-109">**To register a method provider**</span></span>

1.  <span data-ttu-id="7ff4f-110">Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) , который описывает поставщик.</span><span class="sxs-lookup"><span data-stu-id="7ff4f-110">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>

    <span data-ttu-id="7ff4f-111">Класс System [**\_ \_ месодпровидеррегистратион**](--methodproviderregistration.md) наследует многие свойства от родительского класса [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md) , однако единственное свойство, относящееся к поставщику метода, — это путь объекта к экземпляру [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff4f-111">The [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) system class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, However, the only property relevant for a method provider is the object path to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span>

2.  <span data-ttu-id="7ff4f-112">Создайте экземпляр класса [**\_ \_ месодпровидеррегистратион**](--methodproviderregistration.md) , описывающий набор функций поставщика.</span><span class="sxs-lookup"><span data-stu-id="7ff4f-112">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="7ff4f-113">Не забудьте пометить класс как как [**динамический**](dynamic-qualifier.md) , так и квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="7ff4f-113">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="7ff4f-114">**Динамический** квалификатор сигнализирует, что инструментарий WMI должен использовать поставщик для получения экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="7ff4f-114">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="7ff4f-115">Квалификатор **поставщика** указывает имя поставщика, который должен использовать WMI.</span><span class="sxs-lookup"><span data-stu-id="7ff4f-115">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="7ff4f-116">В следующем примере кода показано, как зарегистрировать поставщик метода.</span><span class="sxs-lookup"><span data-stu-id="7ff4f-116">The following code example describes how to register a method provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



