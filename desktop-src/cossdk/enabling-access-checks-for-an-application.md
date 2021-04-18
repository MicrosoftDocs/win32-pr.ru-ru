---
description: Выполнение этого шага включает проверку доступа к процессу или полную безопасность на основе ролей, в зависимости от выбранного уровня безопасности и включение проверки доступа для отдельных компонентов.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Включение проверок доступа для приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692010"
---
# <a name="enabling-access-checks-for-an-application"></a><span data-ttu-id="564b9-103">Включение проверок доступа для приложения</span><span class="sxs-lookup"><span data-stu-id="564b9-103">Enabling Access Checks for an Application</span></span>

<span data-ttu-id="564b9-104">Выполнение этого шага включает проверку доступа к процессу или полную безопасность на основе ролей, в зависимости от выбранного уровня безопасности и включение проверки доступа для отдельных компонентов.</span><span class="sxs-lookup"><span data-stu-id="564b9-104">Performing this step enables either process access checks or full role-based security, depending on what security level you select and whether you enable access checking for individual components.</span></span>

<span data-ttu-id="564b9-105">**Включение проверки доступа для приложения**</span><span class="sxs-lookup"><span data-stu-id="564b9-105">**To enable access checks for an application**</span></span>

1.  <span data-ttu-id="564b9-106">В дереве консоли средства администрирования "службы компонентов" щелкните правой кнопкой мыши приложение COM+, для которого требуется включить проверки доступа, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="564b9-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="564b9-107">В диалоговом окне Свойства приложения перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="564b9-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="564b9-108">Установите флажок **Принудительная проверка доступа для этого приложения** .</span><span class="sxs-lookup"><span data-stu-id="564b9-108">Select the **Enforce access checks for this application** check box.</span></span>

4.  <span data-ttu-id="564b9-109">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="564b9-109">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="564b9-110">Начиная с Windows Server 2003, проверки доступа по умолчанию включены при создании приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="564b9-110">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="564b9-111">Проверки доступа по умолчанию включены на уровне приложения и по умолчанию отключены на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="564b9-111">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="564b9-112">Ранее проверки доступа были отключены по умолчанию на уровне приложения и включены по умолчанию на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="564b9-112">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

<span data-ttu-id="564b9-113">После включения проверки доступа следует выбрать соответствующий уровень безопасности.</span><span class="sxs-lookup"><span data-stu-id="564b9-113">After enabling access checks, you should select the appropriate security level.</span></span> <span data-ttu-id="564b9-114">См. раздел [Настройка уровня безопасности для проверок доступа](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="564b9-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span> <span data-ttu-id="564b9-115">Кроме того, необходимо определить роли и добавить их в приложение.</span><span class="sxs-lookup"><span data-stu-id="564b9-115">Also, you must be sure to define roles and add them to the application.</span></span> <span data-ttu-id="564b9-116">Если проверки доступа включены, но роли не были добавлены, все вызовы приложения завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="564b9-116">If access checks are enabled but no roles have been added, all calls to the application will fail.</span></span> <span data-ttu-id="564b9-117">См. раздел [Определение ролей для приложения](defining-roles-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="564b9-117">See [Defining Roles for an Application](defining-roles-for-an-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="564b9-118">При отладке приложения может быть полезно отключить безопасность, чтобы можно было сосредоточиться на других аспектах поведения и конструкции программы.</span><span class="sxs-lookup"><span data-stu-id="564b9-118">When debugging your application, it might be helpful to disable security so that you can concentrate on other aspects of your program's behavior and design.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="564b9-119">См. также</span><span class="sxs-lookup"><span data-stu-id="564b9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="564b9-120">Назначение ролей компонентам, интерфейсам или методам</span><span class="sxs-lookup"><span data-stu-id="564b9-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="564b9-121">Настройка безопасности Role-Based</span><span class="sxs-lookup"><span data-stu-id="564b9-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="564b9-122">Определение ролей для приложения</span><span class="sxs-lookup"><span data-stu-id="564b9-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="564b9-123">Включение проверок доступа на уровне компонентов</span><span class="sxs-lookup"><span data-stu-id="564b9-123">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="564b9-124">Настройка уровня безопасности для проверок доступа</span><span class="sxs-lookup"><span data-stu-id="564b9-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



