---
title: Тип файла и модель сопоставлений URI
description: Тип файла и модель сопоставлений URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "104070758"
---
# <a name="file-type-and-uri-associations-model"></a><span data-ttu-id="2e618-103">Тип файла и модель сопоставлений URI</span><span class="sxs-lookup"><span data-stu-id="2e618-103">File type and URI associations model</span></span>

## <a name="platforms"></a><span data-ttu-id="2e618-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="2e618-104">Platforms</span></span>

 <span data-ttu-id="2e618-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="2e618-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="2e618-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e618-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="2e618-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2e618-107">Description</span></span>

<span data-ttu-id="2e618-108">Тип файла и модель взаимосвязей URI изменились в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2e618-108">The file type and URI association model has changed in Windows 8.</span></span> <span data-ttu-id="2e618-109">Приложения больше не могут быть заданы программными средствами в качестве обработчика по умолчанию для типа файла или URI.</span><span class="sxs-lookup"><span data-stu-id="2e618-109">Apps are no longer able to programmatically set themselves as the default handler for a file type or URI.</span></span> <span data-ttu-id="2e618-110">Вместо этого пользователь всегда управляет тем, какой обработчик по умолчанию предназначен для типа файла или схемы URI.</span><span class="sxs-lookup"><span data-stu-id="2e618-110">Instead, now the user always controls what the default handler is for a file type or URI scheme.</span></span>

## <a name="manifestation"></a><span data-ttu-id="2e618-111">Проявление</span><span class="sxs-lookup"><span data-stu-id="2e618-111">Manifestation</span></span>

<span data-ttu-id="2e618-112">Способ представления этого изменения зависит от способа разработки приложения, например:</span><span class="sxs-lookup"><span data-stu-id="2e618-112">How this change presents to the user depends upon how the app is designed, for example:</span></span>

-   <span data-ttu-id="2e618-113">Многие приложения проверяют, являются ли они стандартными по умолчанию при каждом запуске, и, если они нет, пользователь запрашивает у пользователя разрешение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2e618-113">Many apps check to see if they are the default every time they run and, if they are not, they prompt the user to set them as default.</span></span> <span data-ttu-id="2e618-114">Однако, поскольку приложения больше не могут выполнять запрос, чтобы определить, какое приложение является обработчиком по умолчанию для типа файлов или схемы URI, ни одна из этих операций не работает.</span><span class="sxs-lookup"><span data-stu-id="2e618-114">However, because apps can no longer accurately query to determine which app is the default handler for a file type or URI scheme, neither of these operations works.</span></span>
-   <span data-ttu-id="2e618-115">Во многих приложениях имеется диалоговое окно или меню, встроенное в, или в установщик, указывающий типы файлов, для которых приложение должно использоваться по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2e618-115">Many apps have a dialog box or menu built in or in their installer that specifies the file types for which the app should serve as the default.</span></span> <span data-ttu-id="2e618-116">Однако, поскольку приложения больше не могут быть заданы программным способом в качестве обработчика по умолчанию для типа файлов или схемы URI, это больше не работает.</span><span class="sxs-lookup"><span data-stu-id="2e618-116">However, because apps can no longer programmatically set themselves as the default handler for a file type or URI scheme, this no longer works.</span></span>

## <a name="mitigation"></a><span data-ttu-id="2e618-117">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="2e618-117">Mitigation</span></span>

<span data-ttu-id="2e618-118">Существует несколько вещей, которые могут сделать пользователи для удовлетворения этих изменений:</span><span class="sxs-lookup"><span data-stu-id="2e618-118">There are several things users can do to accommodate these changes:</span></span>

-   <span data-ttu-id="2e618-119">Пользователям предлагается контекстно выбрать приложение по умолчанию для работы с типами файлов, схемами URI или обоими, если они не указаны.</span><span class="sxs-lookup"><span data-stu-id="2e618-119">Users are prompted contextually to choose a default app to handle file types, URI schemes, or both when one has not been specified</span></span>
-   <span data-ttu-id="2e618-120">Пользователям предлагается изменить свой обработчик по умолчанию после установки новых приложений, которые могут работать с типом файлов или схемой URI.</span><span class="sxs-lookup"><span data-stu-id="2e618-120">Users are offered the option to change their default handler after installing new apps that can handle a file type or URI scheme</span></span>
-   <span data-ttu-id="2e618-121">Панель управления программы по умолчанию позволяет пользователям задавать значения по умолчанию для приложения или для типа файла, схемы URI или и того, и другого. приложения могут ссылаться на панель управления</span><span class="sxs-lookup"><span data-stu-id="2e618-121">The default programs control panel allows users to set defaults for an app, or for a file type, URI scheme, or both; apps can link to the control panel</span></span>
-   <span data-ttu-id="2e618-122">Значения по умолчанию можно изменить в проводнике Windows</span><span class="sxs-lookup"><span data-stu-id="2e618-122">Defaults can be changed from Windows Explorer</span></span>

## <a name="solution"></a><span data-ttu-id="2e618-123">Решение</span><span class="sxs-lookup"><span data-stu-id="2e618-123">Solution</span></span>

<span data-ttu-id="2e618-124">В результате этих изменений предоставляется следующее руководство по API:</span><span class="sxs-lookup"><span data-stu-id="2e618-124">As a result of these changes, this API guidance is provided:</span></span>

-   <span data-ttu-id="2e618-125">Функции некоторых вызовов методов в API [иаппликатионассоЦиатионрегистратион](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) были изменены и больше не должны использоваться.</span><span class="sxs-lookup"><span data-stu-id="2e618-125">The functionality of some method calls within the [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) API has changed, and should no longer be used.</span></span>

    -   <span data-ttu-id="2e618-126">**Не** вызывайте [куеряпписдефаулт](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [куеряпписдефаулталл](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) , чтобы определить, является ли приложение значением по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2e618-126">**Do not** call [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault)/[QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) to determine if an app is the default</span></span>
    -   <span data-ttu-id="2e618-127">**Не** вызывайте [куерикуррентдефаулт](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) , чтобы определить, какое приложение (если таковое имеется) является текущим значением по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2e618-127">**Do not** call [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) to determine which app (if any) is the current default</span></span>
    -   <span data-ttu-id="2e618-128">**Не** вызывайте [сетапписдефаулт](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [сетапписдефаулталл](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) , чтобы задать приложение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2e618-128">**Do not** call [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault)/[SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) to set the default app</span></span>

-   <span data-ttu-id="2e618-129">Ниже приведены рекомендации по пересылке:</span><span class="sxs-lookup"><span data-stu-id="2e618-129">The guidance going forward is:</span></span>

    -   <span data-ttu-id="2e618-130">**Не** запрашивать сведения о том, какое приложение является обработчиком по умолчанию для типов файлов или схем URI</span><span class="sxs-lookup"><span data-stu-id="2e618-130">**Do not** query to see which app is the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="2e618-131">**Не** пытайтесь отслеживать изменения в обработчике по умолчанию для типов файлов или схем URI.</span><span class="sxs-lookup"><span data-stu-id="2e618-131">**Do not** attempt to monitor changes in the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="2e618-132">**Не** пытайтесь задать приложение в качестве обработчика по умолчанию для типов файлов или схем URI.</span><span class="sxs-lookup"><span data-stu-id="2e618-132">**Do not** attempt to set an app as the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="2e618-133">**Не** пытайтесь управлять параметрами по умолчанию для типов файлов или схем URI из приложения.</span><span class="sxs-lookup"><span data-stu-id="2e618-133">**Do not** attempt to manage defaults for file types or URI schemes from within an app</span></span>

    -   <span data-ttu-id="2e618-134">**Интегрируйтесь** с панелью управления [Настройка программ по умолчанию](../shell/default-programs.md) , если хотите разрешить пользователям приложения доступ к пользовательскому интерфейсу управления по умолчанию (пользовательский интерфейс управления в приложении больше не поддерживается).</span><span class="sxs-lookup"><span data-stu-id="2e618-134">**Do** integrate with the [Set Default Programs](../shell/default-programs.md) control panel if you want to allow users of your app to access the default management UI (the management UI within the app is no longer supported)</span></span>

        -   <span data-ttu-id="2e618-135">Вызов [иаппликатионассоЦиатионрегистратионуи:: лаунчадванцедассоЦиатионуи](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) позволяет пользователю получить доступ к странице панели управления "[Установка программ по умолчанию](../shell/default-programs.md)" для указанного приложения</span><span class="sxs-lookup"><span data-stu-id="2e618-135">Calling [IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) allows the user to access the ‘[Set Default Programs](../shell/default-programs.md)’ control panel page for the specified app</span></span>

## <a name="tests"></a><span data-ttu-id="2e618-136">Тесты</span><span class="sxs-lookup"><span data-stu-id="2e618-136">Tests</span></span>

-   <span data-ttu-id="2e618-137">Проверка проверки правильности регистрации приложений в панели управления "Настройка программ по умолчанию"</span><span class="sxs-lookup"><span data-stu-id="2e618-137">Test to verify that apps register properly in Set Default Programs control panel</span></span>
-   <span data-ttu-id="2e618-138">Проверка правильности регистрации приложений для отображения в списке Опенвис для типов файлов, схем URI или и того и другого, которые регистрируются для работы</span><span class="sxs-lookup"><span data-stu-id="2e618-138">Test to verify that apps register properly to appear in the OpenWith list for the file types, URI schemes, or both, that they register to handle</span></span>
-   <span data-ttu-id="2e618-139">Проверьте, появились ли новые уведомления о приложениях после установки приложения и пользователь вызывает тип файла, схему URI или и то, и другое, что приложение зарегистрировалось для работы.</span><span class="sxs-lookup"><span data-stu-id="2e618-139">Test to verify that new app notifications appear after your app is installed and the user invokes a file type, URI scheme, or both, that your app has registered to handle</span></span>

## <a name="resources"></a><span data-ttu-id="2e618-140">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="2e618-140">Resources</span></span>

-   <span data-ttu-id="2e618-141">[Рекомендации по типу файлов и сопоставлению URI в классических приложениях Windows 8](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2e618-141">[Best Practices for File Type and URI Associations in Windows 8 Desktop Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span></span>
-   [<span data-ttu-id="2e618-142">Сопоставление типов файлов и автовоспроизведение создание конференций презентация</span><span class="sxs-lookup"><span data-stu-id="2e618-142">File Type Associations and AutoPlay Build Conference Presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 