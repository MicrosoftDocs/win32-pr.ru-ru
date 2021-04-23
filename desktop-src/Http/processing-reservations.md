---
title: Обработка резервирований
description: Резервирование для частей пространства имен URL-адресов осуществляется системным администратором и размещается в хранилище постоянного резервирования.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104414081"
---
# <a name="processing-reservations"></a><span data-ttu-id="7f4f8-103">Обработка резервирований</span><span class="sxs-lookup"><span data-stu-id="7f4f8-103">Processing Reservations</span></span>

<span data-ttu-id="7f4f8-104">Резервирование для частей пространства имен URL-адресов осуществляется системным администратором и размещается в хранилище постоянного резервирования.</span><span class="sxs-lookup"><span data-stu-id="7f4f8-104">Reservations for portions of the URL namespace are made by the system administrator and placed in the persistent reservation store.</span></span> <span data-ttu-id="7f4f8-105">Корневой каталог пространства имен URL-адресов для HTTP принадлежит системному администратору.</span><span class="sxs-lookup"><span data-stu-id="7f4f8-105">The root of the URL namespace for HTTP is owned by the system administrator.</span></span> <span data-ttu-id="7f4f8-106">Для всех значений узлов и портов в корне пространства имен **relativeUri** всегда предполагается наличие следующих двух резервирований.</span><span class="sxs-lookup"><span data-stu-id="7f4f8-106">For all host and port values, the following two reservations are always assumed at the root of the **relativeUri** namespace.</span></span>



| <span data-ttu-id="7f4f8-107">Пространство имен зарезервировано</span><span class="sxs-lookup"><span data-stu-id="7f4f8-107">Namespace reserved</span></span>                 | <span data-ttu-id="7f4f8-108">Зарезервировано для</span><span class="sxs-lookup"><span data-stu-id="7f4f8-108">Reserved for</span></span>              |
|------------------------------------|---------------------------|
| <span data-ttu-id="7f4f8-109"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="7f4f8-109">https://<host>:<port>/</span></span>  | <span data-ttu-id="7f4f8-110">Администратор LocalSystem</span><span class="sxs-lookup"><span data-stu-id="7f4f8-110">LocalSystem Administrator</span></span> |
| <span data-ttu-id="7f4f8-111"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="7f4f8-111">https://<host>:<port>/</span></span> | <span data-ttu-id="7f4f8-112">Администратор LocalSystem</span><span class="sxs-lookup"><span data-stu-id="7f4f8-112">LocalSystem Administrator</span></span> |



 

<span data-ttu-id="7f4f8-113">Эти неявные резервирования не могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="7f4f8-113">These implicit reservations cannot be removed.</span></span> <span data-ttu-id="7f4f8-114">Однако явное резервирование root можно делегировать другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="7f4f8-114">However, it is possible to delegate explicit root reservations to other users.</span></span> <span data-ttu-id="7f4f8-115">При резервировании, как показано ниже, будут созданы такие делегирования:</span><span class="sxs-lookup"><span data-stu-id="7f4f8-115">Reservations such as the following would create such delegations:</span></span>



| <span data-ttu-id="7f4f8-116">Пространство имен зарезервировано</span><span class="sxs-lookup"><span data-stu-id="7f4f8-116">Namespace reserved</span></span>        | <span data-ttu-id="7f4f8-117">Зарезервировано для</span><span class="sxs-lookup"><span data-stu-id="7f4f8-117">Reserved for</span></span> |
|---------------------------|--------------|
| `https://+:80/`           | <span data-ttu-id="7f4f8-118">Пользователь a, UserC</span><span class="sxs-lookup"><span data-stu-id="7f4f8-118">UserA, UserC</span></span> |
| `https://adatum.com:443/` | <span data-ttu-id="7f4f8-119">Пользователя b</span><span class="sxs-lookup"><span data-stu-id="7f4f8-119">UserB</span></span>        |



 

<span data-ttu-id="7f4f8-120">Если эти делегированные резервирования удаляются системным администратором, владение пространством имен возвращается к неявному резервированию для соответствующих значений узла и порта.</span><span class="sxs-lookup"><span data-stu-id="7f4f8-120">If these delegated reservations are removed by the system administrator, ownership of the namespace reverts to the implicit reservation for the corresponding host and port values.</span></span>

 

 




