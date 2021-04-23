---
title: Сведения о схеме Active Directory
description: Каждый объект в домен Active Directory Services является экземпляром класса объекта, определенного в схеме Active Directory.
ms.assetid: 8fc9cd2d-8fed-4fda-918c-79b01f9a19bb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f55513b359a7ef293b005d93a20ac43f470d515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887443"
---
# <a name="about-the-active-directory-schema"></a><span data-ttu-id="a83ea-103">Сведения о схеме Active Directory</span><span class="sxs-lookup"><span data-stu-id="a83ea-103">About the Active Directory Schema</span></span>

<span data-ttu-id="a83ea-104">Каждый объект в домен Active Directory Services является экземпляром класса объекта, определенного в схеме Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a83ea-104">Every object in Active Directory Domain Services is an instance of an object class defined in the Active Directory schema.</span></span> <span data-ttu-id="a83ea-105">Класс объектов представляет категорию объектов (таких как пользователи, принтеры или приложения) с общим набором характеристик.</span><span class="sxs-lookup"><span data-stu-id="a83ea-105">An object class represents a category of objects, such as users, printers, or application programs, that share a set of common characteristics.</span></span> <span data-ttu-id="a83ea-106">Определение каждого класса объектов содержит список атрибутов, которые можно использовать для описания экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="a83ea-106">The definition for each object class contains a list of the attributes that can be used to describe instances of the class.</span></span> <span data-ttu-id="a83ea-107">Например, класс User имеет такие атрибуты, как **givenName**, **Фамилия** и **streetAddress**.</span><span class="sxs-lookup"><span data-stu-id="a83ea-107">For example, the User class has attributes such as **givenName**, **surname**, and **streetAddress**.</span></span> <span data-ttu-id="a83ea-108">Список атрибутов класса делится на объекты, которые должен содержать объект этого класса, и дополнительные атрибуты, которые может содержать объект.</span><span class="sxs-lookup"><span data-stu-id="a83ea-108">The list of attributes for a class is divided into those that an object of that class must contain, and additional attributes that an object may contain.</span></span> <span data-ttu-id="a83ea-109">Каталог упорядочивается в иерархии. в определении каждого класса также перечислены классы, объекты которых могут быть родителями объектов данного класса — это управляет формой иерархии каталогов.</span><span class="sxs-lookup"><span data-stu-id="a83ea-109">The directory is arranged in a hierarchy; the definition of each class also lists the classes whose objects can be parents of objects of a given class—this controls the shape of the directory hierarchy.</span></span>

<span data-ttu-id="a83ea-110">Схема также формально определяет каждый атрибут.</span><span class="sxs-lookup"><span data-stu-id="a83ea-110">The schema also formally defines each attribute.</span></span> <span data-ttu-id="a83ea-111">Определение для каждого атрибута включает уникальные идентификаторы для атрибута, синтаксис атрибута (т. е. тип данных для значений атрибута), необязательные ограничения диапазона для значений атрибутов, может ли атрибут иметь только одно значение или несколько значений и является ли атрибут индексированным.</span><span class="sxs-lookup"><span data-stu-id="a83ea-111">The definition for each attribute includes unique identifiers for the attribute, the syntax for the attribute (that is, the data type for the attribute's values), optional range limits for the attribute values, whether the attribute can have only one value or multiple values, and whether the attribute is indexed.</span></span> <span data-ttu-id="a83ea-112">Схема каталога определяет каждый атрибут ровно один раз — определения классов объектов содержат ссылки на атрибуты, определенные в схеме.</span><span class="sxs-lookup"><span data-stu-id="a83ea-112">The directory schema defines each attribute exactly once—object class definitions contain references to the attributes defined in the schema.</span></span> <span data-ttu-id="a83ea-113">Например, атрибут "Description" определен только один раз и на него ссылаются многие классы объектов.</span><span class="sxs-lookup"><span data-stu-id="a83ea-113">For example, the "description" attribute is defined only once and is referenced by many object classes.</span></span> <span data-ttu-id="a83ea-114">Это отличается от схемы реляционной базы данных, в которой атрибуты (столбцы) задаются отдельно для каждой таблицы.</span><span class="sxs-lookup"><span data-stu-id="a83ea-114">This is different than a relational database schema, where the "attributes" (columns) are separately defined for each table.</span></span>

 

 




