---
title: ЦЕНУМНС. CPP
description: В примере компонента поставщика перечисление объекта пространства имен использует методы из ценумнс. cpp, перечисленные в следующей таблице.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654345"
---
# <a name="cenumnscpp"></a><span data-ttu-id="95818-103">ЦЕНУМНС. CPP</span><span class="sxs-lookup"><span data-stu-id="95818-103">CENUMNS.CPP</span></span>

<span data-ttu-id="95818-104">В примере компонента поставщика перечисление объекта пространства имен использует методы из ценумнс. cpp, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="95818-104">In the example provider component, the enumeration of a namespace object uses the methods, from cenumns.cpp, listed in the following table.</span></span>



| <span data-ttu-id="95818-105">Метод</span><span class="sxs-lookup"><span data-stu-id="95818-105">Method</span></span>                                              | <span data-ttu-id="95818-106">Описание</span><span class="sxs-lookup"><span data-stu-id="95818-106">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95818-107">**Ксампледснамеспацеенум:: Create**</span><span class="sxs-lookup"><span data-stu-id="95818-107">**CSampleDSNamespaceEnum::Create**</span></span>                  | <span data-ttu-id="95818-108">Создайте объект, чтобы разрешить перечисление объекта пространства имен ADS.</span><span class="sxs-lookup"><span data-stu-id="95818-108">Create an object to allow enumeration of an ADS namespace object.</span></span>                                                                                         |
| <span data-ttu-id="95818-109">**Ксампледснамеспацеенум:: Ксампледснамеспацеенум**</span><span class="sxs-lookup"><span data-stu-id="95818-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span></span>  | <span data-ttu-id="95818-110">Стандартный конструктор.</span><span class="sxs-lookup"><span data-stu-id="95818-110">Standard constructor.</span></span>                                                                                                                                     |
| <span data-ttu-id="95818-111">**Ксампледснамеспацеенум:: ~ Ксампледснамеспацеенум**</span><span class="sxs-lookup"><span data-stu-id="95818-111">**CSampleDSNamespaceEnum::~CSampleDSNamespaceEnum**</span></span> | <span data-ttu-id="95818-112">Стандартный деструктор.</span><span class="sxs-lookup"><span data-stu-id="95818-112">Standard destructor.</span></span>                                                                                                                                      |
| <span data-ttu-id="95818-113">**Ксампледснамеспацеенум:: Next**</span><span class="sxs-lookup"><span data-stu-id="95818-113">**CSampleDSNamespaceEnum::Next**</span></span>                    | <span data-ttu-id="95818-114">Извлечение указанного числа элементов из указанного объекта пространства имен.</span><span class="sxs-lookup"><span data-stu-id="95818-114">Retrieve the specified number of elements from the namespace object indicated.</span></span>                                                                            |
| <span data-ttu-id="95818-115">**Ксампледснамеспацеенум:: Енумобжектс**</span><span class="sxs-lookup"><span data-stu-id="95818-115">**CSampleDSNamespaceEnum::EnumObjects**</span></span>             | <span data-ttu-id="95818-116">Управление получением указателей интерфейса на объекты.</span><span class="sxs-lookup"><span data-stu-id="95818-116">Manage retrieving the interface pointers to the objects.</span></span>                                                                                                  |
| <span data-ttu-id="95818-117">**Ксампледснамеспацеенум:: Фетчобжектс**</span><span class="sxs-lookup"><span data-stu-id="95818-117">**CSampleDSNamespaceEnum::FetchObjects**</span></span>            | <span data-ttu-id="95818-118">Получение набора указателей [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="95818-118">Fetch the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers.</span></span>                                                                          |
| <span data-ttu-id="95818-119">**Ксампледснамеспацеенум:: Фетчнекстобжект**</span><span class="sxs-lookup"><span data-stu-id="95818-119">**CSampleDSNamespaceEnum::FetchNextObject**</span></span>         | <span data-ttu-id="95818-120">Получить следующий объект.</span><span class="sxs-lookup"><span data-stu-id="95818-120">Fetch the next object.</span></span> <span data-ttu-id="95818-121">Если он найден, создайте универсальный объект Active Directory и извлеките его указатель [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="95818-121">If found, create a generic Active Directory object and retrieve its [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |



 

 

 