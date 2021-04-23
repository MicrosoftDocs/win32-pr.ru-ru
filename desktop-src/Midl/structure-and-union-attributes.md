---
title: Атрибуты структуры и объединения
description: Используйте атрибуты Switch \_ \, чтобы указать характеристики объединения в удаленном вызове процедуры. Используйте атрибут Ignore, чтобы назначить определенную структуру или члены объединения в качестве локальных для клиентского приложения.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL MIDL, атрибуты, структура и объединение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486733"
---
# <a name="structure-and-union-attributes"></a><span data-ttu-id="0f05b-105">Атрибуты структуры и объединения</span><span class="sxs-lookup"><span data-stu-id="0f05b-105">Structure and Union Attributes</span></span>

<span data-ttu-id="0f05b-106">Используйте атрибуты **\_ переключателя** , \* чтобы указать характеристики объединения в удаленном вызове процедуры.</span><span class="sxs-lookup"><span data-stu-id="0f05b-106">Use the **switch\_**\* attributes to specify the characteristic of a union in a remote procedure call.</span></span> <span data-ttu-id="0f05b-107">Используйте атрибут [**Ignore**](ignore.md) , чтобы назначить определенную структуру или члены объединения в качестве локальных для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="0f05b-107">Use the [**ignore**](ignore.md) attribute to designate certain structure or union members as local to the client application.</span></span>



| <span data-ttu-id="0f05b-108">attribute</span><span class="sxs-lookup"><span data-stu-id="0f05b-108">Attribute</span></span>                           | <span data-ttu-id="0f05b-109">Использование</span><span class="sxs-lookup"><span data-stu-id="0f05b-109">Usage</span></span>                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f05b-110">**switch**</span><span class="sxs-lookup"><span data-stu-id="0f05b-110">**switch**</span></span>](switch.md)            | <span data-ttu-id="0f05b-111">Выбирает discriminant для инкапсулированного объединения.</span><span class="sxs-lookup"><span data-stu-id="0f05b-111">Selects the discriminant for an encapsulated union.</span></span>                                                                           |
| [<span data-ttu-id="0f05b-112">**параметр \_ имеет**</span><span class="sxs-lookup"><span data-stu-id="0f05b-112">**switch\_is**</span></span>](switch-is.md)     | <span data-ttu-id="0f05b-113">Определяет discriminant для неинкапсулированного объединения.</span><span class="sxs-lookup"><span data-stu-id="0f05b-113">Identifies the discriminant for a nonencapsulated union.</span></span>                                                                      |
| [<span data-ttu-id="0f05b-114">**Тип коммутатора \_**</span><span class="sxs-lookup"><span data-stu-id="0f05b-114">**switch\_type**</span></span>](switch-type.md) | <span data-ttu-id="0f05b-115">Определяет тип discriminant для неинкапсулированного объединения.</span><span class="sxs-lookup"><span data-stu-id="0f05b-115">Identifies the type of the discriminant for a nonencapsulated union.</span></span>                                                          |
| [<span data-ttu-id="0f05b-116">**обращать**</span><span class="sxs-lookup"><span data-stu-id="0f05b-116">**ignore**</span></span>](ignore.md)            | <span data-ttu-id="0f05b-117">Указывает, что указатель, содержащийся в структуре или объединении, и объект, указанный указателем, не передаются.</span><span class="sxs-lookup"><span data-stu-id="0f05b-117">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span> |



 

<span data-ttu-id="0f05b-118">Можно также использовать атрибуты « [массив» и «размер указателя](array-and-sized-pointer-attributes.md) » для определения характеристик элементов структуры или объединения.</span><span class="sxs-lookup"><span data-stu-id="0f05b-118">You can also use the [array and sized pointer attributes](array-and-sized-pointer-attributes.md) to specify characteristics of structure or union members.</span></span>

 

 




