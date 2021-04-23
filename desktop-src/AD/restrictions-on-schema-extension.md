---
title: Ограничения на расширение схемы
description: Чтобы снизить вероятность изменения схемы одним приложением, которое нарушает другие приложения и поддерживает согласованность схемы, домен Active Directory службы применяют ограничения на тип изменений схемы, которые может выполнять приложение или пользователь.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773103"
---
# <a name="restrictions-on-schema-extension"></a><span data-ttu-id="06892-103">Ограничения на расширение схемы</span><span class="sxs-lookup"><span data-stu-id="06892-103">Restrictions on Schema Extension</span></span>

<span data-ttu-id="06892-104">Чтобы снизить вероятность изменения схемы одним приложением, которое нарушает другие приложения и поддерживает согласованность схемы, домен Active Directory службы применяют ограничения на тип изменений схемы, которые может выполнять приложение или пользователь.</span><span class="sxs-lookup"><span data-stu-id="06892-104">In order to reduce the possibility of schema changes by one application breaking other applications and to maintain schema consistency, Active Directory Domain Services enforce restrictions on the type of schema changes that an application or user is allowed to make.</span></span>

<span data-ttu-id="06892-105">Ограничения накладываются только на изменение существующих объектов схемы.</span><span class="sxs-lookup"><span data-stu-id="06892-105">The restrictions are imposed only on modification of existing schema objects.</span></span> <span data-ttu-id="06892-106">Схема разбита на две категории.</span><span class="sxs-lookup"><span data-stu-id="06892-106">The schema is categorized into two categories.</span></span> <span data-ttu-id="06892-107">Объекты схемы, поставляемые с Windows 2000 в базовой схеме, относятся к категории 1.</span><span class="sxs-lookup"><span data-stu-id="06892-107">The schema objects that ship with Windows 2000 in the base schema belong to Category 1.</span></span> <span data-ttu-id="06892-108">Все объекты схемы, добавленные позже другими приложениями или пользователями через динамическое расширение схемы, относятся к категории 2.</span><span class="sxs-lookup"><span data-stu-id="06892-108">Any schema objects added later by other applications or users through dynamic schema extension belong to Category 2.</span></span> <span data-ttu-id="06892-109">Категория объекта схемы может определяться битом 0x10, установленным в атрибуте **systemFlags** в объекте **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="06892-109">The category of a schema object can be determined by the 0x10 bit set in the **systemFlags** attribute on the **classSchema** object.</span></span> <span data-ttu-id="06892-110">Этот бит задается только для объектов Category 1 и не может быть изменен, а также не может быть задан для любого объекта категории 2.</span><span class="sxs-lookup"><span data-stu-id="06892-110">This bit is only set on Category 1 objects, and cannot be altered, nor can it be set on any Category 2 object.</span></span>

<span data-ttu-id="06892-111">Атрибут **systemFlags** используется внутренне службами домен Active Directory Services для обнаружения особых характеристик объектов "Infrastructure" в базовой схеме.</span><span class="sxs-lookup"><span data-stu-id="06892-111">The **systemFlags** attribute is used internally by Active Directory Domain Services to identify special characteristics of "infrastructure" objects in the base schema.</span></span> <span data-ttu-id="06892-112">Кроме определения объектов Category 1, элемент управления **systemFlags** управляет возможностью перемещения, удаления или переименования объекта.</span><span class="sxs-lookup"><span data-stu-id="06892-112">In addition to identifying Category 1 objects, **systemFlags** controls whether an object can be moved, deleted, or renamed.</span></span> <span data-ttu-id="06892-113">Эти операции запрещаются для выполнения объектов, от которых зависит Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="06892-113">These operations are prevented for objects that Windows 2000 depends on to run.</span></span>

<span data-ttu-id="06892-114">Для любых объектов схемы, Категория 1 или 2, домен Active Directory служб накладывают следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="06892-114">On any schema objects, Category 1 or 2, Active Directory Domain Services impose the following restrictions:</span></span>

-   <span data-ttu-id="06892-115">Нельзя добавить новый **mustContain** в класс (напрямую или через наследование путем добавления вспомогательного класса).</span><span class="sxs-lookup"><span data-stu-id="06892-115">You cannot add a new **mustContain** to a class (directly or through inheritance by adding an auxiliary class).</span></span>
-   <span data-ttu-id="06892-116">Удалить **mustContain** класса (напрямую или через наследование) нельзя.</span><span class="sxs-lookup"><span data-stu-id="06892-116">You cannot delete any **mustContain** of the class (directly or through inheritance).</span></span>

<span data-ttu-id="06892-117">Кроме того, для объектов схемы категории 1 накладываются следующие дополнительные ограничения.</span><span class="sxs-lookup"><span data-stu-id="06892-117">In addition, the following additional restrictions are imposed on Category 1 schema objects:</span></span>

-   <span data-ttu-id="06892-118">Нельзя изменить следующие атрибуты атрибута Category 1:</span><span class="sxs-lookup"><span data-stu-id="06892-118">You cannot change the following attributes of a Category 1 attribute:</span></span>

    -   <span data-ttu-id="06892-119">**ранжеловер** и **ранжеуппер** (диапазон значений).</span><span class="sxs-lookup"><span data-stu-id="06892-119">**rangeLower** and **rangeUpper** (value range).</span></span>
    -   <span data-ttu-id="06892-120">**аттрибутесекуритигуид** (определяет, к какому свойству принадлежит данный атрибут, если он есть).</span><span class="sxs-lookup"><span data-stu-id="06892-120">**attributeSecurityGuid** (determines which property set the attribute belongs in, if any).</span></span>

-   <span data-ttu-id="06892-121">Нельзя изменить **дефаултобжекткатегори** класса Category 1.</span><span class="sxs-lookup"><span data-stu-id="06892-121">You cannot change the **defaultObjectCategory** of a Category 1 class.</span></span>
-   <span data-ttu-id="06892-122">Нельзя изменить **objectCategory** любого экземпляра класса Category 1.</span><span class="sxs-lookup"><span data-stu-id="06892-122">You cannot change the **objectCategory** of any instance of a Category 1 class.</span></span>
-   <span data-ttu-id="06892-123">Невозможно сделать класс или атрибут категории 1 уничтоженными.</span><span class="sxs-lookup"><span data-stu-id="06892-123">You cannot make a Category 1 class or attribute defunct.</span></span>
-   <span data-ttu-id="06892-124">Невозможно изменить атрибут **lDAPDisplayName** класса или атрибута категории 1.</span><span class="sxs-lookup"><span data-stu-id="06892-124">You cannot change the **lDAPDisplayName** of a Category 1 class or attribute.</span></span>
-   <span data-ttu-id="06892-125">Нельзя переименовать класс или атрибут категории 1.</span><span class="sxs-lookup"><span data-stu-id="06892-125">You cannot rename a Category 1 class or attribute.</span></span>

 

 




