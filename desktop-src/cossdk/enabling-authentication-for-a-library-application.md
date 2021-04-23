---
description: Включение проверки подлинности для библиотечного приложения
ms.assetid: 80c80c14-ceef-4a74-810d-6aa3cc320cef
title: Включение проверки подлинности для библиотечного приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cfa9f2a6a5e3c1312fa13e0aff1e9f4ea17e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682354"
---
# <a name="enabling-authentication-for-a-library-application"></a><span data-ttu-id="f7580-103">Включение проверки подлинности для библиотечного приложения</span><span class="sxs-lookup"><span data-stu-id="f7580-103">Enabling Authentication for a Library Application</span></span>

<span data-ttu-id="f7580-104">Так как приложения библиотеки COM+ размещаются в других процессах, их требования к безопасности могут отличаться от требований, предъявляемых к серверным приложениям.</span><span class="sxs-lookup"><span data-stu-id="f7580-104">Because COM+ library applications are hosted by other processes, their security requirements may be different from those of server applications.</span></span> <span data-ttu-id="f7580-105">Если приложение библиотеки будет размещено в браузере, может потребоваться получение обратных вызовов, не прошедших проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="f7580-105">If the library application will be hosted by a browser, it might need to receive unauthenticated callbacks.</span></span>

<span data-ttu-id="f7580-106">Чтобы решить эту необходимость, можно отключить проверку подлинности, чтобы ведущий процесс не выполнял проверку безопасности для вызывающих объектов приложения библиотеки.</span><span class="sxs-lookup"><span data-stu-id="f7580-106">To address this need, you can disable authentication so that the hosting process does not perform security checks for callers of the library application.</span></span> <span data-ttu-id="f7580-107">При отключении проверки подлинности вызовы приложения библиотеки эффективно проходят без проверки подлинности — все вызовы будут выполнены успешно.</span><span class="sxs-lookup"><span data-stu-id="f7580-107">When you disable authentication, calls to the library application effectively go unauthenticated—all calls to it will succeed.</span></span> <span data-ttu-id="f7580-108">Дополнительные сведения см. в разделе [Библиотека Application Security](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="f7580-108">For more information, see [Library Application Security](library-application-security.md).</span></span>

<span data-ttu-id="f7580-109">**Включение или отключение проверки подлинности для библиотечного приложения**</span><span class="sxs-lookup"><span data-stu-id="f7580-109">**To enable (or disable) authentication for a library application**</span></span>

1.  <span data-ttu-id="f7580-110">Щелкните правой кнопкой мыши приложение COM+, для которого включается или отключается проверка подлинности, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="f7580-110">Right-click the COM+ application for which you are enabling or disabling authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="f7580-111">В диалоговом окне Свойства приложения перейдите на вкладку **Безопасность** .</span><span class="sxs-lookup"><span data-stu-id="f7580-111">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="f7580-112">В разделе **Проверка** подлинности установите флажок **включить проверку подлинности** , чтобы включить проверку подлинности. Снятие флажка приведет к отключению проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f7580-112">Under **Authentication**, select the **Enable authentication** check box to enable authentication; clearing the check box will disable authentication.</span></span>

4.  <span data-ttu-id="f7580-113">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f7580-113">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7580-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f7580-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7580-115">Установка уровня проверки подлинности для серверного приложения</span><span class="sxs-lookup"><span data-stu-id="f7580-115">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 



