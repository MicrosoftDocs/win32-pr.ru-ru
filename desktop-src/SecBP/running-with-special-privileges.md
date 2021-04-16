---
description: Для правильной работы некоторых функций требуются специальные права.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Запуск с особыми привилегиями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664479"
---
# <a name="running-with-special-privileges"></a><span data-ttu-id="a793a-103">Запуск с особыми привилегиями</span><span class="sxs-lookup"><span data-stu-id="a793a-103">Running with Special Privileges</span></span>

<span data-ttu-id="a793a-104">Для правильной работы некоторых функций требуются специальные [права](/windows/desktop/SecAuthZ/privileges) .</span><span class="sxs-lookup"><span data-stu-id="a793a-104">Some functions require special [privileges](/windows/desktop/SecAuthZ/privileges) to run correctly.</span></span> <span data-ttu-id="a793a-105">В некоторых случаях эта функция может выполняться только определенными пользователями или членами определенных групп.</span><span class="sxs-lookup"><span data-stu-id="a793a-105">In some cases, the function can only be run by certain users or by members of certain groups.</span></span> <span data-ttu-id="a793a-106">Наиболее распространенным требованием является то, что пользователь является локальным администратором.</span><span class="sxs-lookup"><span data-stu-id="a793a-106">The most common requirement is that the user be a local administrator.</span></span> <span data-ttu-id="a793a-107">Для других функций требуется, чтобы учетная запись пользователя включала определенные привилегии.</span><span class="sxs-lookup"><span data-stu-id="a793a-107">Other functions require the user's account to have specific privileges enabled.</span></span>

<span data-ttu-id="a793a-108">Чтобы снизить вероятность того, что несанкционированный код сможет получить контроль, система должна работать с минимальными необходимыми привилегиями.</span><span class="sxs-lookup"><span data-stu-id="a793a-108">To reduce the possibility of unauthorized code being able to get control, the system should run with the least privilege necessary.</span></span> <span data-ttu-id="a793a-109">Приложения, которым требуется вызывать функции, требующие специальных привилегий, могут оставить систему уязвимой для атак хакеров.</span><span class="sxs-lookup"><span data-stu-id="a793a-109">Applications that need to call functions that require special privileges can leave the system open to attack by hackers.</span></span> <span data-ttu-id="a793a-110">Такие приложения должны работать в течение короткого периода времени и сообщать пользователю о вовлеченных в него последствиях безопасности.</span><span class="sxs-lookup"><span data-stu-id="a793a-110">Such applications should be designed to run for short periods of time and should inform the user of the security implications involved.</span></span>

<span data-ttu-id="a793a-111">Сведения о запуске от имени разных пользователей и о том, как включить привилегии в приложении, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="a793a-111">For information about how to run as different users and how to enable privileges in your application, see the following topics:</span></span><dl>

[<span data-ttu-id="a793a-112">Запуск с правами администратора</span><span class="sxs-lookup"><span data-stu-id="a793a-112">Running with Administrator Privileges</span></span>](running-with-administrator-privileges.md)  
[<span data-ttu-id="a793a-113">Запрос учетных данных для пользователя</span><span class="sxs-lookup"><span data-stu-id="a793a-113">Asking the User for Credentials</span></span>](asking-the-user-for-credentials.md)  
[<span data-ttu-id="a793a-114">Изменение привилегий в токене</span><span class="sxs-lookup"><span data-stu-id="a793a-114">Changing Privileges in a Token</span></span>](changing-privileges-in-a-token.md)  
[<span data-ttu-id="a793a-115">Назначение привилегий учетной записи</span><span class="sxs-lookup"><span data-stu-id="a793a-115">Assigning Privileges to an Account</span></span>](assigning-privileges-to-an-account.md)  
</dl>

 

 
