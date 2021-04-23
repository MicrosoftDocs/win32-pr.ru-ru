---
title: Активация сеанса в сеансе с моникером сеанса
description: Активация между сеансами (также называемая межсеансией активации) позволяет клиентскому процессу запускать (активировать) процесс локального сервера в указанном сеансе.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793363"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a><span data-ttu-id="3e8eb-103">Активация сеанса в сеансе с моникером сеанса</span><span class="sxs-lookup"><span data-stu-id="3e8eb-103">Session-to-Session Activation with a Session Moniker</span></span>

<span data-ttu-id="3e8eb-104">Активация между сеансами (также называемая межсеансией активации) позволяет клиентскому процессу запускать (активировать) процесс локального сервера в указанном сеансе.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-104">Session-to-session activation (also called cross-session activation) allows a client process to start (activate) a local server process on a specified session.</span></span> <span data-ttu-id="3e8eb-105">Эта функция доступна для приложений, настроенных для запуска в контексте безопасности интерактивного пользователя, также известного как режим активации "Интерактивный пользователь запуска от имени".</span><span class="sxs-lookup"><span data-stu-id="3e8eb-105">This feature is available for applications that are configured to run in the security context of the interactive user, also known as the "RunAs Interactive User" object activation mode.</span></span> <span data-ttu-id="3e8eb-106">Дополнительные сведения о контекстах безопасности см. в описании [контекста безопасности клиента](/windows/desktop/SecAuthZ/the-client-security-context).</span><span class="sxs-lookup"><span data-stu-id="3e8eb-106">For more information about security contexts, see [The Client's Security Context](/windows/desktop/SecAuthZ/the-client-security-context).</span></span>

<span data-ttu-id="3e8eb-107">Распределенная модель COM (DCOM) обеспечивает активацию объектов для каждого сеанса с помощью предоставленного системой [моникера сеанса](session-monikers.md).</span><span class="sxs-lookup"><span data-stu-id="3e8eb-107">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied [Session Moniker](session-monikers.md).</span></span> <span data-ttu-id="3e8eb-108">Другие предоставляемые системой моникеры включают [моникеры файлов](../com/file-monikers.md), [моникеры элементов](../com/item-monikers.md), универсальные [Составные моникеры](../com/composite-monikers.md), [средства защиты от](../com/anti-monikers.md)моникеров, [моникеры указателей](../com/pointer-monikers.md)и [моникеры URL-адресов](../com/url-monikers.md).</span><span class="sxs-lookup"><span data-stu-id="3e8eb-108">Other system-supplied monikers include [file monikers](../com/file-monikers.md), [item monikers](../com/item-monikers.md), generic [composite monikers](../com/composite-monikers.md), [anti-monikers](../com/anti-monikers.md), [pointer monikers](../com/pointer-monikers.md), and [URL monikers](../com/url-monikers.md).</span></span>

<span data-ttu-id="3e8eb-109">Чтобы иметь возможность использовать моникер сеанса, приложение DCOM должно быть настроено для запуска от имени интерактивного пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-109">To be able to use the session moniker, the DCOM application must be set to run as the interactive user.</span></span> <span data-ttu-id="3e8eb-110">Это можно задать с помощью средства администрирования "службы компонентов", просмотра свойств приложения DCOM и выбора **интерактивного пользователя** на вкладке **удостоверение** . Дополнительные сведения о возможных угрозах безопасности, связанных с настройкой DCOM-приложения для запуска в качестве интерактивного пользователя в среде службы удаленных рабочих столов, см. в разделе "удостоверение приложения (COM)" документации по COM в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-110">This can be set by using the Component Services Administrative tool, viewing the Properties of the DCOM application, and selecting **The interactive user** on the **Identity** tab. For more information about the possible security risks associated with setting a DCOM application to run as the interactive user in a Remote Desktop Services environment, see the "Application Identity (COM)" section of the COM documentation in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="3e8eb-111">Если для запуска приложения выбран какой-либо другой тип пользователя, моникер сеанса будет игнорироваться приложением.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-111">If any other type of user is selected to run the application, the session moniker will be ignored by the application.</span></span> <span data-ttu-id="3e8eb-112">Моникер сеанса также игнорируется серверными приложениями COM+.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-112">The session moniker is also ignored by COM+ server applications.</span></span> <span data-ttu-id="3e8eb-113">Дополнительные сведения о других способах выбора типа пользователя для запуска приложения см. в документации по COM в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-113">For more information about other methods for selecting the type of user to run the application, see the COM documentation in the Platform SDK.</span></span>

<span data-ttu-id="3e8eb-114">Чтобы создать моникер сеанса, необходимо составить идентификатор сеанса службы удаленных рабочих столов сеанса с моникером класса, который указывает идентификатор класса сервера обработки.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-114">To create a session moniker, you must compose the session ID of the Remote Desktop Services session with a class moniker that specifies the process server's class ID.</span></span>

<span data-ttu-id="3e8eb-115">**Создание моникера сеанса**</span><span class="sxs-lookup"><span data-stu-id="3e8eb-115">**To create a session moniker**</span></span>

1.  <span data-ttu-id="3e8eb-116">Добавьте перед отображаемым именем моникера класса отображаемое имя моникера сеанса, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="3e8eb-116">Prefix the display name of the class moniker with the display name of the session moniker by using the following syntax:</span></span>

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    <span data-ttu-id="3e8eb-117">где *digits* представляет идентификатор сеанса, в котором будет запущен серверный процесс, и где *идентификатор класса* представляет идентификатор класса сервера.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-117">where *digits* represents the session ID of the session on which the server process will be started, and where *class id* represents the class ID of the server.</span></span> <span data-ttu-id="3e8eb-118">Обратите внимание, что идентификатор сеанса — это номер основания 10.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-118">Note that the session ID is a base-10 number.</span></span>

    <span data-ttu-id="3e8eb-119">Для компьютеров, работающих под управлением Windows XP или более поздней версии, при использовании следующего синтаксиса COM отправляет активацию в текущий активный сеанс физической консоли, независимо от его идентификатора сеанса:</span><span class="sxs-lookup"><span data-stu-id="3e8eb-119">For computers that are running Windows XP or later, using the following syntax will result in COM sending the activation to the currently active physical console session, whatever its session ID is:</span></span>

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  <span data-ttu-id="3e8eb-120">После создания моникера сеанса можно передать результат в функцию [**мкпарседисплайнаме**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) или функцию [мкпарседисплайнамикс](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3e8eb-120">After you have created the session moniker, you can pass the result to either the [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) function or the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function.</span></span>

<span data-ttu-id="3e8eb-121">Моникер сеанса можно использовать так же, как и любой другой моникер.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-121">You can use a session moniker in the same way as you would use any other moniker.</span></span>

<span data-ttu-id="3e8eb-122">Пример кода, демонстрирующий активацию локального серверного процесса в указанном сеансе, см. в разделе [Использование моникера сеанса](using-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="3e8eb-122">For a code sample that demonstrates how to activate a local server process on a specified session, see [Using a Session Moniker](using-a-session-moniker.md).</span></span>

<span data-ttu-id="3e8eb-123">Дополнительные сведения об активации объектов, предоставляемых системой моникерах и моникерах классов см. в документации по COM в пакете Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-123">For more information about object activation, system-supplied monikers and class monikers, see the COM documentation in the Platform SDK.</span></span>

> [!Note]  
> <span data-ttu-id="3e8eb-124">Процессы, создаваемые во всех сеансах, имеют верхний предел размера блока среды.</span><span class="sxs-lookup"><span data-stu-id="3e8eb-124">Processes that are created across sessions have an upper limit on the size of the environment block.</span></span> <span data-ttu-id="3e8eb-125">Это ограничение составляет около 4 КБ, но может быть больше или меньше в зависимости от того, какие другие сведения необходимы для создания процесса (например, имена файлов, каталоги и параметры для нового процесса).</span><span class="sxs-lookup"><span data-stu-id="3e8eb-125">This limit is around 4 KB, but it can be larger or smaller depending on what other information is needed to create the process (for example file names, directories, and parameters for the new process).</span></span>

 

 

 