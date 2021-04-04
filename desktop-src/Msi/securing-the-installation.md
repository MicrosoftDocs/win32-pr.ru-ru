---
description: Добавьте все свойства пароля из таблицы Кустомусераккаунтс в свойство Мсихидденпропертиес в таблице свойств.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Защита установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999680"
---
# <a name="securing-the-installation"></a><span data-ttu-id="1d8c0-103">Защита установки</span><span class="sxs-lookup"><span data-stu-id="1d8c0-103">Securing the Installation</span></span>

<span data-ttu-id="1d8c0-104">Добавьте все свойства пароля из таблицы Кустомусераккаунтс в свойство [**мсихидденпропертиес**](msihiddenproperties.md) в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="1d8c0-104">Add all of the Password properties from the CustomUserAccounts table to the [**MsiHiddenProperties**](msihiddenproperties.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="1d8c0-105">Добавьте также имена отложенных настраиваемых действий в свойство **мсихидденпропертиес** .</span><span class="sxs-lookup"><span data-stu-id="1d8c0-105">Add the names of the deferred custom actions to the **MsiHiddenProperties** property as well.</span></span> <span data-ttu-id="1d8c0-106">Это предотвратит запись программой установки конфиденциальных значений свойств (паролей) в журнал и гарантирует, что эти значения не будут регистрироваться, если отложенные настраиваемые действия используют значения в качестве свойства CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="1d8c0-106">This will prevent the installer from writing the sensitive property values (the passwords) into the log and will ensure these values are not logged when the deferred custom actions use the values as the CustomActionData property.</span></span>

<span data-ttu-id="1d8c0-107">Чтобы пароль пользователя был доступен в службе установщик Windows, свойство Password должно быть добавлено в свойство [**секурекустомпропертиес**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="1d8c0-107">For the user's password to be available in the Windows Installer service, the password property must be added to the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

[<span data-ttu-id="1d8c0-108">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="1d8c0-108">Property Table</span></span>](property-table.md)



| <span data-ttu-id="1d8c0-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="1d8c0-109">Property</span></span>                                                 | <span data-ttu-id="1d8c0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1d8c0-110">Value</span></span>                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="1d8c0-111">**мсихидденпропертиес**</span><span class="sxs-lookup"><span data-stu-id="1d8c0-111">**MsiHiddenProperties**</span></span>](msihiddenproperties.md)       | <span data-ttu-id="1d8c0-112">ТЕСТУСЕРПАССВОРД; Креатеаккаунт; RemoveAccount роллбаккаккаунт</span><span class="sxs-lookup"><span data-stu-id="1d8c0-112">TESTUSERPASSWORD;CreateAccount;RemoveAccount;RollbackAccount</span></span> |
| [<span data-ttu-id="1d8c0-113">**секурекустомпропертиес**</span><span class="sxs-lookup"><span data-stu-id="1d8c0-113">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="1d8c0-114">тестусерпассворд</span><span class="sxs-lookup"><span data-stu-id="1d8c0-114">TESTUSERPASSWORD</span></span>                                             |



 

<span data-ttu-id="1d8c0-115">На этом пример завершается.</span><span class="sxs-lookup"><span data-stu-id="1d8c0-115">This concludes the sample.</span></span>

 

 



