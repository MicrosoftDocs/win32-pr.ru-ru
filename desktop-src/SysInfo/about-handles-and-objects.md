---
description: Система использует объекты и дескрипторы для регулирования доступа к системным ресурсам по двум основным причинам.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Об дескрипторах и объектах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998613"
---
# <a name="about-handles-and-objects"></a><span data-ttu-id="f31fb-103">Об дескрипторах и объектах</span><span class="sxs-lookup"><span data-stu-id="f31fb-103">About Handles and Objects</span></span>

<span data-ttu-id="f31fb-104">Система использует объекты и дескрипторы для регулирования доступа к системным ресурсам по двум основным причинам.</span><span class="sxs-lookup"><span data-stu-id="f31fb-104">The system uses objects and handles to regulate access to system resources for two main reasons.</span></span> <span data-ttu-id="f31fb-105">Во-первых, использование объектов гарантирует, что корпорация Майкрософт сможет обновить функциональность системы, пока не будет сохранен исходный интерфейс объекта.</span><span class="sxs-lookup"><span data-stu-id="f31fb-105">First, the use of objects ensures that Microsoft can update system functionality, as long as the original object interface is maintained.</span></span> <span data-ttu-id="f31fb-106">При выпуске последующих версий системы можно использовать обновленный объект без дополнительной работы.</span><span class="sxs-lookup"><span data-stu-id="f31fb-106">When subsequent versions of the system are released, you can use the updated object with little or no additional work.</span></span>

<span data-ttu-id="f31fb-107">Во вторых, использование объектов позволяет использовать преимущества системы безопасности Windows.</span><span class="sxs-lookup"><span data-stu-id="f31fb-107">Secondly, the use of objects enables you to take advantage of Windows security.</span></span> <span data-ttu-id="f31fb-108">Каждый объект имеет собственный список управления доступом (ACL), указывающий действия, которые процесс может выполнять над объектом.</span><span class="sxs-lookup"><span data-stu-id="f31fb-108">Each object has its own access-control list (ACL) that specifies the actions a process can perform on the object.</span></span> <span data-ttu-id="f31fb-109">Система проверяет список ACL объекта каждый раз, когда приложение создает маркер для объекта.</span><span class="sxs-lookup"><span data-stu-id="f31fb-109">The system examines an object's ACL each time an application creates a handle to the object.</span></span> <span data-ttu-id="f31fb-110">Дополнительные сведения см. в статье [Управление доступом](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="f31fb-110">For more information, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

-   [<span data-ttu-id="f31fb-111">Диспетчер объектов</span><span class="sxs-lookup"><span data-stu-id="f31fb-111">Object Manager</span></span>](object-manager.md)
-   [<span data-ttu-id="f31fb-112">Объектный интерфейс</span><span class="sxs-lookup"><span data-stu-id="f31fb-112">Object Interface</span></span>](object-interface.md)
-   [<span data-ttu-id="f31fb-113">Пространства имен объектов</span><span class="sxs-lookup"><span data-stu-id="f31fb-113">Object Namespaces</span></span>](/windows/desktop/Sync/object-namespaces)
-   [<span data-ttu-id="f31fb-114">Ограничения по обработке</span><span class="sxs-lookup"><span data-stu-id="f31fb-114">Handle Limitations</span></span>](handle-limitations.md)
-   [<span data-ttu-id="f31fb-115">Наследование в обработке</span><span class="sxs-lookup"><span data-stu-id="f31fb-115">Handle Inheritance</span></span>](handle-inheritance.md)

 

 
