---
title: Свойства и атрибуты ADSI
description: Атрибуты иногда называют свойствами. Это может вызвать путаницу. В этой документации используются следующие определения свойств и атрибутов.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Свойства ADSI и атрибуты ADSI
- ADSI ADSI, использование, доступ к данным, свойствам и атрибутам и управление ими
- свойства ADSI
- атрибуты ADSI
- свойства ADSI, определение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654153"
---
# <a name="adsi-properties-and-attributes"></a><span data-ttu-id="36956-110">Свойства и атрибуты ADSI</span><span class="sxs-lookup"><span data-stu-id="36956-110">ADSI Properties and Attributes</span></span>

<span data-ttu-id="36956-111">Атрибуты иногда называют свойствами.</span><span class="sxs-lookup"><span data-stu-id="36956-111">Attributes are sometimes referred to as properties.</span></span> <span data-ttu-id="36956-112">Это может вызвать путаницу.</span><span class="sxs-lookup"><span data-stu-id="36956-112">This can cause confusion.</span></span> <span data-ttu-id="36956-113">В этой документации используются следующие определения свойств и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="36956-113">This documentation uses the following definitions for properties and attributes.</span></span>

<span data-ttu-id="36956-114">Свойства представляют собой именованные значения, связанные с программным объектом.</span><span class="sxs-lookup"><span data-stu-id="36956-114">Properties are named values associated with a programming object.</span></span> <span data-ttu-id="36956-115">Например, интерфейс [**iAds**](/windows/desktop/api/Iads/nn-iads-iads) предоставляет такие свойства, как [**класс**](iads-property-methods.md) и **имя**.</span><span class="sxs-lookup"><span data-stu-id="36956-115">For example, the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface exposes properties such as [**Class**](iads-property-methods.md) and **Name**.</span></span>

<span data-ttu-id="36956-116">Атрибуты — это данные, связанные с объектами в службе каталогов.</span><span class="sxs-lookup"><span data-stu-id="36956-116">Attributes are the data associated with objects in a directory service.</span></span> <span data-ttu-id="36956-117">Например, объект пользователя будет иметь атрибут **CN** , который содержит строку, представляющую общее или относительное различающееся имя объекта.</span><span class="sxs-lookup"><span data-stu-id="36956-117">For example, a user object will have an attribute called **cn** which contains a string that is the common or relative distinguished name of the object.</span></span> <span data-ttu-id="36956-118">Атрибуты доступны через методы интерфейса ADSI, такие как [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. Постановка**](/windows/desktop/api/Iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="36956-118">Attributes are accessible through ADSI interface methods such as [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span></span>

<span data-ttu-id="36956-119">Дополнительные сведения о свойствах и атрибутах ADSI см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="36956-119">For more information about ADSI properties and attributes, see:</span></span>

-   [<span data-ttu-id="36956-120">Кэш атрибутов ADSI</span><span class="sxs-lookup"><span data-stu-id="36956-120">The ADSI Attribute Cache</span></span>](the-adsi-attribute-cache.md)
-   [<span data-ttu-id="36956-121">Сравнение одного и нескольких атрибутов значений</span><span class="sxs-lookup"><span data-stu-id="36956-121">Single vs. Multiple Value Attributes</span></span>](single-vs--multiple-value-attributes.md)
-   [<span data-ttu-id="36956-122">Active Directory операционные атрибуты</span><span class="sxs-lookup"><span data-stu-id="36956-122">Active Directory Operational Attributes</span></span>](active-directory-operational-attributes.md)

 

 




