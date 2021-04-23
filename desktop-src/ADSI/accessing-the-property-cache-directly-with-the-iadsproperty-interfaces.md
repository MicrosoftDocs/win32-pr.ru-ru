---
title: Доступ к кэшу свойств с помощью интерфейсов Иадспроперти
description: Интерфейсы Иадспроперти состоят из Иадспропертилист, Иадспропертентри и Иадспропертивалуе.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Доступ к кэшу свойств напрямую с интерфейсами Иадспроперти ADSI
- интерфейс ADSI кэша свойств
- кэширование свойств ADSI с использованием интерфейсов Иадспроперти для доступа к кэшу свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48cd8675f4c439e3d3597e2d4fa59dac57e0896
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/04/2019
ms.locfileid: "103987105"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a><span data-ttu-id="ae767-106">Доступ к кэшу свойств с помощью интерфейсов Иадспроперти</span><span class="sxs-lookup"><span data-stu-id="ae767-106">Accessing Property Cache with IADsProperty Interfaces</span></span>

<span data-ttu-id="ae767-107">Интерфейсы [**иадспроперти**](/windows/desktop/api/Iads/nn-iads-iadsproperty) состоят из [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**иадспропертентри**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)и [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue).</span><span class="sxs-lookup"><span data-stu-id="ae767-107">The [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interfaces consist of [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue).</span></span> <span data-ttu-id="ae767-108">Эти интерфейсы предоставляют методы для прямого доступа к свойствам кэша объектов и управления ими.</span><span class="sxs-lookup"><span data-stu-id="ae767-108">These interfaces provide methods to directly access and manipulate the properties of an object cache.</span></span> <span data-ttu-id="ae767-109">Свойство называется записью свойства и соответствует атрибуту, определенному в схеме.</span><span class="sxs-lookup"><span data-stu-id="ae767-109">A property is known as a property entry and corresponds to an attribute defined in the schema.</span></span> <span data-ttu-id="ae767-110">Запись свойства может иметь одно или несколько значений свойств.</span><span class="sxs-lookup"><span data-stu-id="ae767-110">A property entry can have one, or many, property values.</span></span> <span data-ttu-id="ae767-111">Набор записей свойств организован как список свойств.</span><span class="sxs-lookup"><span data-stu-id="ae767-111">A set of property entries are organized as a property list.</span></span>

<span data-ttu-id="ae767-112">Интерфейс [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) управляет списком свойств объекта ADSI.</span><span class="sxs-lookup"><span data-stu-id="ae767-112">The [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface manages the property list of an ADSI object.</span></span> <span data-ttu-id="ae767-113">Интерфейс [**иадспропертентри**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) выполняет эту операцию для записи свойства.</span><span class="sxs-lookup"><span data-stu-id="ae767-113">The [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface performs this operation for a property entry.</span></span> <span data-ttu-id="ae767-114">Аналогичным образом интерфейс [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) представляет одно или несколько значений свойств.</span><span class="sxs-lookup"><span data-stu-id="ae767-114">Similarly, the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interface represents one, or more, property values.</span></span> <span data-ttu-id="ae767-115">Вместе они предоставляют пользователям механизм:</span><span class="sxs-lookup"><span data-stu-id="ae767-115">Together, they provide a mechanism for users to:</span></span>

-   <span data-ttu-id="ae767-116">Работать непосредственно с кэшем свойств.</span><span class="sxs-lookup"><span data-stu-id="ae767-116">Work directly with the property cache.</span></span>
-   <span data-ttu-id="ae767-117">Работа с каталогами, которые не содержат схемы, например сервер LDAP версии 2.</span><span class="sxs-lookup"><span data-stu-id="ae767-117">Work with directories that do not contain schemas, such as an LDAP version 2 server.</span></span>

<span data-ttu-id="ae767-118">Интерфейсы [**иадспроперти**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* работают строго в кэше свойств и не пытаются взаимодействовать с сервером для получения или изменения данных в постоянном хранилище.</span><span class="sxs-lookup"><span data-stu-id="ae767-118">The [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)\* interfaces operate strictly on the property cache and do not make any attempt to cooperate with the server to retrieve or modify the data in the persistent store.</span></span> <span data-ttu-id="ae767-119">Таким образом, эти интерфейсы используются только для проверки и управления свойствами в клиентском кэше.</span><span class="sxs-lookup"><span data-stu-id="ae767-119">As such, these interfaces are used only to examine and manipulate properties in the client cache.</span></span> <span data-ttu-id="ae767-120">Перед использованием этих интерфейсов необходимо явно вызвать метод [**iAds::**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) GetObject или метод [**iAds:: жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) , чтобы загрузить свойства объекта в кэш, если кэш не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="ae767-120">Before using these interfaces, you must call the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method or the [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method explicitly to load the object properties into the cache, if the cache has not been initialized.</span></span> <span data-ttu-id="ae767-121">После вызова методов этих интерфейсов необходимо вызвать функцию [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , чтобы сохранить изменения в базовом хранилище каталога.</span><span class="sxs-lookup"><span data-stu-id="ae767-121">After calling the methods of these interfaces, you must call [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) to persist the changes to the underlying directory store.</span></span>

<span data-ttu-id="ae767-122">Дополнительные сведения и пример кода, который можно использовать для реализации этих интерфейсов, см. в разделе [пример кода для использования интерфейсов иадспроперти для доступа к кэшу свойств](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).</span><span class="sxs-lookup"><span data-stu-id="ae767-122">For more information and a code example that can used to implement these interfaces, see [Example Code for Using IADsProperty Interfaces to Access the Property Cache](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).</span></span>

 

 




