---
description: Включение проверок доступа на уровне компонентов
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Включение проверок доступа на уровне компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701170"
---
# <a name="enabling-access-checks-at-the-component-level"></a><span data-ttu-id="b7b83-103">Включение проверок доступа на уровне компонентов</span><span class="sxs-lookup"><span data-stu-id="b7b83-103">Enabling Access Checks at the Component Level</span></span>

<span data-ttu-id="b7b83-104">Если приложение содержит компонент, для которого не требуются проверки безопасности, можно отключить проверку ролей для этого компонента, чтобы повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="b7b83-104">If your application includes a component that does not need security checks, you might decide to disable role checks for that component to improve performance.</span></span> <span data-ttu-id="b7b83-105">Или при отладке может быть полезно отключить безопасность, чтобы можно было сосредоточиться на других аспектах работы программы.</span><span class="sxs-lookup"><span data-stu-id="b7b83-105">Or when debugging, it might be helpful to disable security so that you can concentrate on other aspects of program functionality.</span></span>

<span data-ttu-id="b7b83-106">По умолчанию при установке компонента включены проверки доступа на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="b7b83-106">By default, when you install a component, component-level access checks are enabled.</span></span> <span data-ttu-id="b7b83-107">Однако это вступает в силу только в том случае, если [проверки доступа на уровне приложения](enabling-access-checks-for-an-application.md) включены и [уровень безопасности](setting-a-security-level-for-access-checks.md) настроен на **выполнение проверок доступа на уровне процесса и компонента**.</span><span class="sxs-lookup"><span data-stu-id="b7b83-107">However, this takes effect only when [application-level access checks](enabling-access-checks-for-an-application.md) are enabled and when the [security level](setting-a-security-level-for-access-checks.md) is set to **Perform access checks at the process and component level**.</span></span>

<span data-ttu-id="b7b83-108">**Включение или отключение проверки доступа на уровне компонента**</span><span class="sxs-lookup"><span data-stu-id="b7b83-108">**To enable or disable access checks at the component level**</span></span>

1.  <span data-ttu-id="b7b83-109">В дереве консоли средства администрирования "службы компонентов" выберите приложение COM+, содержащее компонент, для которого необходимо отключить (или включить) проверку роли.</span><span class="sxs-lookup"><span data-stu-id="b7b83-109">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the component for which you want to disable (or enable) role checks.</span></span> <span data-ttu-id="b7b83-110">Разверните представление в дереве, чтобы просмотреть компоненты в папке **Components** .</span><span class="sxs-lookup"><span data-stu-id="b7b83-110">Expand the view in the tree to view the components in the **Components** folder.</span></span>

2.  <span data-ttu-id="b7b83-111">Щелкните правой кнопкой мыши компонент, для которого необходимо включить проверку ролей, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="b7b83-111">Right-click the component for which you want to enable role checks, and then click **Properties**.</span></span>

3.  <span data-ttu-id="b7b83-112">В диалоговом окне Свойства компонента перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="b7b83-112">In the component properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="b7b83-113">Выберите **принудительно использовать проверки доступа на уровне компонентов** для принудительного применения проверок на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="b7b83-113">Select **Enforce component level access checks** to enforce component-level checks.</span></span>

5.  <span data-ttu-id="b7b83-114">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b7b83-114">Click **OK**.</span></span>

<span data-ttu-id="b7b83-115">Новый параметр вступит в силу при следующем запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="b7b83-115">The new setting will take effect the next time the application is started.</span></span>

> [!Note]  
> <span data-ttu-id="b7b83-116">Начиная с Windows Server 2003 проверки доступа на уровне компонентов по умолчанию отключены при создании приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="b7b83-116">As of Windows Server 2003, component-level access checks are disabled by default when creating a COM+ application.</span></span> <span data-ttu-id="b7b83-117">Проверки доступа по умолчанию включены на уровне приложения и по умолчанию отключены на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="b7b83-117">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="b7b83-118">Ранее проверки доступа были отключены по умолчанию на уровне приложения и включены по умолчанию на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="b7b83-118">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b7b83-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b7b83-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7b83-120">Назначение ролей компонентам, интерфейсам или методам</span><span class="sxs-lookup"><span data-stu-id="b7b83-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="b7b83-121">Настройка безопасности Role-Based</span><span class="sxs-lookup"><span data-stu-id="b7b83-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="b7b83-122">Определение ролей для приложения</span><span class="sxs-lookup"><span data-stu-id="b7b83-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="b7b83-123">Включение проверок доступа для приложения</span><span class="sxs-lookup"><span data-stu-id="b7b83-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="b7b83-124">Настройка уровня безопасности для проверок доступа</span><span class="sxs-lookup"><span data-stu-id="b7b83-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



