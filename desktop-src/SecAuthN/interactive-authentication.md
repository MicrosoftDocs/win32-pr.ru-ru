---
description: Проверка подлинности является интерактивной, когда пользователю предлагается ввести сведения для входа в систему. Локальный центр безопасности (LSA) выполняет интерактивную проверку подлинности, когда пользователь входит в систему через пользовательский интерфейс GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Интерактивная аутентификация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348062"
---
# <a name="interactive-authentication"></a><span data-ttu-id="91bd2-104">Интерактивная аутентификация</span><span class="sxs-lookup"><span data-stu-id="91bd2-104">Interactive Authentication</span></span>

<span data-ttu-id="91bd2-105">Проверка подлинности является интерактивной, когда пользователю предлагается ввести сведения для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="91bd2-105">Authentication is interactive when a user is prompted to supply logon information.</span></span> <span data-ttu-id="91bd2-106">[*Локальный центр безопасности*](../secgloss/l-gly.md) (LSA) выполняет интерактивную проверку подлинности, когда пользователь входит в систему через пользовательский интерфейс [*GINA*](../secgloss/g-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="91bd2-106">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) performs an interactive authentication when a user logs on through the [*GINA*](../secgloss/g-gly.md) user interface.</span></span> <span data-ttu-id="91bd2-107">На следующем рисунке показаны части типичной интерактивной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="91bd2-107">The following illustration shows the parts of a typical interactive authentication.</span></span>

![Интерактивная проверка подлинности](images/lsaint3.png)

<span data-ttu-id="91bd2-109">Пользователь сигнализирует системе начать последовательность входа, набрав сочетание клавиш CTRL + ALT [*+ Del (*](../secgloss/s-gly.md) SAS).</span><span class="sxs-lookup"><span data-stu-id="91bd2-109">A user signals the system to begin the logon sequence by typing the CTRL+ALT+DEL [*secure attention sequence*](../secgloss/s-gly.md) (SAS).</span></span> <span data-ttu-id="91bd2-110">[*Winlogon*](../secgloss/w-gly.md) получает SAS и вызывает GINA для вывода пользовательского интерфейса и получения данных входа пользователя, таких как имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="91bd2-110">[*Winlogon*](../secgloss/w-gly.md) receives the SAS and calls the GINA to display a user interface and obtain the user's logon data, such as a user name and password.</span></span>

<span data-ttu-id="91bd2-111">После получения данных входа GINA вызывает функцию [**лсалогонусер**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) для проверки подлинности пользователя, указывая, какой пакет проверки подлинности должен использоваться для вычисления данных входа в систему.</span><span class="sxs-lookup"><span data-stu-id="91bd2-111">After obtaining the logon data, the GINA calls the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) function to authenticate the user, specifying which authentication package must be used to evaluate the logon data.</span></span>

<span data-ttu-id="91bd2-112">LSA вызывает указанный пакет проверки подлинности и передает ему данные входа в систему.</span><span class="sxs-lookup"><span data-stu-id="91bd2-112">The LSA calls the specified authentication package and passes the logon data to it.</span></span> <span data-ttu-id="91bd2-113">Пакет проверки подлинности проверяет данные и определяет, успешно ли выполнена проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="91bd2-113">The authentication package examines the data and determines whether the authentication is successful.</span></span> <span data-ttu-id="91bd2-114">Результат проверки подлинности возвращается в LSA и из LSA в GINA.</span><span class="sxs-lookup"><span data-stu-id="91bd2-114">The authentication result is returned to the LSA and from the LSA, to the GINA.</span></span>

<span data-ttu-id="91bd2-115">GINA отображает успешное или неуспешное выполнение проверки подлинности пользователя и возвращает результат проверки подлинности в Winlogon.</span><span class="sxs-lookup"><span data-stu-id="91bd2-115">The GINA displays the success or failure of the authentication to the user and returns the result of the authentication to Winlogon.</span></span> <span data-ttu-id="91bd2-116">Если проверка подлинности прошла удачно, начнется сеанс входа пользователя, и набор [*учетных данных*](../secgloss/c-gly.md) для входа будет сохранен для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="91bd2-116">If the authentication succeeds, the user's logon session begins and a set of logon [*credentials*](../secgloss/c-gly.md) are saved for future reference.</span></span>

> [!Note]  
> <span data-ttu-id="91bd2-117">Как правило, разработчик, записывающий пользовательскую GINA для принятия специализированных данных входа в систему, таких как [*смарт-карта*](../secgloss/s-gly.md) или данные для просмотра сетчатки, также должен написать пакет проверки подлинности, отвечающий за обработку этих данных и определение его подлинности.</span><span class="sxs-lookup"><span data-stu-id="91bd2-117">In general, a developer who writes a custom GINA to accept specialized logon data, such as a [*smart card*](../secgloss/s-gly.md) or retinal-scan data, must also write an authentication package responsible for processing that data and determining its authenticity.</span></span>

 

<span data-ttu-id="91bd2-118">Дополнительные сведения о Winlogon и GINA см. в разделе [Winlogon и GINA](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="91bd2-118">For more information about Winlogon and GINAs, see [Winlogon and GINA](winlogon-and-gina.md).</span></span> <span data-ttu-id="91bd2-119">Дополнительные сведения о пакетах проверки подлинности см. в разделе [Создание настраиваемых пакетов безопасности](creating-custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="91bd2-119">For more information about authentication packages, see [Creating Custom Security Packages](creating-custom-security-packages.md).</span></span>

 

 
