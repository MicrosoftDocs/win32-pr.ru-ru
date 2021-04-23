---
title: Атрибуты объекта «пользователь»
description: Объект пользователя имеет несколько атрибутов. В этом разделе описываются ключевые атрибуты, используемые Windows, средства администрирования и адресная книга Windows (WAB). Он не описывает все атрибуты. для объекта User не используются многие атрибуты.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- Атрибуты объекта пользователя AD
- Пользователи AD, атрибуты объектов пользователя
- Объекты AD, пользователь, атрибуты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c90d8d5f28c41971f5f6910cfb8bef1fafd6f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987303"
---
# <a name="user-object-attributes"></a><span data-ttu-id="7f9b8-108">Атрибуты объекта «пользователь»</span><span class="sxs-lookup"><span data-stu-id="7f9b8-108">User Object Attributes</span></span>

<span data-ttu-id="7f9b8-109">Объект пользователя имеет несколько атрибутов.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-109">A user object has multiple attributes.</span></span> <span data-ttu-id="7f9b8-110">В этом разделе описываются ключевые атрибуты, используемые Windows, средства администрирования и адресная книга Windows (WAB).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-110">This section documents key attributes used by Windows, administrative tools, and the Windows Address Book (WAB).</span></span> <span data-ttu-id="7f9b8-111">Он не описывает все атрибуты. для объекта User не используются многие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-111">It does not describe all attributes; many attributes are not used for the user object.</span></span>

<span data-ttu-id="7f9b8-112">Некоторые атрибуты хранятся в каталоге, например [**CN**](/windows/desktop/ADSchema/a-cn), [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)и т. д., и реплицируются на все контроллеры домена в домене.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-112">Some attributes are stored in the directory, such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), and so on, and replicated to all domain controllers within a domain.</span></span> <span data-ttu-id="7f9b8-113">Подмножество этих атрибутов также реплицируется в глобальный каталог.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-113">A subset of these attributes is also replicated to the global catalog.</span></span>

<span data-ttu-id="7f9b8-114">Нереплицированные атрибуты хранятся на каждом контроллере домена, но не реплицируются в других местах, таких как [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**ластлогон**](/windows/desktop/ADSchema/a-lastlogon), [**ластлогофф**](/windows/desktop/ADSchema/a-lastlogoff)и т. д.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-114">Non-replicated attributes are stored on each domain controller, but are not replicated elsewhere, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), and so on.</span></span> <span data-ttu-id="7f9b8-115">Нереплицированные атрибуты — это атрибуты, относящиеся к конкретному контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-115">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="7f9b8-116">Например, **ластлогон** — это последняя Дата и время проверки сетевого входа пользователя на конкретный контроллер домена, который возвращает свойство.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-116">For example, **lastLogon** is the last date and time that the user network logon was validated by the particular domain controller that is returning the property.</span></span>

<span data-ttu-id="7f9b8-117">Объект пользователя также имеет сконструированные атрибуты, которые не хранятся в каталоге, но вычисляются контроллером домена, например [**каноникалнаме**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**алловедаттрибутес**](/windows/desktop/ADSchema/a-allowedattributes)и т. д.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-117">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), and so on.</span></span>

<span data-ttu-id="7f9b8-118">Атрибуты для пользовательских объектов классифицируются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7f9b8-118">Attributes for user objects are classified as:</span></span>

<dl> <dt>

<span data-ttu-id="7f9b8-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Атрибуты базового объекта</span><span class="sxs-lookup"><span data-stu-id="7f9b8-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Base Object Attributes</span></span>
</dt> <dd>

<span data-ttu-id="7f9b8-120">Эта категория содержит атрибуты, необходимые для всех объектов каталога, таких как [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)и т. д.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-120">This category includes attributes required for all directory objects, such as [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7f9b8-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Атрибуты именования</span><span class="sxs-lookup"><span data-stu-id="7f9b8-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Naming Attributes</span></span>
</dt> <dd>

<span data-ttu-id="7f9b8-122">В эту категорию входят атрибуты, используемые для обращения к объекту или его указания, такие как [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid)и т. д.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-122">This category includes attributes used to refer to or identify the object, such as [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), and so on.</span></span> <span data-ttu-id="7f9b8-123">Дополнительные сведения об именовании атрибутов для объектов User см. в разделе [атрибуты именования пользователей](naming-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-123">For more information about naming attributes for user objects, see [User Naming Attributes](naming-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f9b8-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Атрибуты безопасности</span><span class="sxs-lookup"><span data-stu-id="7f9b8-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Security Attributes</span></span>
</dt> <dd>

<span data-ttu-id="7f9b8-125">В эту категорию входят атрибуты для входа и контроля доступа.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-125">This category includes attributes for logon and access control.</span></span> <span data-ttu-id="7f9b8-126">Дополнительные сведения об атрибутах безопасности для объектов User см. в разделе [атрибуты безопасности пользователя](security-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-126">For more information about security attributes for user objects, see [User Security Attributes](security-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f9b8-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Атрибуты адресной книги</span><span class="sxs-lookup"><span data-stu-id="7f9b8-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Address Book Attributes</span></span>
</dt> <dd>

<span data-ttu-id="7f9b8-128">Эта категория включает атрибуты для электронной почты и пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-128">This category includes attributes for email and user data.</span></span> <span data-ttu-id="7f9b8-129">Дополнительные сведения об атрибутах адресной книги для объектов User см. в разделе [атрибуты адресной книги пользователя](address-book-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-129">For more information about address book attributes for user objects, see [User Address Book Attributes](address-book-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f9b8-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Атрибуты конкретного приложения</span><span class="sxs-lookup"><span data-stu-id="7f9b8-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Application Specific Attributes</span></span>
</dt> <dd>

<span data-ttu-id="7f9b8-131">В эту категорию входят пользовательские данные конфигурации для конкретных приложений.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-131">This category includes user-specific configuration data for specific applications.</span></span>

</dd> </dl>

<span data-ttu-id="7f9b8-132">Дополнительные сведения о чтении и изменении атрибутов объекта пользователя см. в разделе [чтение и запись атрибутов объектов в домен Active Directory Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-132">For more information about reading and modifying attributes for a user object, see [Reading and Writing Attributes of Objects in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="7f9b8-133">Дополнительные сведения о классе User, включая полный список атрибутов [**mayContain**](/windows/desktop/ADSchema/a-maycontain) и [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) класса, см. в разделе [**User**](/windows/desktop/ADSchema/c-user).</span><span class="sxs-lookup"><span data-stu-id="7f9b8-133">For more information about the User class, including a complete list of the [**mayContain**](/windows/desktop/ADSchema/a-maycontain) and [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) attributes of the class, see [**User**](/windows/desktop/ADSchema/c-user).</span></span>

## <a name="setting-passwords"></a><span data-ttu-id="7f9b8-134">Установка паролей</span><span class="sxs-lookup"><span data-stu-id="7f9b8-134">Setting Passwords</span></span>

<span data-ttu-id="7f9b8-135">Пароль пользователя нельзя изменить напрямую, так как это приведет к отправке незашифрованного пароля по сети.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-135">The password for a user cannot be modified directly because this would involve sending an unencrypted password over the network.</span></span> <span data-ttu-id="7f9b8-136">Чтобы задать пароль для пользователя, необходимо использовать метод [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) или [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="7f9b8-136">To set the password for a user, it is necessary to use the [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) or [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="7f9b8-137">Метод **IADsUser. ChangePassword** используется, когда приложение позволяет пользователю изменить свой пароль.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-137">The **IADsUser.ChangePassword** method is used when the application is allowing the user to change their own password.</span></span> <span data-ttu-id="7f9b8-138">Метод **IADsUser. SetPassword** используется, когда приложение позволяет администратору сбросить пароль.</span><span class="sxs-lookup"><span data-stu-id="7f9b8-138">The **IADsUser.SetPassword** method is used when the application enables an administrator to reset a password.</span></span>

 

 