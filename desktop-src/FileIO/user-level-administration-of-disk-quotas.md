---
description: Как получить больше свободного места на диске после превышения квоты.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Администрирование дисковых квот на уровне пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664272"
---
# <a name="user-level-administration-of-disk-quotas"></a><span data-ttu-id="39c36-103">Администрирование дисковых квот на уровне пользователя</span><span class="sxs-lookup"><span data-stu-id="39c36-103">User-level Administration of Disk Quotas</span></span>

<span data-ttu-id="39c36-104">Квоты диска прозрачны для пользователя.</span><span class="sxs-lookup"><span data-stu-id="39c36-104">Disk quotas are transparent to the user.</span></span> <span data-ttu-id="39c36-105">Когда пользователь запрашивает объем свободного места на диске, система сообщает только о доступной квоте, доступной пользователю.</span><span class="sxs-lookup"><span data-stu-id="39c36-105">When a user asks how much space is free on a disk, the system reports only the available quota allowance the user has available.</span></span> <span data-ttu-id="39c36-106">Если пользователь превышает эту квоту, система возвращает сообщение **об ошибке \_ \_ переполнения диска** , точно так же, как было бы означать, что диск заполнен.</span><span class="sxs-lookup"><span data-stu-id="39c36-106">If the user exceeds this allowance, the system returns the **ERROR\_DISK\_FULL** error, just as it would to indicate that the disk was full.</span></span>

<span data-ttu-id="39c36-107">Чтобы получить больше свободного места на диске после превышения квоты, пользователь должен выполнить одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="39c36-107">To obtain more free disk space after exceeding the quota allowance, the user must do one of the following:</span></span>

-   <span data-ttu-id="39c36-108">Удалите некоторые файлы.</span><span class="sxs-lookup"><span data-stu-id="39c36-108">Delete some files.</span></span>
-   <span data-ttu-id="39c36-109">Попросите другого пользователя запросить владение некоторыми файлами.</span><span class="sxs-lookup"><span data-stu-id="39c36-109">Have another user claim ownership of some files.</span></span>
-   <span data-ttu-id="39c36-110">Повысьте квоту у администратора.</span><span class="sxs-lookup"><span data-stu-id="39c36-110">Have the administrator increase the quota allowance.</span></span>

<span data-ttu-id="39c36-111">Программы, которым требуется получить фактический объем свободного места на диске, могут вызвать функцию [**жетдискфриспацеекс**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) и взглянуть на параметр *тоталнумбероффрибитес* .</span><span class="sxs-lookup"><span data-stu-id="39c36-111">Programs that need to retrieve the actual amount of free disk space can call the [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) function and look at the *TotalNumberOfFreeBytes* parameter.</span></span>

 

 



