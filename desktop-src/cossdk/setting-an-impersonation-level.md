---
description: При задании уровня олицетворения для приложения определяется, какой уровень полномочий приложение предоставляет другим приложениям для использования его удостоверения при его вызове.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Установка уровня олицетворения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141797"
---
# <a name="setting-an-impersonation-level"></a><span data-ttu-id="766db-103">Установка уровня олицетворения</span><span class="sxs-lookup"><span data-stu-id="766db-103">Setting an Impersonation Level</span></span>

<span data-ttu-id="766db-104">При задании уровня олицетворения для приложения определяется, какой уровень полномочий приложение предоставляет другим приложениям для использования его удостоверения при его вызове.</span><span class="sxs-lookup"><span data-stu-id="766db-104">When you set an impersonation level for an application, you determine what degree of authority the application grants other applications to use its identity when it calls them.</span></span> <span data-ttu-id="766db-105">Это значение можно задать только для серверных приложений COM+ — приложения библиотеки выполняются под удостоверением ведущего процесса и используют уровень олицетворения, который он указывает.</span><span class="sxs-lookup"><span data-stu-id="766db-105">You can set this only for COM+ server applications—library applications run under the identity of the hosting process and use the impersonation level that it specifies.</span></span> <span data-ttu-id="766db-106">Дополнительные сведения см. в разделе [уровни олицетворения](/windows/desktop/com/impersonation-levels).</span><span class="sxs-lookup"><span data-stu-id="766db-106">For more detail, see [Impersonation Levels](/windows/desktop/com/impersonation-levels).</span></span>

<span data-ttu-id="766db-107">**Выбор уровня олицетворения**</span><span class="sxs-lookup"><span data-stu-id="766db-107">**To select an impersonation level**</span></span>

1.  <span data-ttu-id="766db-108">Щелкните правой кнопкой мыши приложение COM+, для которого задается олицетворение, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="766db-108">Right-click the COM+ application for which you are setting impersonation, and then click **Properties**.</span></span>

2.  <span data-ttu-id="766db-109">В диалоговом окне Свойства приложения перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="766db-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="766db-110">В поле **уровень олицетворения** выберите соответствующий уровень.</span><span class="sxs-lookup"><span data-stu-id="766db-110">In the **Impersonation level** box, select the appropriate level.</span></span> <span data-ttu-id="766db-111">Ниже приведены уровни, упорядоченные от предоставления минимума более глубокому центру:</span><span class="sxs-lookup"><span data-stu-id="766db-111">The levels are as follows, ordered from granting least to greatest authority:</span></span>

    -   <span data-ttu-id="766db-112">**Анонимно**.</span><span class="sxs-lookup"><span data-stu-id="766db-112">**Anonymous**.</span></span> <span data-ttu-id="766db-113">Клиент анонимен по отношению к серверу.</span><span class="sxs-lookup"><span data-stu-id="766db-113">The client is anonymous to the server.</span></span> <span data-ttu-id="766db-114">Сервер может олицетворять клиента, но маркер олицетворения (локальные учетные данные) не содержит никаких сведений о клиенте.</span><span class="sxs-lookup"><span data-stu-id="766db-114">The server can impersonate the client, but the impersonation token (a local credential) does not contain any information about the client.</span></span>
    -   <span data-ttu-id="766db-115">**Выявление**.</span><span class="sxs-lookup"><span data-stu-id="766db-115">**Identify**.</span></span> <span data-ttu-id="766db-116">Сервер может получить удостоверение клиента и выполнить олицетворение клиента для проверки списка ACL.</span><span class="sxs-lookup"><span data-stu-id="766db-116">The server can obtain the client's identity and can impersonate the client to do ACL checks.</span></span>
    -   <span data-ttu-id="766db-117">**Олицетворять**.</span><span class="sxs-lookup"><span data-stu-id="766db-117">**Impersonate**.</span></span> <span data-ttu-id="766db-118">Сервер может олицетворять клиента, действуя от его имени, хотя и с ограничениями.</span><span class="sxs-lookup"><span data-stu-id="766db-118">The server can impersonate the client while acting on its behalf, although with restrictions.</span></span> <span data-ttu-id="766db-119">Сервер может обращаться к ресурсам на том же компьютере, что и клиент.</span><span class="sxs-lookup"><span data-stu-id="766db-119">The server can access resources on the same computer as the client.</span></span> <span data-ttu-id="766db-120">Если сервер находится на том же компьютере, что и клиент, он может получить доступ к сетевым ресурсам в качестве клиента.</span><span class="sxs-lookup"><span data-stu-id="766db-120">If the server is on the same computer as the client, it can access network resources as the client.</span></span> <span data-ttu-id="766db-121">Если сервер находится на компьютере, отличном от клиента, он может получить доступ только к тем ресурсам, которые находятся на том же компьютере, что и сервер.</span><span class="sxs-lookup"><span data-stu-id="766db-121">If the server is on a computer different from the client, it can access only resources that are on the same computer as the server.</span></span> <span data-ttu-id="766db-122">Это значение по умолчанию для серверных приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="766db-122">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="766db-123">**Делегат**.</span><span class="sxs-lookup"><span data-stu-id="766db-123">**Delegate**.</span></span> <span data-ttu-id="766db-124">Сервер может олицетворять клиента, действуя от его имени, будь то на том же компьютере, что и клиент.</span><span class="sxs-lookup"><span data-stu-id="766db-124">The server can impersonate the client while acting on its behalf, whether on the same computer as the client.</span></span> <span data-ttu-id="766db-125">Во время олицетворения учетные данные клиента (как с локальными, так и с учетом допустимой сети) могут быть переданы на любое количество компьютеров.</span><span class="sxs-lookup"><span data-stu-id="766db-125">During impersonation, the client's credentials (both those with local and those with network validity) can be passed to any number of machines.</span></span>

4.  <span data-ttu-id="766db-126">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="766db-126">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="766db-127">См. также</span><span class="sxs-lookup"><span data-stu-id="766db-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="766db-128">Настройка безопасности Role-Based</span><span class="sxs-lookup"><span data-stu-id="766db-128">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="766db-129">Настройка политики ограниченного использования программ</span><span class="sxs-lookup"><span data-stu-id="766db-129">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="766db-130">Включение проверки подлинности для библиотечного приложения</span><span class="sxs-lookup"><span data-stu-id="766db-130">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="766db-131">Установка уровня проверки подлинности для серверного приложения</span><span class="sxs-lookup"><span data-stu-id="766db-131">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
