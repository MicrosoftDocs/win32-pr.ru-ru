---
description: Доступом к пространствам имен WMI и их данным управляют дескрипторы безопасности.
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: Защита пространств имен WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711661"
---
# <a name="securing-wmi-namespaces"></a><span data-ttu-id="9f862-103">Защита пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="9f862-103">Securing WMI Namespaces</span></span>

<span data-ttu-id="9f862-104">Доступом к пространствам имен WMI и их данным управляют [*дескрипторы безопасности*](gloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="9f862-104">Access to WMI namespaces and their data is controlled by [*security descriptors*](gloss-s.md).</span></span> <span data-ttu-id="9f862-105">Вы можете защитить данные в [*пространствах имен*](gloss-n.md) , настроив дескриптор безопасности пространства имен, чтобы управлять доступом к данным и методам.</span><span class="sxs-lookup"><span data-stu-id="9f862-105">You can protect data in your [*namespaces*](gloss-n.md) by adjusting the namespace security descriptor to control who has access to the data and methods.</span></span> <span data-ttu-id="9f862-106">Дополнительные сведения см. [в разделе доступ к защищаемым ОБЪЕКТАМ WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9f862-106">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>


<span data-ttu-id="9f862-107">В следующих разделах описывается безопасность пространства имен WMI и управление доступом к пространствам имен.</span><span class="sxs-lookup"><span data-stu-id="9f862-107">The following topics describe WMI namespace security and how to control access to namespaces.</span></span>

<dl> <dt>

<span data-ttu-id="9f862-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Доступ к пространствам имен WMI](access-to-wmi-namespaces.md)</span><span class="sxs-lookup"><span data-stu-id="9f862-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Access to WMI Namespaces](access-to-wmi-namespaces.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f862-109">Безопасность пространства имен WMI зависит от стандартных [*идентификаторов безопасности*](/windows/desktop/SecGloss/s-gly) пользователей Windows (SID) и списков управления доступом.</span><span class="sxs-lookup"><span data-stu-id="9f862-109">WMI namespace security relies on standard Windows user [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) and access control lists.</span></span> <span data-ttu-id="9f862-110">Администраторы и пользователи имеют разные разрешения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9f862-110">Administrators and users have different default permissions.</span></span>

</dd> <dt>

<span data-ttu-id="9f862-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Задание дескрипторов безопасности пространства имен](setting-namespace-security-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="9f862-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f862-112">После существования пространства имен в репозитории WMI можно изменить безопасность пространства имен с помощью элемента управления WMI или путем вызова методов [**\_ \_ системсекурити**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="9f862-112">After a namespace exists in the WMI repository, you can change the security on the namespace by using the WMI Control or by calling the methods of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f862-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Требуется зашифрованное соединение с пространством имен](requiring-an-encrypted-connection-to-a-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f862-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f862-114">Квалификатор **рекуиресенкриптион** в пространстве имен требует, чтобы клиентское приложение WMI или сценарий использовали уровень проверки подлинности, который шифрует удаленные вызовы процедур.</span><span class="sxs-lookup"><span data-stu-id="9f862-114">The **RequiresEncryption** qualifier on a namespace requires the WMI client application or script to use the authentication level which encrypts remote procedure calls.</span></span> <span data-ttu-id="9f862-115">Как входящие запросы данных, так и асинхронные обратные вызовы должны быть зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="9f862-115">Both incoming data requests and asynchronous callbacks must be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="9f862-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Установка наследования безопасности пространства имен](establishing-inheritance-of-namespace-security.md)</span><span class="sxs-lookup"><span data-stu-id="9f862-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establishing Inheritance of Namespace Security](establishing-inheritance-of-namespace-security.md)</span></span>
</dt> <dd>

<span data-ttu-id="9f862-117">Можно контролировать, наследует ли Дочернее пространство имен дескриптор безопасности родительского пространства имен.</span><span class="sxs-lookup"><span data-stu-id="9f862-117">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="9f862-118">См. также</span><span class="sxs-lookup"><span data-stu-id="9f862-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f862-119">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="9f862-119">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="9f862-120">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="9f862-120">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="9f862-121">Создание пространства имен с помощью API инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="9f862-121">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[<span data-ttu-id="9f862-122">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="9f862-122">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
