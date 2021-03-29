---
title: Поставщики служб ADSI
description: В этом разделе приводятся общие сведения о поставщиках служб ADSI, предоставляемых на сервере.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, поставщики услуг
- Поставщики услуг ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654348"
---
# <a name="adsi-service-providers"></a><span data-ttu-id="a4ce5-105">Поставщики служб ADSI</span><span class="sxs-lookup"><span data-stu-id="a4ce5-105">ADSI Service Providers</span></span>

<span data-ttu-id="a4ce5-106">ADSI включает поставщики услуг, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-106">ADSI includes the service providers listed in the following table.</span></span>



| <span data-ttu-id="a4ce5-107">Поставщик службы</span><span class="sxs-lookup"><span data-stu-id="a4ce5-107">Service provider</span></span> | <span data-ttu-id="a4ce5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a4ce5-108">Description</span></span>                                                                                | <span data-ttu-id="a4ce5-109">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="a4ce5-109">For more information</span></span>                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a4ce5-110">LDAP</span><span class="sxs-lookup"><span data-stu-id="a4ce5-110">LDAP</span></span><br/>  | <span data-ttu-id="a4ce5-111">Реализация пространства имен, совместимая с протоколом упрощенного доступа к каталогу.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-111">Namespace implementation compatible with Lightweight Directory Access Protocol.</span></span><br/> | [<span data-ttu-id="a4ce5-112">Поставщик LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="a4ce5-112">ADSI LDAP Provider</span></span>](adsi-ldap-provider.md)<br/>   |
| <span data-ttu-id="a4ce5-113">WinNT</span><span class="sxs-lookup"><span data-stu-id="a4ce5-113">WinNT</span></span><br/> | <span data-ttu-id="a4ce5-114">Реализация пространства имен, совместимая с Windows.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-114">Namespace implementation compatible with Windows.</span></span><br/>                               | [<span data-ttu-id="a4ce5-115">Поставщик ADSI WinNT</span><span class="sxs-lookup"><span data-stu-id="a4ce5-115">ADSI WinNT Provider</span></span>](adsi-winnt-provider.md)<br/> |



 

<span data-ttu-id="a4ce5-116">Другие поставщики служб входят в состав продуктов, отличных от интерфейсов ADSI.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-116">Other service providers are included as part of products other than ADSI.</span></span> <span data-ttu-id="a4ce5-117">Ниже перечислены поставщики служб ADSI, реализованные корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-117">The following are the ADSI service providers implemented by Microsoft.</span></span>



| <span data-ttu-id="a4ce5-118">Поставщик службы</span><span class="sxs-lookup"><span data-stu-id="a4ce5-118">Service provider</span></span> | <span data-ttu-id="a4ce5-119">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="a4ce5-119">For more information</span></span>                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ce5-120">Службы IIS</span><span class="sxs-lookup"><span data-stu-id="a4ce5-120">IIS</span></span><br/>   | <span data-ttu-id="a4ce5-121">[Архитектура поставщика IIS ADSI](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="a4ce5-121">[IIS ADSI Provider Architecture](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span></span><br/> |



 

<span data-ttu-id="a4ce5-122">Методы и методы свойств, предоставляемые интерфейсами ADSI, не поддерживаются каждым поставщиком служб.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-122">The methods and property methods exposed by ADSI interfaces are not supported by every service provider.</span></span> <span data-ttu-id="a4ce5-123">Поскольку разные службы каталогов зависят от типов объектов и свойств, используют разные протоколы и проверку подлинности, интерфейсы ADSI предназначены для беспрепятственной работы с поддерживаемыми поставщиками служб.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-123">Because different directory services vary in the types of objects and properties stored, use different protocols, and authentication, ADSI is designed to work seamlessly with supported service providers.</span></span> <span data-ttu-id="a4ce5-124">Таким образом, существуют интерфейсы, методы и методы свойств, работающие с одним поставщиком услуг, например LDAP, которые могут не работать на другом, например в WinNT.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-124">Thus, there are interfaces, methods, and property methods that work with one service provider, such as LDAP, that may not work on another, such as WinNT.</span></span>

<span data-ttu-id="a4ce5-125">В этом разделе содержатся сведения о конкретном поставщике, такие как формат ADsPath, список объектов ADSI, используемых для данного поставщика услуг, а также сведения о типе данных и синтаксисе поставщиков услуг, входящих в состав ADSI.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-125">This section contains provider-specific information, such as the ADsPath format, a listing of ADSI objects used for that service provider, and data type and syntax information for the service providers included with ADSI.</span></span> <span data-ttu-id="a4ce5-126">Также имеется сводное описание интерфейсов ADSI, поддерживаемых каждым поставщиком, входящим в состав ADSI.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-126">There is also a summary description of ADSI interfaces supported by each provider included with ADSI.</span></span>

<span data-ttu-id="a4ce5-127">В ADSI различные поставщики связаны с различными библиотеками DLL.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-127">In ADSI, different providers are associated with different DLLs.</span></span> <span data-ttu-id="a4ce5-128">Поставщик LDAP связан с Adsldp.dll, Adsldpc.dll и Adsmsext.dll.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-128">The LDAP provider is associated with Adsldp.dll, Adsldpc.dll, and Adsmsext.dll.</span></span> <span data-ttu-id="a4ce5-129">Поставщик WinNT связан с Adsnt.dll.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-129">The WinNT provider is associated with Adsnt.dll.</span></span> <span data-ttu-id="a4ce5-130">Поставщик МАРШРУТИЗАТОРа связан с Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-130">The ROUTER provider is associated with Activeds.dll.</span></span>

> [!Note]  
> <span data-ttu-id="a4ce5-131">Не следует рассчитывать, что поставщики ADSI по умолчанию являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-131">Do not assume that default ADSI providers are thread-safe.</span></span> <span data-ttu-id="a4ce5-132">Многопоточные разработчики приложений должны координировать доступ между потоками посредством правильного использования объектов синхронизации, таких как семафоры, мьютексы, критические разделы и т. д.</span><span class="sxs-lookup"><span data-stu-id="a4ce5-132">Multithreaded application developers should coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

<span data-ttu-id="a4ce5-133">Дополнительные сведения о поставщиках служб ADSI см. в разделе Поддержка [маршрутизатора ADSI](adsi-router.md) и [поставщика интерфейсов ADSI](provider-support-of-adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a4ce5-133">For more information about ADSI service providers, see [ADSI Router](adsi-router.md) and [Provider Support of ADSI interfaces](provider-support-of-adsi-interfaces.md).</span></span>

 

