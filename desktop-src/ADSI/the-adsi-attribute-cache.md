---
title: Кэш атрибутов ADSI
description: Объектная модель ADSI предоставляет кэш атрибутов на стороне клиента для каждого объекта ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- Кэш ADSI для кэша атрибутов ADSI
- ADSI ADSI, использование, доступ к данным и управление ими с помощью ADSI, кэш атрибутов
- атрибуты ADSI, кэширование атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772911"
---
# <a name="the-adsi-attribute-cache"></a><span data-ttu-id="c3d4c-106">Кэш атрибутов ADSI</span><span class="sxs-lookup"><span data-stu-id="c3d4c-106">The ADSI Attribute Cache</span></span>

<span data-ttu-id="c3d4c-107">Объектная модель ADSI предоставляет кэш атрибутов на стороне клиента для каждого объекта ADSI.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-107">The ADSI object model provides a client-side attribute cache for each ADSI object.</span></span> <span data-ttu-id="c3d4c-108">Кэш атрибутов сравним с таблицей в памяти, которая содержит имена и значения большинства загруженных атрибутов объектов.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-108">The attribute cache is comparable to a table in memory that contains the names and values of most object attributes that have been downloaded.</span></span> <span data-ttu-id="c3d4c-109">Некоторые атрибуты, такие как операционные атрибуты, не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-109">Some attributes, such as operational attributes, are not cached.</span></span> <span data-ttu-id="c3d4c-110">ADSI использует кэширование свойств для повышения производительности манипуляций с атрибутами и добавления возможностей транзакций для операций чтения и записи атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-110">ADSI uses property caching to enhance the performance of attribute manipulation and add transactioning capability for attribute read and write operations.</span></span> <span data-ttu-id="c3d4c-111">Эта возможность важна для клиентов, написанных на языках, которые не имеют собственного механизма пакетной обработки для настройки атрибутов, таких как система разработки Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-111">This capability is critical for clients written in languages that have no native batching mechanism for setting attributes, such as Microsoft Visual Basic development system.</span></span> <span data-ttu-id="c3d4c-112">Без кэша свойств ADSI такие клиенты должны иметь доступ к серверу при каждом считывании или записи атрибута.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-112">Without the ADSI property cache, such clients would have to access the server every time an attribute is read or written.</span></span>

<span data-ttu-id="c3d4c-113">Когда объект создается или сначала привязан к, кэш свойств для объекта пуст.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-113">When an object is created or first bound to, the property cache for the object is empty.</span></span> <span data-ttu-id="c3d4c-114">Когда вызывается метод [**iAds::-info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) , ADSI загружает запрошенные атрибуты объекта из базовой службы каталогов в локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-114">When the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called, ADSI loads the requested attributes for the object from the underlying directory service into the local cache.</span></span> <span data-ttu-id="c3d4c-115">Когда считывается значение определенного атрибута и кэш пуст, ADSI делает неявный вызов метода **iAds::-info** .</span><span class="sxs-lookup"><span data-stu-id="c3d4c-115">When a specific attribute value is read and the cache is empty, ADSI makes an implicit call to the **IADs::GetInfo** method.</span></span> <span data-ttu-id="c3d4c-116">При заполнении кэша все операции чтения атрибута работают только с содержимым кэша.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-116">When the cache is filled, all attribute read operations work on the contents of the cache only.</span></span>

<span data-ttu-id="c3d4c-117">При записи значения атрибута новое значение сохраняется в локальном кэше до тех пор, пока не будет вызван метод [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="c3d4c-117">When an attribute value is written, the new value is stored in the local cache until the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span> <span data-ttu-id="c3d4c-118">При вызове метода **iAds:: сетинфо** атрибуты в кэше фиксируются в базовой службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-118">When the **IADs::SetInfo** method is called, the attributes in the cache are committed to the underlying directory service.</span></span> <span data-ttu-id="c3d4c-119">После вызова метода **iAds:: сетинфо** значения остаются в кэше до тех пор, пока не будет явно обновлен другой вызов метода [**iAds::-info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .</span><span class="sxs-lookup"><span data-stu-id="c3d4c-119">After the **IADs::SetInfo** method is called, the values remain in the cache until explicitly refreshed with another call to the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3d4c-120">Метод [**iAds::**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) OutAttribute следует использовать аккуратно, так как этот метод всегда перезаписывает значения атрибутов в кэше из базовой службы каталогов, даже если кэшированное значение было изменено.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-120">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method must be used carefully because this method will always overwrite the attribute values in the cache from the underlying directory service, even if the cached value has been changed.</span></span> <span data-ttu-id="c3d4c-121">То есть он перезапишет значения атрибутов, которые были изменены в кэше, но не зафиксированы в базовой службе каталогов с помощью вызова метода [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="c3d4c-121">That is, it will overwrite attribute values that have been changed in the cache, but not committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>

 

<span data-ttu-id="c3d4c-122">На следующем рисунке показаны различные методы, используемые при работе с кэшем.</span><span class="sxs-lookup"><span data-stu-id="c3d4c-122">The following figure shows the different methods used to operate on the cache.</span></span>

![кэш атрибутов ADSI](images/ds2propc.png)

 

 




