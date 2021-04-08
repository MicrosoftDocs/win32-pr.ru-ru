---
title: ЦЕНУМСЧ. CPP
description: В примере компонента поставщика перечисление объекта схемы использует методы из ценумсч. cpp, перечисленные в следующей таблице.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887580"
---
# <a name="cenumschcpp"></a><span data-ttu-id="f2c3d-103">ЦЕНУМСЧ. CPP</span><span class="sxs-lookup"><span data-stu-id="f2c3d-103">CENUMSCH.CPP</span></span>

<span data-ttu-id="f2c3d-104">В примере компонента поставщика перечисление объекта схемы использует методы из ценумсч. cpp, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-104">In the example provider component, the enumeration of a schema object uses the methods, from cenumsch.cpp, listed in the following table.</span></span>



| <span data-ttu-id="f2c3d-105">Метод</span><span class="sxs-lookup"><span data-stu-id="f2c3d-105">Method</span></span>                                        | <span data-ttu-id="f2c3d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f2c3d-106">Description</span></span>                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2c3d-107">**Ксампледссчемаенум:: Create**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-107">**CSampleDSSchemaEnum::Create**</span></span>               | <span data-ttu-id="f2c3d-108">Создайте объект, чтобы разрешить перечисление объекта класса схемы ADSI.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-108">Create an object to allow enumeration of an ADSI schema class object.</span></span>                                                |
| <span data-ttu-id="f2c3d-109">**Ксампледссчемаенум:: Ксампледссчемаенум**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span></span>  | <span data-ttu-id="f2c3d-110">Стандартный конструктор.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-110">Standard constructor.</span></span>                                                                                                |
| <span data-ttu-id="f2c3d-111">**Ксампледссчемаенум:: ~ Ксампледссчемаенум**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-111">**CSampleDSSchemaEnum::~CSampleDSSchemaEnum**</span></span> | <span data-ttu-id="f2c3d-112">Стандартный деструктор.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-112">Standard destructor.</span></span>                                                                                                 |
| <span data-ttu-id="f2c3d-113">**Ксампледссчемаенум:: Next**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-113">**CSampleDSSchemaEnum::Next**</span></span>                 | <span data-ttu-id="f2c3d-114">Извлечение указанного числа элементов из указанного объекта схемы.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-114">Retrieve the specified number of elements from the schema object indicated.</span></span>                                          |
| <span data-ttu-id="f2c3d-115">**Ксампледссчемаенум:: Енумобжектс**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-115">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="f2c3d-116">Управление получением указателей интерфейсов на объекты указанного типа объекта.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-116">Manage retrieving the interfaces pointers to the objects of the object type indicated.</span></span>                               |
| <span data-ttu-id="f2c3d-117">**Ксампледссчемаенум:: Енумобжектс**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-117">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="f2c3d-118">Управление получением указателей интерфейса на объекты типа объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-118">Manage retrieving the interface pointers to the objects of the default object type.</span></span>                                  |
| <span data-ttu-id="f2c3d-119">**Ксампледссчемаенум:: Енумклассес**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-119">**CSampleDSSchemaEnum::EnumClasses**</span></span>          | <span data-ttu-id="f2c3d-120">Управление получением указателей интерфейса только на объекты класса схемы, содержащиеся в этом объекте.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-120">Manage retrieving the interface pointers to only the schema class objects contained in this object.</span></span>                  |
| <span data-ttu-id="f2c3d-121">**Ксампледссчемаенум:: Жетклассобжект**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-121">**CSampleDSSchemaEnum::GetClassObject**</span></span>       | <span data-ttu-id="f2c3d-122">Получение определения следующего класса схемы; Если он найден, создайте объект класса схемы и возвратите указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-122">Retrieve the next schema class definition; if found, create a schema class object, and return the interface pointer.</span></span> |
| <span data-ttu-id="f2c3d-123">**Ксампледссчемаенум:: Енумпропертиес**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-123">**CSampleDSSchemaEnum::EnumProperties**</span></span>       | <span data-ttu-id="f2c3d-124">Управление получением указателей интерфейса на объекты свойств, которые содержатся только в этом объекте.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-124">Manage retrieving the interface pointers to the property objects only contained in this object.</span></span>                      |
| <span data-ttu-id="f2c3d-125">**Ксампледссчемаенум:: Жетпропертйобжект**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-125">**CSampleDSSchemaEnum::GetPropertyObject**</span></span>    | <span data-ttu-id="f2c3d-126">Получение определения следующего свойства; Если он найден, создайте объект класса схемы и возвратите указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-126">Retrieve the next property definition; if found, create a schema class object, and return the interface pointer.</span></span>     |
| <span data-ttu-id="f2c3d-127">**Ксампледссчемаенум:: Енумсинтаксес**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span></span>         | <span data-ttu-id="f2c3d-128">Управление получением указателей интерфейса на объекты синтаксиса, которые содержатся только в этом объекте.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-128">Manage retrieving the interface pointers to the syntax objects only contained in this object.</span></span>                        |
| <span data-ttu-id="f2c3d-129">**Ксампледссчемаенум:: Жетсинтаксобжект**</span><span class="sxs-lookup"><span data-stu-id="f2c3d-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span></span>      | <span data-ttu-id="f2c3d-130">Получите следующее определение синтаксиса. Если он найден, создайте объект класса схемы и возвратите указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f2c3d-130">Retrieve the next syntax definition; if found, create a schema class object, and return the interface pointer.</span></span>       |



 

 

 




