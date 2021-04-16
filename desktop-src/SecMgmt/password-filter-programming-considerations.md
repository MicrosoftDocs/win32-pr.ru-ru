---
description: Содержит сведения о реализации функций экспорта фильтрации паролей.
ms.assetid: ec7c1e7e-844a-43d4-b756-02bc1062d7b8
title: Рекомендации по программированию фильтрации паролей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad13a52f66c29142248ca07179d8692887b1acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662305"
---
# <a name="password-filter-programming-considerations"></a><span data-ttu-id="b6534-103">Рекомендации по программированию фильтрации паролей</span><span class="sxs-lookup"><span data-stu-id="b6534-103">Password Filter Programming Considerations</span></span>

<span data-ttu-id="b6534-104">При реализации функций экспорта [*фильтра паролей*](/windows/desktop/SecGloss/p-gly) учитывайте следующие соображения.</span><span class="sxs-lookup"><span data-stu-id="b6534-104">When implementing [*password filter*](/windows/desktop/SecGloss/p-gly) export functions, keep the following considerations in mind:</span></span>

-   <span data-ttu-id="b6534-105">При работе с паролями в [*виде открытого текста*](/windows/desktop/SecGloss/p-gly) следует соблюдать осторожность.</span><span class="sxs-lookup"><span data-stu-id="b6534-105">Take great care when working with [*plaintext*](/windows/desktop/SecGloss/p-gly) passwords.</span></span> <span data-ttu-id="b6534-106">Отправка безтекстовых паролей по сетям может привести к нарушению безопасности.</span><span class="sxs-lookup"><span data-stu-id="b6534-106">Sending plaintext passwords over networks could compromise security.</span></span> <span data-ttu-id="b6534-107">Сетевые «средства прослушивания» позволяют легко отслеживать трафик паролей в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="b6534-107">Network "sniffers" can easily watch for plaintext password traffic.</span></span>
-   <span data-ttu-id="b6534-108">Удалите всю память, используемую для хранения паролей, вызвав функцию [**секурезеромемори**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) перед освобождением памяти.</span><span class="sxs-lookup"><span data-stu-id="b6534-108">Erase all memory used to store passwords by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function before freeing memory.</span></span>
-   <span data-ttu-id="b6534-109">Все буферы, передаваемые в уведомления паролей и подпрограммы фильтров, должны рассматриваться как доступные только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b6534-109">All buffers passed into password notification and filter routines should be treated as read-only.</span></span> <span data-ttu-id="b6534-110">Запись данных в эти буферы может привести к нестабильной работе.</span><span class="sxs-lookup"><span data-stu-id="b6534-110">Writing data to these buffers may cause unstable behavior.</span></span>
-   <span data-ttu-id="b6534-111">Все уведомления паролей и подпрограммы фильтрации должны быть потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="b6534-111">All password notification and filter routines should be thread-safe.</span></span> <span data-ttu-id="b6534-112">Используйте критические разделы или другие методы синхронного программирования для защиты данных, если это уместно.</span><span class="sxs-lookup"><span data-stu-id="b6534-112">Use critical sections or other synchronous programming techniques to protect data where appropriate.</span></span>
-   <span data-ttu-id="b6534-113">Уведомление и фильтрация паролей выполняются только на компьютере, где размещена учетная запись.</span><span class="sxs-lookup"><span data-stu-id="b6534-113">Password notification and filtering take place only on the computer that houses the account.</span></span>
-   <span data-ttu-id="b6534-114">Все контроллеры домена доступны для записи, поэтому пакеты фильтров паролей должны присутствовать на всех контроллерах домена.</span><span class="sxs-lookup"><span data-stu-id="b6534-114">All domain controllers are writeable, therefore password filter packages must be present on all domain controllers.</span></span>

    <span data-ttu-id="b6534-115">**Домены Windows NT 4,0:** Уведомления об учетных записях домена выполняются только на основном контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="b6534-115">**Windows NT 4.0 domains:** Notification on domain accounts takes place only on the primary domain controller.</span></span> <span data-ttu-id="b6534-116">Помимо основного контроллера домена, пакеты фильтрации паролей должны быть установлены на всех резервных контроллерах домена, чтобы разрешить продолжение уведомлений в случае изменения роли сервера.</span><span class="sxs-lookup"><span data-stu-id="b6534-116">In addition to the primary domain controller, the password filter packages should be installed on all backup domain controllers to allow notifications to continue in the event of server role changes.</span></span>

-   <span data-ttu-id="b6534-117">Все библиотеки DLL фильтра паролей выполняются в [*контексте безопасности*](/windows/desktop/SecGloss/s-gly) локальной системной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b6534-117">All password filter DLLs run in the [*security context*](/windows/desktop/SecGloss/s-gly) of the local system account.</span></span>



| <span data-ttu-id="b6534-118">Сведения о</span><span class="sxs-lookup"><span data-stu-id="b6534-118">For information about</span></span>                                                                                                                     | <span data-ttu-id="b6534-119">См.</span><span class="sxs-lookup"><span data-stu-id="b6534-119">See</span></span>                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6534-120">Как установить и зарегистрировать собственную библиотеку DLL для [*фильтрации паролей*](/windows/desktop/SecGloss/p-gly) .</span><span class="sxs-lookup"><span data-stu-id="b6534-120">How to install and register your own [*password filter*](/windows/desktop/SecGloss/p-gly) DLL.</span></span> | [<span data-ttu-id="b6534-121">Установка и регистрация библиотеки DLL фильтрации паролей</span><span class="sxs-lookup"><span data-stu-id="b6534-121">Installing and Registering a Password Filter DLL</span></span>](installing-and-registering-a-password-filter-dll.md) |
| <span data-ttu-id="b6534-122">Библиотека DLL фильтра паролей, предоставляемая корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="b6534-122">The password filter DLL provided by Microsoft.</span></span>                                                                                            | [<span data-ttu-id="b6534-123">Принудительное применение надежных паролей и Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="b6534-123">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)         |
| <span data-ttu-id="b6534-124">Экспорт функций, реализованных с помощью библиотеки DLL фильтрации паролей.</span><span class="sxs-lookup"><span data-stu-id="b6534-124">Export functions implemented by a password filter DLL.</span></span>                                                                                    | [<span data-ttu-id="b6534-125">Функции фильтрации паролей</span><span class="sxs-lookup"><span data-stu-id="b6534-125">Password Filter Functions</span></span>](management-functions.md)                          |



 

 

 
