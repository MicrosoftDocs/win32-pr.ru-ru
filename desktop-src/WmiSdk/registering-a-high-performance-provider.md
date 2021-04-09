---
description: Как и другие поставщики экземпляров, вы регистрируете высокопроизводительный поставщик в Microsoft Windows&\# 160; Инструментарий управления (WMI) путем создания экземпляра \_ \_ классов Win32Provider и \_ \_ инстанцепровидеррегистратион.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Регистрация поставщика High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e38653be78747bbfe68ce01d610e9b65b4c981d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080531"
---
# <a name="registering-a-high-performance-provider"></a><span data-ttu-id="4f468-103">Регистрация поставщика High-Performance</span><span class="sxs-lookup"><span data-stu-id="4f468-103">Registering a High-Performance Provider</span></span>

<span data-ttu-id="4f468-104">Как и другие поставщики экземпляров, вы регистрируете высокопроизводительный поставщик с помощью Microsoft инструментарий управления Windows (WMI) (WMI), создавая экземпляр классов [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="4f468-104">Like other instance providers, you register a high-performance provider with Microsoft Windows Management Instrumentation (WMI) by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes.</span></span> <span data-ttu-id="4f468-105">Экземпляр **\_ \_ Win32Provider** определяет физическую реализацию поставщика, а экземпляр **\_ \_ инстанцепровидеррегистратион** определяет набор функций поставщика.</span><span class="sxs-lookup"><span data-stu-id="4f468-105">The **\_\_Win32Provider** instance defines the provider's physical implementation, and the **\_\_InstanceProviderRegistration** instance defines the provider's feature set.</span></span> <span data-ttu-id="4f468-106">Дополнительные сведения см. [в разделе Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4f468-106">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="4f468-107">Следующая процедура описывает, как зарегистрировать высокопроизводительный поставщик экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4f468-107">The following procedure describes how to register a high-performance instance provider.</span></span>

<span data-ttu-id="4f468-108">**Регистрация поставщика высокопроизводительного экземпляра**</span><span class="sxs-lookup"><span data-stu-id="4f468-108">**To register a high-performance instance provider**</span></span>

1.  <span data-ttu-id="4f468-109">Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) , описывающий поставщик.</span><span class="sxs-lookup"><span data-stu-id="4f468-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class describing the provider.</span></span>

    <span data-ttu-id="4f468-110">Не забудьте добавить свойство **клиентлоадаблеклсид** в экземпляр [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="4f468-110">Be sure to add a **ClientLoadableCLSID** property to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span> <span data-ttu-id="4f468-111">Если поставщик и клиент находятся на одном компьютере, Инструментарий WMI загружает поставщик в процессе в клиенте с помощью **клиентлоадаблеклсид** в качестве идентификатора класса.</span><span class="sxs-lookup"><span data-stu-id="4f468-111">If both the provider and client reside on the same computer, WMI loads the provider in-process to the client using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="4f468-112">Когда поставщик и клиент располагаются на разных компьютерах, Инструментарий WMI загружает внутрипроцессный поставщик в WMI.</span><span class="sxs-lookup"><span data-stu-id="4f468-112">When the provider and client reside on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="4f468-113">Инструментарий WMI также использует **клиентлоадаблеклсид** для поддержки операций обновления.</span><span class="sxs-lookup"><span data-stu-id="4f468-113">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

2.  <span data-ttu-id="4f468-114">Создайте экземпляр класса [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) , описывающий набор функций поставщика.</span><span class="sxs-lookup"><span data-stu-id="4f468-114">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="4f468-115">Не забудьте пометить класс как как [**динамический**](dynamic-qualifier.md) , так и квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="4f468-115">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="4f468-116">**Динамический** квалификатор сигнализирует, что инструментарий WMI должен использовать поставщик для получения экземпляров класса.</span><span class="sxs-lookup"><span data-stu-id="4f468-116">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="4f468-117">Квалификатор **поставщика** указывает имя поставщика, который должен использовать WMI.</span><span class="sxs-lookup"><span data-stu-id="4f468-117">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

    <span data-ttu-id="4f468-118">Поставщик высокой производительности также должен поддерживать состояние для операций, операций перечисления или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="4f468-118">A high-performance provider also needs to state support for operations, enumeration operations, or both.</span></span> <span data-ttu-id="4f468-119">Убедитесь, что в реализации используются свойства **суппортсжет** и **суппортсенумератион** .</span><span class="sxs-lookup"><span data-stu-id="4f468-119">Make sure you use the **SupportsGet** and **SupportsEnumeration** properties in your implementation.</span></span>

<span data-ttu-id="4f468-120">В следующем примере кода показано, как реализовать классы [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ инстанцепровидеррегистратион**](--instanceproviderregistration.md) для высокопроизводительного поставщика.</span><span class="sxs-lookup"><span data-stu-id="4f468-120">The following code example shows you how to implement the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) classes for a high-performance provider.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a><span data-ttu-id="4f468-121">См. также</span><span class="sxs-lookup"><span data-stu-id="4f468-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f468-122">Создание поставщика экземпляров в поставщике High-Performance</span><span class="sxs-lookup"><span data-stu-id="4f468-122">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



