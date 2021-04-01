---
description: Настройка политики ограниченного использования программ
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Настройка политики ограниченного использования программ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072521"
---
# <a name="configuring-the-software-restriction-policy"></a><span data-ttu-id="49721-103">Настройка политики ограниченного использования программ</span><span class="sxs-lookup"><span data-stu-id="49721-103">Configuring the Software Restriction Policy</span></span>

<span data-ttu-id="49721-104">При явном задании уровней доверия политики ограниченного использования программ для приложения COM+ вы переопределяете параметры по умолчанию для всей системы.</span><span class="sxs-lookup"><span data-stu-id="49721-104">When you explicitly set the software restriction policy trust levels of a COM+ application, you are overriding the default systemwide settings.</span></span> <span data-ttu-id="49721-105">Это часто требуется для серверных приложений COM+, так как уровень доверия в общедоступной области устанавливается одинаково для всех серверных приложений (поскольку все они работают в одном файле, dllhost.exe).</span><span class="sxs-lookup"><span data-stu-id="49721-105">This is often necessary for COM+ server applications because the systemwide trust level is set the same for all server applications (because they all run in the same file, dllhost.exe).</span></span> <span data-ttu-id="49721-106">Однако если задать уровень доверия политики ограниченного использования программ для приложения библиотеки COM+, то вы повлияете на конфигурацию приложения для всей системы.</span><span class="sxs-lookup"><span data-stu-id="49721-106">However, when you set the software restriction policy trust level of a COM+ library application, you are affecting the systemwide configuration for that application.</span></span> <span data-ttu-id="49721-107">Обсуждение применения политики ограниченного использования программ в COM+ см. в разделе [Использование политики ограниченного использования программ в com+](using-the-software-restriction-policy-in-com-.md).</span><span class="sxs-lookup"><span data-stu-id="49721-107">For a discussion of how to use the software restriction policy in COM+, see [Using the Software Restriction Policy in COM+](using-the-software-restriction-policy-in-com-.md).</span></span>

<span data-ttu-id="49721-108">**Настройка политики ограниченного использования программ**</span><span class="sxs-lookup"><span data-stu-id="49721-108">**To set the software restriction policy**</span></span>

1.  <span data-ttu-id="49721-109">Щелкните правой кнопкой мыши приложение COM+, для которого задается политика ограниченного использования программ, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="49721-109">Right-click the COM+ application for which you are setting the software restriction policy, and then click **Properties**.</span></span>

2.  <span data-ttu-id="49721-110">В диалоговом окне Свойства приложения перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="49721-110">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="49721-111">В разделе **политика ограниченного использования программ** установите флажок **Применить политику ограниченного использования программ** . Это позволяет задать уровень доверия.</span><span class="sxs-lookup"><span data-stu-id="49721-111">Under **Software Restriction Policy**, select the **Apply software restriction policy** check box; this enables you to set the trust level.</span></span> <span data-ttu-id="49721-112">Снятие флажка приведет к тому, что COM+ будет использовать конфигурацию всей системы политики ограниченного использования программ для приложения.</span><span class="sxs-lookup"><span data-stu-id="49721-112">Clearing the check box will cause COM+ to use the systemwide configuration of the software restriction policy for the application.</span></span> <span data-ttu-id="49721-113">Этот флажок соответствует свойству Српенаблед коллекции [**приложений**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="49721-113">This check box corresponds to the SRPEnabled property of the [**Applications**](applications.md) collection.</span></span>

4.  <span data-ttu-id="49721-114">В поле **уровень ограничений** выберите соответствующий уровень.</span><span class="sxs-lookup"><span data-stu-id="49721-114">In the **Restriction Level** box, select the appropriate level.</span></span> <span data-ttu-id="49721-115">Это раскрывающийся список соответствует свойству Срптрустлевел коллекции [**приложений**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="49721-115">This drop-down box corresponds to the SRPTrustLevel property of the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="49721-116">Ниже приведены уровни, упорядоченные по крайней мере до наиболее надежного.</span><span class="sxs-lookup"><span data-stu-id="49721-116">The levels are as follows, ordered from least to most trusted:</span></span>

    -   <span data-ttu-id="49721-117">**Запрещено**.</span><span class="sxs-lookup"><span data-stu-id="49721-117">**Disallowed**.</span></span> <span data-ttu-id="49721-118">Приложению запрещено использовать полные привилегии пользователя.</span><span class="sxs-lookup"><span data-stu-id="49721-118">The application is disallowed from using the full privileges of the user.</span></span> <span data-ttu-id="49721-119">В него можно загрузить компоненты с любым уровнем доверия.</span><span class="sxs-lookup"><span data-stu-id="49721-119">Components with any trust level can be loaded into it.</span></span>
    -   <span data-ttu-id="49721-120">Без **ограничений**.</span><span class="sxs-lookup"><span data-stu-id="49721-120">**Unrestricted**.</span></span> <span data-ttu-id="49721-121">Приложение имеет неограниченный доступ к привилегиям пользователя.</span><span class="sxs-lookup"><span data-stu-id="49721-121">The application has unrestricted access to the user's privileges.</span></span> <span data-ttu-id="49721-122">В него можно загрузить только компоненты с неограниченным уровнем доверия.</span><span class="sxs-lookup"><span data-stu-id="49721-122">Only components with an Unrestricted trust level can be loaded into it.</span></span>

5.  <span data-ttu-id="49721-123">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="49721-123">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49721-124">См. также</span><span class="sxs-lookup"><span data-stu-id="49721-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49721-125">Настройка безопасности Role-Based</span><span class="sxs-lookup"><span data-stu-id="49721-125">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="49721-126">Включение проверки подлинности для библиотечного приложения</span><span class="sxs-lookup"><span data-stu-id="49721-126">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="49721-127">Установка уровня проверки подлинности для серверного приложения</span><span class="sxs-lookup"><span data-stu-id="49721-127">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[<span data-ttu-id="49721-128">Установка уровня олицетворения</span><span class="sxs-lookup"><span data-stu-id="49721-128">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



