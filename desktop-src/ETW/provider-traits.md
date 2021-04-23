---
description: Признаки поставщика — это метод присоединения дополнительных данных к регистрации отдельного поставщика.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Признаки поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985857"
---
# <a name="provider-traits"></a><span data-ttu-id="f5fa2-103">Признаки поставщика</span><span class="sxs-lookup"><span data-stu-id="f5fa2-103">Provider Traits</span></span>

<span data-ttu-id="f5fa2-104">Признаки поставщика — это метод присоединения дополнительных данных к регистрации отдельного поставщика.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-104">Provider Traits are a method of attaching more data to an individual provider registration.</span></span> <span data-ttu-id="f5fa2-105">Их можно использовать для поставщиков на основе манифеста или Трацелоггинг.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-105">They can be used for manifest-based or TraceLogging providers.</span></span> <span data-ttu-id="f5fa2-106">В настоящее время это включает поддержку добавления имени поставщика и (или) группы поставщиков в регистрацию отдельного поставщика.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-106">This currently includes support for adding a Provider Name and/or Provider Group to an individual provider registration.</span></span> <span data-ttu-id="f5fa2-107">В будущем, скорее всего, будут добавляться дополнительные типы признаков.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-107">More trait types are likely to be added in the future.</span></span> <span data-ttu-id="f5fa2-108">Эти сведения хранятся в ядре как двоичный BLOB-объект формата набора.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-108">This information is stored in the kernel as a binary blob of a set format.</span></span>

<span data-ttu-id="f5fa2-109">Признаки можно задать только один раз для регистрации.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-109">Traits can only be set once for a registration.</span></span> <span data-ttu-id="f5fa2-110">Дальнейшие попытки установить признаки для этой регистрации завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-110">Any further attempts to set the traits on that registration will fail.</span></span>

<span data-ttu-id="f5fa2-111">Чтобы задать признаки поставщика для поставщика на основе манифеста, вызовите функцию [**евентсетинформатион**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) с классом Information евентпровидерсеттраитс.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-111">To set Provider Traits on a manifest-based provider, call the [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) function with the EventProviderSetTraits information class.</span></span> <span data-ttu-id="f5fa2-112">Буфер Евентинформатион должен содержать двоичный BLOB-объект следующего формата:</span><span class="sxs-lookup"><span data-stu-id="f5fa2-112">The EventInformation buffer should contain a binary blob of the following format:</span></span>

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

<span data-ttu-id="f5fa2-113">Отдельные признаки должны иметь следующий формат:</span><span class="sxs-lookup"><span data-stu-id="f5fa2-113">Individual traits should be in the following format:</span></span>

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

<span data-ttu-id="f5fa2-114">Из отдельных признаков, \_ тип характеристик поставщика трассировки событий Windows \_ \_ определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f5fa2-114">From the individual trait, ETW\_PROVIDER\_TRAIT\_TYPE is defined as:</span></span>

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

<span data-ttu-id="f5fa2-115">Поставщики Трацелоггинг автоматически устанавливают признаки поставщика при вызове функции [**трацелоггингрегистер**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) .</span><span class="sxs-lookup"><span data-stu-id="f5fa2-115">TraceLogging providers automatically set the Provider Traits when the [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) function is called.</span></span> <span data-ttu-id="f5fa2-116">Имя поставщика Трацелоггинг всегда будет включаться в его признаки.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-116">The TraceLogging provider's name will always be included in its traits.</span></span> <span data-ttu-id="f5fa2-117">Группу можно задать для поставщика Трацелоггинг с помощью макроса [**трацелоггингоптионграуп**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) в определении поставщика.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-117">A group can be set on a TraceLogging provider using the [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) macro in the provider definition.</span></span>

## <a name="custom-traits"></a><span data-ttu-id="f5fa2-118">Пользовательские признаки</span><span class="sxs-lookup"><span data-stu-id="f5fa2-118">Custom Traits</span></span>

<span data-ttu-id="f5fa2-119">Хотя большинство 255 возможных типов признаков еще не определены, типы признаков 1-127 зарезервированы для определения корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-119">Although most of the 255 possible trait types are not yet defined, trait types 1-127 are reserved for definition by Microsoft.</span></span> <span data-ttu-id="f5fa2-120">Остальные более высокие значения индексированного типа могут использоваться внешними разработчиками по мере их появлении.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-120">The remaining higher indexed type values can be used by external developers as they see fit.</span></span> <span data-ttu-id="f5fa2-121">Любой пользователь, просматривая добавление собственных пользовательских признаков к поставщику, должен попытаться удержать общий размер признаков менее 256 байт по следующим причинам:</span><span class="sxs-lookup"><span data-stu-id="f5fa2-121">Anyone considering adding their own custom traits to their provider should try to keep their total trait size under 256 bytes for the following reasons:</span></span>

-   <span data-ttu-id="f5fa2-122">Признаки включаются в каждое событие, написанное для поставщика.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-122">The traits are included in every event written for the provider.</span></span> <span data-ttu-id="f5fa2-123">Большие признаки могут привести к очень большому объему файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-123">Large traits could lead to very large log files.</span></span>
-   <span data-ttu-id="f5fa2-124">Признаки хранятся в нестраничном пуле ядра в течение времени существования поставщика.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-124">The traits are stored in nonpaged kernel pool for the lifetime of the provider.</span></span>

## <a name="provider-groups"></a><span data-ttu-id="f5fa2-125">Группы поставщиков</span><span class="sxs-lookup"><span data-stu-id="f5fa2-125">Provider Groups</span></span>

<span data-ttu-id="f5fa2-126">Группа поставщиков представляет собой управляемую идентификатором GUID сущность, похожую на самого поставщика.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-126">A provider group is a GUID-defined controllable entity much like a provider itself.</span></span> <span data-ttu-id="f5fa2-127">Ключевое различие заключается в том, что в то время как идентификатор GUID поставщика используется для управления регистрацией только своего поставщика, группа будет управлять всеми ее регистрациями членов.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-127">The key difference is that while a provider GUID is used to control registrations of just its provider, a group will control all of its member registrations.</span></span> <span data-ttu-id="f5fa2-128">Например, если включить группу поставщиков с заданным ключевым словом и уровнем, будут включены все регистрации членов групп с этим ключевым словом и уровнем.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-128">For example, enabling a provider group with a given keyword and level will enable all of the groups member registrations with that keyword and level.</span></span>

<span data-ttu-id="f5fa2-129">Членство в группе может быть ограничено разрешениями.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-129">Group membership may be restricted by permissions.</span></span> <span data-ttu-id="f5fa2-130">Если вызывающий объект [**евентсетинформатион**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) не имеет разрешений на присоединение к указанной группе, членство будет отклонено.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-130">If the caller of [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) doesn't have permissions to join the specified group, then membership will be denied.</span></span>

<span data-ttu-id="f5fa2-131">В некоторых случаях для контроллера сеанса трассировки может потребоваться исключить несколько поставщиков из включенной группы.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-131">In some cases the trace session controller may want to exclude a few providers from its enable of a group.</span></span> <span data-ttu-id="f5fa2-132">Это можно сделать, задав список запретов.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-132">This can be done by setting a disallow list.</span></span> <span data-ttu-id="f5fa2-133">Список запретов — это список идентификаторов GUID поставщика, которые не будут включены на основе параметров группы для одного сеанса ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-133">A disallow list is a list of provider GUIDs that will not be enabled based on the group settings for a single logging session.</span></span> <span data-ttu-id="f5fa2-134">Списки запретов можно динамически изменять с помощью [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) и класса Information трацесетдисалловлист.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-134">Disallow lists can be changed dynamically with [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) and the TraceSetDisallowList information class.</span></span>

<span data-ttu-id="f5fa2-135">Хотя большинство действий по включению можно выполнять для групп поставщиков аналогичным образом для отдельных поставщиков, существуют некоторые исключения.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-135">While most enable actions can be done for Provider Groups in a similar manner to individual providers, there are some exceptions.</span></span> <span data-ttu-id="f5fa2-136">Исключения:</span><span class="sxs-lookup"><span data-stu-id="f5fa2-136">Exceptions include:</span></span>

-   <span data-ttu-id="f5fa2-137">Группы поставщиков не могут управляться частными сеансами трассировки.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-137">Provider Groups cannot be controlled by private trace sessions.</span></span>
-   <span data-ttu-id="f5fa2-138">Имя события, идентификатор события и фильтры полезных данных неприменимы к группам поставщиков, так как они предполагают определенную информацию об отдельном поставщике.</span><span class="sxs-lookup"><span data-stu-id="f5fa2-138">Event Name, Event ID, and Payload filters are not applicable to Provider Groups as they assume specific information of an individual provider.</span></span>

 

 
