---
title: Защита объектов и атрибутов
description: Список управления доступом (ACL) защищает все объекты в службах домен Active Directory.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Защита объектов и атрибутов
- безопасность AD, защита объектов и атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773130"
---
# <a name="object-and-attribute-protection"></a><span data-ttu-id="28738-105">Защита объектов и атрибутов</span><span class="sxs-lookup"><span data-stu-id="28738-105">Object and Attribute Protection</span></span>

<span data-ttu-id="28738-106">Список управления доступом (ACL) защищает все объекты в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="28738-106">An access-control list (ACL) protects all objects in Active Directory Domain Services.</span></span> <span data-ttu-id="28738-107">Списки управления доступом определяют, кто может просматривать объект, какие атрибуты они могут читать, а также какие действия каждый пользователь может выполнять над объектом.</span><span class="sxs-lookup"><span data-stu-id="28738-107">ACLs determine who can view the object, what attributes they can read, and what actions each user can perform on the object.</span></span> <span data-ttu-id="28738-108">Существование объекта или атрибута никогда не раскрывается неавторизованному пользователю.</span><span class="sxs-lookup"><span data-stu-id="28738-108">The existence of an object or an attribute is never revealed to an unauthorized user.</span></span>

<span data-ttu-id="28738-109">ACL — это список записей управления доступом (ACE), сохраненных вместе с защищаемым объектом.</span><span class="sxs-lookup"><span data-stu-id="28738-109">An ACL is a list of access-control entries (ACEs) stored with the object that it protects.</span></span> <span data-ttu-id="28738-110">В Windows NT и Windows 2000 список ACL хранится в виде двоичного значения, называемого дескриптором безопасности.</span><span class="sxs-lookup"><span data-stu-id="28738-110">In Windows NT and Windows 2000, an ACL is stored as a binary value, called a security descriptor.</span></span> <span data-ttu-id="28738-111">Каждый элемент ACE содержит идентификатор безопасности (SID), который определяет участника (пользователя или группу), к которому применяется ACE, и данные о типе доступа, предоставляемом или запрещающим ACE.</span><span class="sxs-lookup"><span data-stu-id="28738-111">Each ACE contains a security identifier (SID), which identifies the principal (user or group) to whom the ACE applies, and data about what type of access the ACE grants or denies.</span></span>

<span data-ttu-id="28738-112">Списки управления доступом для объектов каталога содержат записи ACE, которые применяются к объекту в целом, и записи ACE, относящиеся к отдельным атрибутам объекта.</span><span class="sxs-lookup"><span data-stu-id="28738-112">ACLs for directory objects contain ACEs that apply to the object as a whole and ACEs that apply to the individual attributes of the object.</span></span> <span data-ttu-id="28738-113">Это позволяет администратору управлять не только тем, какие пользователи могут видеть объект, но и какие свойства эти пользователи могут просматривать.</span><span class="sxs-lookup"><span data-stu-id="28738-113">This allows an administrator to control not only which users can see an object, but also what properties those users can view.</span></span> <span data-ttu-id="28738-114">Например, всем пользователям могут быть предоставлены права на чтение атрибутов электронной почты и номера телефона для всех остальных пользователей, но свойства безопасности пользователей могут быть запрещены для всех, кроме членов особой группы администраторов безопасности.</span><span class="sxs-lookup"><span data-stu-id="28738-114">For example, all users might be granted read access to the email and telephone number attributes for all other users, but security properties of users might be denied to all but members of a special security administrators group.</span></span> <span data-ttu-id="28738-115">Отдельным пользователям может быть предоставлен доступ на запись к личным атрибутам, таким как телефонные и почтовые адреса для собственных объектов пользователя.</span><span class="sxs-lookup"><span data-stu-id="28738-115">Individual users might be granted write access to personal attributes such as the telephone and mailing addresses on their own user objects.</span></span>

 

 




