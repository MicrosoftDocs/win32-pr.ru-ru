---
title: Схема (AD DS)
description: Active Directory схема реализуется как набор экземпляров класса объекта, хранящихся в каталоге.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory схемы Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2019
ms.locfileid: "103785421"
---
# <a name="schema-ad-ds"></a><span data-ttu-id="77f21-104">Схема (AD DS)</span><span class="sxs-lookup"><span data-stu-id="77f21-104">Schema (AD DS)</span></span>

<span data-ttu-id="77f21-105">Active Directory схема реализуется как набор экземпляров класса объекта, хранящихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="77f21-105">Active Directory schema is implemented as a set of object class instances stored in the directory.</span></span> <span data-ttu-id="77f21-106">Это сильно отличается от многих каталогов, которые имеют схему, но сохраняют ее как текстовый файл, который считывается при запуске.</span><span class="sxs-lookup"><span data-stu-id="77f21-106">This is very different than many directories that have a schema but store it as a text file read at startup.</span></span> <span data-ttu-id="77f21-107">Хранение схемы в каталоге имеет множество преимуществ.</span><span class="sxs-lookup"><span data-stu-id="77f21-107">Storing the schema in the directory has many advantages.</span></span> <span data-ttu-id="77f21-108">Например, пользовательские приложения могут прочитать его, чтобы узнать, какие объекты и свойства доступны.</span><span class="sxs-lookup"><span data-stu-id="77f21-108">For example, user applications can read it to discover what objects and properties are available.</span></span>

<span data-ttu-id="77f21-109">Active Directory схему можно динамически обновлять.</span><span class="sxs-lookup"><span data-stu-id="77f21-109">Active Directory schema can be updated dynamically.</span></span> <span data-ttu-id="77f21-110">Это значит, что приложение может расширить схему новыми атрибутами и классами и использовать расширения немедленно.</span><span class="sxs-lookup"><span data-stu-id="77f21-110">That is, an application can extend the schema with new attributes and classes and use the extensions immediately.</span></span> <span data-ttu-id="77f21-111">Обновление схемы выполняется путем создания или изменения объектов схемы, хранящихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="77f21-111">Schema updates are accomplished by creating or modifying the schema objects stored in the directory.</span></span> <span data-ttu-id="77f21-112">Как и каждый объект в Active Directory, списки управления доступом (ACL) защищают объекты схемы, поэтому полномочные пользователи могут изменять схему только.</span><span class="sxs-lookup"><span data-stu-id="77f21-112">Like every object in Active Directory, access-control lists (ACLs) protect schema objects, so authorized users only may alter the schema.</span></span>

<span data-ttu-id="77f21-113">Дополнительные сведения см. в разделе [схема Active Directory](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="77f21-113">For more information, see [Active Directory Schema](active-directory-schema.md).</span></span>

 

 




