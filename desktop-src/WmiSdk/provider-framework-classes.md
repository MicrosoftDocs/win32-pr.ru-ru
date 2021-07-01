---
description: Сведения о классах WMI C++, которые являются частью платформы поставщика WMI и теперь считаются в конечном состоянии.
ms.assetid: 062a7724-0589-4e9d-af7a-39fd9c08e40b
ms.tgt_platform: multiple
title: Классы инфраструктуры поставщиков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf4ef94b25e51b7f012987552babd30a93e7792
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120449"
---
# <a name="provider-framework-classes"></a><span data-ttu-id="7c6fb-103">Классы инфраструктуры поставщиков</span><span class="sxs-lookup"><span data-stu-id="7c6fb-103">Provider Framework Classes</span></span>

<span data-ttu-id="7c6fb-104">\[Классы C++ с WMI, которые являются частью инфраструктуры поставщика WMI, теперь считаются окончательными, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-104">\[WMI C++ classes that are part of the WMI Provider Framework are are now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="7c6fb-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="7c6fb-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="7c6fb-106">Платформа поставщика реализует следующие классы.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-106">The provider framework implements the following classes.</span></span>



| <span data-ttu-id="7c6fb-107">Класс Framework</span><span class="sxs-lookup"><span data-stu-id="7c6fb-107">Framework class</span></span>                                | <span data-ttu-id="7c6fb-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7c6fb-108">Description</span></span>                                                                                                                                                                                                         |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c6fb-109">**кфрамеворккуери**</span><span class="sxs-lookup"><span data-stu-id="7c6fb-109">**CFrameworkQuery**</span></span>](/windows/desktop/api/FrQuery/nl-frquery-cframeworkquery)     | <span data-ttu-id="7c6fb-110">Содержит методы для обработки запросов.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-110">Contains methods for query processing.</span></span>                                                                                                                                                                              |
| [<span data-ttu-id="7c6fb-111">**CInstance**</span><span class="sxs-lookup"><span data-stu-id="7c6fb-111">**CInstance**</span></span>](/windows/desktop/api/Instance/nl-instance-cinstance)                 | <span data-ttu-id="7c6fb-112">Содержит методы для установки и получения свойств и является инкапсуляцией интерфейса [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="7c6fb-112">Contains methods to set and retrieve properties and is an encapsulation of the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface.</span></span> <span data-ttu-id="7c6fb-113">Разработчику не нужно напрямую обращаться к методам **ивбемклассобжект** .</span><span class="sxs-lookup"><span data-stu-id="7c6fb-113">Implementer should not have to access **IWbemClassObject** methods directly.</span></span> |
| [<span data-ttu-id="7c6fb-114">**ксреадбасе**</span><span class="sxs-lookup"><span data-stu-id="7c6fb-114">**CThreadBase**</span></span>](/windows/desktop/api/ThrdBase/nl-thrdbase-cthreadbase)             | <span data-ttu-id="7c6fb-115">Базовый класс, предоставляющий механизмы безопасности внутреннего потока для платформы поставщика WMI.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-115">A base class that supplies the internal thread safety mechanisms for the WMI Provider Framework.</span></span>                                                                                                                    |
| [<span data-ttu-id="7c6fb-116">**квбемглуефактори**</span><span class="sxs-lookup"><span data-stu-id="7c6fb-116">**CWbemGlueFactory**</span></span>](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemgluefactory)   | <span data-ttu-id="7c6fb-117">Часть платформы поставщика WMI.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-117">Part of the WMI Provider Framework.</span></span> <span data-ttu-id="7c6fb-118">Инфраструктура поставщика реализует методы этого интерфейса для внутреннего создания новых экземпляров классов для поставщика.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-118">The Provider Framework implements methods of this interface internally to create new instances of classes for the provider.</span></span>                                                     |
| [<span data-ttu-id="7c6fb-119">**квбемпровидерглуе**</span><span class="sxs-lookup"><span data-stu-id="7c6fb-119">**CWbemProviderGlue**</span></span>](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) | <span data-ttu-id="7c6fb-120">Реализует [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и методы, которые управляют загрузкой и выгрузкой поставщика платформы.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-120">Implements [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and methods that control the loading and unloading of the framework provider.</span></span>                                                                             |
| [<span data-ttu-id="7c6fb-121">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="7c6fb-121">**Provider**</span></span>](/windows/desktop/api/Provider/nl-provider-provider)                   | <span data-ttu-id="7c6fb-122">Содержит вспомогательные функции и предоставляет реализации по умолчанию методов [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span><span class="sxs-lookup"><span data-stu-id="7c6fb-122">Contains helper functions and provides default implementations of the methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span></span>                                                                                            |



 

<span data-ttu-id="7c6fb-123">Обратите внимание, что многие методы платформы используют параметры [**чстринг**](chstring.md) .</span><span class="sxs-lookup"><span data-stu-id="7c6fb-123">Note that many of the framework methods use [**CHString**](chstring.md) parameters.</span></span> <span data-ttu-id="7c6fb-124">**Чстринг** поддерживает многие те же методы и свойства, что и Microsoft Foundation Classes (MFC), но без затрат на MFC.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-124">**CHString** supports many of the same methods and properties as the Microsoft Foundation Classes (MFC), but without the overhead of MFC.</span></span> <span data-ttu-id="7c6fb-125">Дополнительные сведения о **чстринг** см. в разделе **Справочник по классам чстринг**.</span><span class="sxs-lookup"><span data-stu-id="7c6fb-125">For more information about **CHString**, see **CHString Class Reference**.</span></span>

 

 
