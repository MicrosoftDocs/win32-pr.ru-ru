---
description: Библиотека DLL фильтрации паролей Windows, Passfilt.dll, выполняется в контексте безопасности локальной системной учетной записи и помогает фильтровать пароли домена или локальной учетной записи.
ms.assetid: 12a6fe6d-5b37-4fcf-bd04-0a22d84ba323
title: Установка и регистрация библиотеки DLL фильтрации паролей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb2e9f93630dc6bdaa5dbcc7e665a6b1cebff0e
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327169"
---
# <a name="installing-and-registering-a-password-filter-dll"></a><span data-ttu-id="de5b6-103">Установка и регистрация библиотеки DLL фильтрации паролей</span><span class="sxs-lookup"><span data-stu-id="de5b6-103">Installing and Registering a Password Filter DLL</span></span>

<span data-ttu-id="de5b6-104">Для фильтрации паролей домена или локальной учетной записи можно использовать фильтр паролей Windows.</span><span class="sxs-lookup"><span data-stu-id="de5b6-104">You can use the Windows password filter to filter domain or local account passwords.</span></span> <span data-ttu-id="de5b6-105">Чтобы использовать фильтр паролей для учетных записей домена, установите и зарегистрируйте библиотеку DLL на каждом контроллере домена в домене.</span><span class="sxs-lookup"><span data-stu-id="de5b6-105">To use the password filter for domain accounts, install and register the DLL on each domain controller in the domain.</span></span>

<span data-ttu-id="de5b6-106">Чтобы установить фильтр паролей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="de5b6-106">Perform the following steps to install your password filter.</span></span> <span data-ttu-id="de5b6-107">Эти действия можно выполнить вручную, или можно написать установщик для выполнения этих действий.</span><span class="sxs-lookup"><span data-stu-id="de5b6-107">You can perform these steps manually, or you can write an installer to perform these steps.</span></span> <span data-ttu-id="de5b6-108">Чтобы выполнить эти действия, необходимо быть администратором или принадлежать к группе администраторов.</span><span class="sxs-lookup"><span data-stu-id="de5b6-108">You need to be an Administrator or belong to the Administrator Group to perform these steps.</span></span>

<span data-ttu-id="de5b6-109">**Установка и регистрация библиотеки DLL фильтрации паролей Windows**</span><span class="sxs-lookup"><span data-stu-id="de5b6-109">**To install and register a Windows password filter DLL**</span></span>

1.  <span data-ttu-id="de5b6-110">Скопируйте библиотеку DLL в каталог установки Windows на контроллере домена или на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="de5b6-110">Copy the DLL to the Windows installation directory on the domain controller or local computer.</span></span> <span data-ttu-id="de5b6-111">При стандартной установке папка по умолчанию — \\ Windows \\ System32.</span><span class="sxs-lookup"><span data-stu-id="de5b6-111">On standard installations, the default folder is \\Windows\\System32.</span></span> <span data-ttu-id="de5b6-112">Убедитесь, что вы создали 32-разрядную библиотеку DLL фильтрации паролей для 32-разрядных компьютеров и 64-разрядную библиотеку DLL фильтрации паролей для 64-разрядных компьютеров, а затем скопируйте их в соответствующее расположение.</span><span class="sxs-lookup"><span data-stu-id="de5b6-112">Make sure that you create a 32-bit password filter DLL for 32-bit computers and a 64-bit password filter DLL for 64-bit computers, and then copy them to the appropriate location.</span></span>
2.  <span data-ttu-id="de5b6-113">Чтобы зарегистрировать фильтр паролей, обновите следующий раздел системного реестра:</span><span class="sxs-lookup"><span data-stu-id="de5b6-113">To register the password filter, update the following system registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Control
                Lsa
    ```

    <span data-ttu-id="de5b6-114">Если значение **пакетов уведомлений** типа *REG_MULTI_SZ* существует, добавьте имя библиотеки DLL в существующие данные значения.</span><span class="sxs-lookup"><span data-stu-id="de5b6-114">If the **Notification Packages** value of type *REG_MULTI_SZ* exists, add the name of your DLL to the existing value data.</span></span> <span data-ttu-id="de5b6-115">Не перезаписывайте существующие значения и не включайте расширение DLL.</span><span class="sxs-lookup"><span data-stu-id="de5b6-115">Do not overwrite the existing values, and do not include the .dll extension.</span></span>

    <span data-ttu-id="de5b6-116">Если значение **пакетов уведомлений** не существует, создайте его, присвойте ему тип *REG_MULTI_SZ* , а затем укажите имя библиотеки DLL для данных значения.</span><span class="sxs-lookup"><span data-stu-id="de5b6-116">If the **Notification Packages** value does not exist, create it, give it the *REG_MULTI_SZ* type and then specify the name of the DLL for the value data.</span></span> <span data-ttu-id="de5b6-117">Не включайте расширение DLL.</span><span class="sxs-lookup"><span data-stu-id="de5b6-117">Do not include the .dll extension.</span></span>

    <span data-ttu-id="de5b6-118">Значение **пакетов уведомлений** может добавлять несколько пакетов.</span><span class="sxs-lookup"><span data-stu-id="de5b6-118">The **Notification Packages** value can add multiple packages.</span></span>

3.  <span data-ttu-id="de5b6-119">Найдите параметр сложность пароля.</span><span class="sxs-lookup"><span data-stu-id="de5b6-119">Find the password complexity setting.</span></span>

    <span data-ttu-id="de5b6-120">На панели управления щелкните **производительность и обслуживание**, щелкните **Администрирование**, дважды щелкните **Локальная политика безопасности**, дважды щелкните политики **учетных записей**, а затем дважды щелкните **Политика паролей**.</span><span class="sxs-lookup"><span data-stu-id="de5b6-120">In Control Panel, click **Performance and Maintenance**, click **Administrative Tools**, double-click **Local Security Policy**, double-click **Account Policies**, and then double-click **Password Policy**.</span></span>

4.  <span data-ttu-id="de5b6-121">Чтобы применить фильтр паролей Windows по умолчанию и настраиваемый фильтр паролей, убедитесь, что включен параметр политики **пароли должны соответствовать требованиям сложности** .</span><span class="sxs-lookup"><span data-stu-id="de5b6-121">To enforce both the default Windows password filter and the custom password filter, ensure that the **Passwords must meet complexity requirements** policy setting is enabled.</span></span> <span data-ttu-id="de5b6-122">В противном случае отключите параметр политики **пароли должны соответствовать требованиям сложности** .</span><span class="sxs-lookup"><span data-stu-id="de5b6-122">Otherwise, disable the **Passwords must meet complexity requirements** policy setting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de5b6-123">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="de5b6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de5b6-124">Рекомендации по программированию фильтрации паролей</span><span class="sxs-lookup"><span data-stu-id="de5b6-124">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="de5b6-125">Принудительное применение надежных паролей и Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="de5b6-125">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)
</dt> <dt>

[<span data-ttu-id="de5b6-126">Функции фильтрации паролей</span><span class="sxs-lookup"><span data-stu-id="de5b6-126">Password Filter Functions</span></span>](management-functions.md)
</dt> </dl>

 

 



