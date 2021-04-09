---
title: Делегирование
description: Делегирование является одной из наиболее важных функций безопасности служб домен Active Directory Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- Делегирование AD
- безопасность AD, делегирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986161"
---
# <a name="delegation"></a><span data-ttu-id="383cd-105">Делегирование</span><span class="sxs-lookup"><span data-stu-id="383cd-105">Delegation</span></span>

<span data-ttu-id="383cd-106">*Делегирование* является одной из наиболее важных функций безопасности служб домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="383cd-106">*Delegation* is one of the most important security features of Active Directory Domain Services.</span></span> <span data-ttu-id="383cd-107">Делегирование позволяет более высокому администратору предоставлять определенные административные права для контейнеров и поддеревьев отдельным пользователям и группам.</span><span class="sxs-lookup"><span data-stu-id="383cd-107">Delegation enables a higher administrative authority to grant specific administrative rights for containers and subtrees to individuals and groups.</span></span> <span data-ttu-id="383cd-108">Администраторы домена, обладающие широкими полномочиями для больших сегментов пользователей, больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="383cd-108">Domain administrators, with broad authority over large segments of users, are no longer required.</span></span>

<span data-ttu-id="383cd-109">ACE может предоставить пользователю или группе определенные административные права для объектов в контейнере.</span><span class="sxs-lookup"><span data-stu-id="383cd-109">An ACE can grant specific administrative rights for the objects in a container to a user or group.</span></span> <span data-ttu-id="383cd-110">Права предоставляются для конкретных операций с конкретными классами объектов с помощью элементов управления доступом в ACL контейнера.</span><span class="sxs-lookup"><span data-stu-id="383cd-110">Rights are granted for specific operations on specific object classes using ACEs in the container's ACL.</span></span> <span data-ttu-id="383cd-111">Например, чтобы позволить пользователю с именем "пользователь 1" быть администратором подразделения "Корпоративное учетное обеспечение", добавьте ACE в список управления доступом на корпоративном учете следующим образом:</span><span class="sxs-lookup"><span data-stu-id="383cd-111">For example, to enable a user named "user 1" to be an administrator of the "Corporate Accounting" organizational unit, add ACEs to the ACL on "Corporate Accounting" as follows:</span></span>

<span data-ttu-id="383cd-112">"" пользователь 1 "; Им Создание, изменение, удаление; пользовательский класс объекта "пользователь 1"; Им Создание, изменение, удаление; Группа классов объектов "пользователь 1"; Им Write; пользователь класса Object; Пароль атрибута "</span><span class="sxs-lookup"><span data-stu-id="383cd-112">""user 1";Grant ;Create, Modify, Delete;Object-Class User"user 1";Grant ;Create, Modify, Delete;Object-Class Group"user 1";Grant ;Write;Object-Class User; Attribute Password"</span></span>

<span data-ttu-id="383cd-113">Теперь пользователь 1 может создавать новых пользователей и группы в корпоративном учетном процессе и устанавливать пароли для существующих пользователей, но пользователь 1 не может создавать другие классы объектов и не может повлиять на работу пользователей в других контейнерах, если, конечно, пользователь 1 не получает доступ к другим контейнерам ACE.</span><span class="sxs-lookup"><span data-stu-id="383cd-113">Now, user 1 can create new users and groups in Corporate Accounting and set the passwords on existing users, but user 1 cannot create any other object classes and cannot affect users in any other containers, unless, of course, user 1 is granted that access by ACEs on the other containers.</span></span>

 

 




