---
description: Описание защиты объектов учетной записи.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Защита объектов учетных записей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f495a3dc943ef73eef5074e0edc73247ceb02d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663923"
---
# <a name="account-object-protection"></a><span data-ttu-id="b6484-103">Защита объектов учетных записей</span><span class="sxs-lookup"><span data-stu-id="b6484-103">Account Object Protection</span></span>

<span data-ttu-id="b6484-104">Объекты [**учетной записи**](account-object.md) защищаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b6484-104">[**Account**](account-object.md) objects are protected in the following fashion:</span></span>

-   <span data-ttu-id="b6484-105">В **мире** группы есть универсальное \_ выполнение.</span><span class="sxs-lookup"><span data-stu-id="b6484-105">The group **WORLD** has GENERIC\_EXECUTE.</span></span>
-   <span data-ttu-id="b6484-106">У **локального \_ администратора** группы есть доступ для удаления, общего \_ чтения, универсальной \_ записи, общего \_ выполнения и записи \_ списка DACL.</span><span class="sxs-lookup"><span data-stu-id="b6484-106">The group **LOCAL\_ADMIN** has DELETE, GENERIC\_READ, GENERIC\_WRITE, GENERIC\_EXECUTE, and WRITE\_DACL access.</span></span>
-   <span data-ttu-id="b6484-107">Группа **"локальный \_ Администратор"** назначается как владелец и основная группа объектов учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b6484-107">The group **LOCAL\_ADMIN** is assigned as owner and primary group of Account objects.</span></span>

 

 



