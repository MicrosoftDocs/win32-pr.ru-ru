---
title: Динамически связываемые вспомогательные классы
description: Динамически связываемый вспомогательный класс — это класс, присоединенный к отдельному объекту, а не к классу объекта.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Динамически связываемые вспомогательные классы Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252789"
---
# <a name="dynamically-linked-auxiliary-classes"></a><span data-ttu-id="f5dff-104">Динамически связываемые вспомогательные классы</span><span class="sxs-lookup"><span data-stu-id="f5dff-104">Dynamically Linked Auxiliary Classes</span></span>

<span data-ttu-id="f5dff-105">Динамически связываемый вспомогательный класс — это класс, присоединенный к отдельному объекту, а не к классу объекта.</span><span class="sxs-lookup"><span data-stu-id="f5dff-105">A dynamically linked auxiliary class is a class that is attached to an individual object, rather than to an object class.</span></span> <span data-ttu-id="f5dff-106">Динамическая компоновка позволяет хранить дополнительные атрибуты в отдельном объекте без влияния на весь лес расширения определения схемы для всего класса.</span><span class="sxs-lookup"><span data-stu-id="f5dff-106">Dynamic linking enables you to store additional attributes with an individual object without the forest-wide impact of extending the schema definition for an entire class.</span></span> <span data-ttu-id="f5dff-107">Например, предприятие может использовать динамическую компоновку, чтобы присоединить вспомогательный класс, относящийся к продажам, к объектам-пользователям своих сотрудников по продажам и другим вспомогательным классам отдела для пользовательских объектов сотрудников в других подразделениях.</span><span class="sxs-lookup"><span data-stu-id="f5dff-107">For example, an enterprise could use dynamic linking to attach a sales-specific auxiliary class to the user objects of its sales people, and other department-specific auxiliary classes to the user objects of employees in other departments.</span></span>

<span data-ttu-id="f5dff-108">Динамическая компоновка не сложна: добавьте имя вспомогательного класса к значениям атрибута **objectClass** объекта.</span><span class="sxs-lookup"><span data-stu-id="f5dff-108">Dynamic linking is not complex: add the name of the auxiliary class to the values of an object's **objectClass** attribute.</span></span> <span data-ttu-id="f5dff-109">Если вспомогательный класс имеет обязательные атрибуты (**муссаве** или **системмуссаве**), их необходимо задать одновременно.</span><span class="sxs-lookup"><span data-stu-id="f5dff-109">If the auxiliary class has any mandatory attributes (**mustHave** or **systemMustHave**), you must set them at the same time.</span></span> <span data-ttu-id="f5dff-110">Дополнительные сведения и пример кода см. в разделе [Добавление вспомогательного класса к экземпляру объекта](adding-an-auxiliary-class-to-an-object-instance.md).</span><span class="sxs-lookup"><span data-stu-id="f5dff-110">For more information and a code example, see [Adding an Auxiliary Class to an Object Instance](adding-an-auxiliary-class-to-an-object-instance.md).</span></span>

<span data-ttu-id="f5dff-111">Чтобы удалить динамически связываемый вспомогательный класс, очистите значения всех атрибутов вспомогательного класса, а затем удалите имя вспомогательного класса из атрибута **objectClass** объекта.</span><span class="sxs-lookup"><span data-stu-id="f5dff-111">To remove a dynamically linked auxiliary class, clear the values of all attributes from the auxiliary class, and then remove the name of the auxiliary class from the **objectClass** attribute of the object.</span></span>

<span data-ttu-id="f5dff-112">При динамическом добавлении вспомогательного класса, который является подклассом другого вспомогательного класса, в целевой объект добавляются оба вспомогательных класса.</span><span class="sxs-lookup"><span data-stu-id="f5dff-112">If you dynamically add an auxiliary class that is a subclass of another auxiliary class, both auxiliary classes are added to the target object.</span></span> <span data-ttu-id="f5dff-113">Однако при удалении дочернего вспомогательного класса его родительский класс не удаляется. Каждый класс должен быть явно удален.</span><span class="sxs-lookup"><span data-stu-id="f5dff-113">However, removing the child auxiliary class does not remove its parent; each class must be explicitly removed.</span></span>

 

 




