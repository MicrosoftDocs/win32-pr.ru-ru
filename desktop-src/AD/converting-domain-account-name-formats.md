---
title: Преобразование форматов имен учетных записей домена
description: Функции Microsoft Win32 для работы с диспетчером управления службами (SCM) на сервере узла используют \ 0034; \\ Формат имени пользователя домена \ 0034; для учетных записей служб.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789606"
---
# <a name="converting-domain-account-name-formats"></a><span data-ttu-id="441fc-103">Преобразование форматов имен учетных записей домена</span><span class="sxs-lookup"><span data-stu-id="441fc-103">Converting Domain Account Name Formats</span></span>

<span data-ttu-id="441fc-104">Функции Microsoft Win32 для работы с диспетчером управления службами (SCM) на сервере узла используют <domain> \\ <username> Формат "" для учетных записей служб.</span><span class="sxs-lookup"><span data-stu-id="441fc-104">The Microsoft Win32 functions for working with the service control manager (SCM) on a host server use the "<domain>\\<username>" format for service accounts.</span></span> <span data-ttu-id="441fc-105">Например, при вызове функции [**куерисервицеконфиг**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) для получения учетной записи пользователя, от имени которой выполняется служба, функция возвращает имя в формате "Fabrikam \\ жеффсмис".</span><span class="sxs-lookup"><span data-stu-id="441fc-105">For example, if you call the [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) function to retrieve the user account under which your service runs, the function returns the name in "Fabrikam\\jeffsmith" format.</span></span> <span data-ttu-id="441fc-106">Для привязки к учетной записи пользователя в каталоге, например для изменения пароля учетной записи, требуется различающееся имя учетной записи, в котором используется формат "CN = Джефф Smith, CN = Users, DC = Fabrikam, DC = COM".</span><span class="sxs-lookup"><span data-stu-id="441fc-106">To bind to the user account in the directory, for example to change the account password, the distinguished name of the account is required, which has the format "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM".</span></span>

<span data-ttu-id="441fc-107">Для преобразования между различными форматами имен используйте функцию [**транслатенаме**](/windows/desktop/api/secext/nf-secext-translatenamea) , которая может преобразовывать имена в другие форматы, например имя участника-пользователя (UPN).</span><span class="sxs-lookup"><span data-stu-id="441fc-107">To convert between the various name formats, use the [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) function, which can convert a name to other formats, such as a user principal name (UPN).</span></span>

 

 