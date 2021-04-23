---
description: Чтобы создать поставщик событий WMI, необходимо зарегистрировать \_ \_ экземпляр Win32Provider, представляющий поставщика, с помощью экземпляра \_ \_ евентпровидеррегистратион.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Регистрация поставщика событий
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156763"
---
# <a name="registering-an-event-provider"></a><span data-ttu-id="fe78f-103">Регистрация поставщика событий</span><span class="sxs-lookup"><span data-stu-id="fe78f-103">Registering an Event Provider</span></span>

<span data-ttu-id="fe78f-104">Чтобы создать [*поставщик событий*](gloss-e.md) WMI, необходимо зарегистрировать экземпляр [**\_ \_ Win32Provider**](--win32provider.md) , представляющий поставщика, с помощью экземпляра [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="fe78f-104">To create a WMI [*event provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventProviderRegistration**](--eventproviderregistration.md).</span></span> <span data-ttu-id="fe78f-105">В качестве COM-объекта поставщик должен зарегистрироваться в операционной системе и инструментарии WMI.</span><span class="sxs-lookup"><span data-stu-id="fe78f-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="fe78f-106">В следующей процедуре предполагается, что вы уже реализовали процесс регистрации, как описано в статье [Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fe78f-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="fe78f-107">В следующей процедуре описывается регистрация поставщика событий.</span><span class="sxs-lookup"><span data-stu-id="fe78f-107">The following procedure describes how to register an event provider.</span></span>

<span data-ttu-id="fe78f-108">**Регистрация поставщика событий**</span><span class="sxs-lookup"><span data-stu-id="fe78f-108">**To register an event provider**</span></span>

1.  <span data-ttu-id="fe78f-109">Создайте экземпляр класса [**\_ \_ Win32Provider**](--win32provider.md) , который описывает поставщик.</span><span class="sxs-lookup"><span data-stu-id="fe78f-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="fe78f-110">Создайте экземпляр класса [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) , описывающий набор функций поставщика.</span><span class="sxs-lookup"><span data-stu-id="fe78f-110">Create an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="fe78f-111">Класс [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) наследует многие свойства от родительского класса [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="fe78f-111">The [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class.</span></span> <span data-ttu-id="fe78f-112">Свойства, локальные для класса **\_ \_ евентпровидеррегистратион** , представляют собой путь к объекту поставщика и список запросов, описывающих события, которые поддерживает поставщик.</span><span class="sxs-lookup"><span data-stu-id="fe78f-112">The properties local to the **\_\_EventProviderRegistration** class are the object path to the provider and a list of queries that describe the events that the provider supports.</span></span> <span data-ttu-id="fe78f-113">Дополнительные сведения см. в разделе [запрос WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="fe78f-113">For more information, see [Querying WMI](querying-wmi.md).</span></span>

3.  <span data-ttu-id="fe78f-114">Загрузите реализацию классов [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="fe78f-114">Load your implementation of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) classes into the WMI repository.</span></span>

    <span data-ttu-id="fe78f-115">Инструментарий WMI использует определение класса для регистрации и доступа к поставщику событий.</span><span class="sxs-lookup"><span data-stu-id="fe78f-115">WMI uses your class definition to register and access your event provider.</span></span> <span data-ttu-id="fe78f-116">Дополнительные сведения см. [в разделе Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fe78f-116">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="fe78f-117">В следующем примере кода описывается реализация класса [**\_ \_ Win32Provider**](--win32provider.md) и класса [**\_ \_ евентпровидеррегистратион**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="fe78f-117">The following code example describes an implementation of a [**\_\_Win32Provider**](--win32provider.md) class and a [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

<span data-ttu-id="fe78f-118">Первый запрос указывает, что поставщик создает все уведомления о событиях для класса внешних событий Факсевент.</span><span class="sxs-lookup"><span data-stu-id="fe78f-118">The first query indicates that the provider generates all event notifications for the extrinsic event class FaxEvent.</span></span> <span data-ttu-id="fe78f-119">Поскольку в нем используется оператор ISA, второй запрос подразумевает, что поставщик создает уведомления для всех событий создания экземпляра для класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) и всех его подклассов.</span><span class="sxs-lookup"><span data-stu-id="fe78f-119">Because it uses the ISA operator, the second query implies that the provider generates notifications for all instance creation events for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and all of its subclasses.</span></span>

<span data-ttu-id="fe78f-120">Когда поставщик регистрируется для предоставления внутреннего события, это событие должно применяться ко всем экземплярам класса.</span><span class="sxs-lookup"><span data-stu-id="fe78f-120">When a provider registers to provide an intrinsic event, the event must apply to all instances of a class.</span></span> <span data-ttu-id="fe78f-121">Иными словами, запрос не может быть написан, чтобы предоставить события создания экземпляра только для некоторых дисков, принадлежащих классу [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="fe78f-121">In other words, a query cannot be written to provide instance creation events for only some of the disk drives that belong to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

 

 
