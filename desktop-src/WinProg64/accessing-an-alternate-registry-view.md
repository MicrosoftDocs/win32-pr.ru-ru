---
title: Доступ к альтернативному представлению реестра
description: По умолчанию 32-разрядное приложение, работающее на WOW64, получает доступ к 32-разрядному представлению реестра, а 64-разрядное приложение — к 64-разрядному представлению реестра.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- представления реестра, 64-разрядное программирование для Windows
- WOW64 64-разрядное программирование Windows, представления реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "105703410"
---
# <a name="accessing-an-alternate-registry-view"></a><span data-ttu-id="6e08c-105">Доступ к альтернативному представлению реестра</span><span class="sxs-lookup"><span data-stu-id="6e08c-105">Accessing an Alternate Registry View</span></span>

<span data-ttu-id="6e08c-106">По умолчанию 32-разрядное приложение, работающее на WOW64, получает доступ к 32-разрядному представлению реестра, а 64-разрядное приложение — к 64-разрядному представлению реестра.</span><span class="sxs-lookup"><span data-stu-id="6e08c-106">By default, a 32-bit application running on WOW64 accesses the 32-bit registry view and a 64-bit application accesses the 64-bit registry view.</span></span> <span data-ttu-id="6e08c-107">Следующие флаги позволяют 32-разрядным приложениям обращаться к перенаправленным ключам в представлении реестра 64-bit и 64-bit Applications для доступа к перенаправленным ключам в представлении реестра в режиме 32-bit.</span><span class="sxs-lookup"><span data-stu-id="6e08c-107">The following flags enable 32-bit applications to access redirected keys in the 64-bit registry view and 64-bit applications to access redirected keys in the 32-bit registry view.</span></span> <span data-ttu-id="6e08c-108">Эти флаги не влияют на общие разделы реестра.</span><span class="sxs-lookup"><span data-stu-id="6e08c-108">These flags have no effect on shared registry keys.</span></span> <span data-ttu-id="6e08c-109">Дополнительные сведения см. в разделе [разделы реестра, затрагиваемые WOW64](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="6e08c-109">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>



| <span data-ttu-id="6e08c-110">Имя флага</span><span class="sxs-lookup"><span data-stu-id="6e08c-110">Flag name</span></span>         | <span data-ttu-id="6e08c-111">Значение</span><span class="sxs-lookup"><span data-stu-id="6e08c-111">Value</span></span>  | <span data-ttu-id="6e08c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6e08c-112">Description</span></span>                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e08c-113">КЛЮЧ \_ WOW64 \_ 64KEY</span><span class="sxs-lookup"><span data-stu-id="6e08c-113">KEY\_WOW64\_64KEY</span></span> | <span data-ttu-id="6e08c-114">0x0100</span><span class="sxs-lookup"><span data-stu-id="6e08c-114">0x0100</span></span> | <span data-ttu-id="6e08c-115">Доступ к 64-разрядному ключу из 32-разрядного или 64-разрядного приложения.</span><span class="sxs-lookup"><span data-stu-id="6e08c-115">Access a 64-bit key from either a 32-bit or 64-bit application.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="6e08c-116">КЛЮЧ \_ WOW64 \_ 32KEY</span><span class="sxs-lookup"><span data-stu-id="6e08c-116">KEY\_WOW64\_32KEY</span></span> | <span data-ttu-id="6e08c-117">0x0200</span><span class="sxs-lookup"><span data-stu-id="6e08c-117">0x0200</span></span> | <span data-ttu-id="6e08c-118">Доступ к 32-разрядному ключу из 32-разрядного или 64-разрядного приложения.</span><span class="sxs-lookup"><span data-stu-id="6e08c-118">Access a 32-bit key from either a 32-bit or 64-bit application.</span></span><br/><span data-ttu-id="6e08c-119">**Windows 10 на ARM:** Это относится к 32-разрядному представлению реестра ARM для процессов с 32-разрядным процессором и с представлением реестра 32-bit x86 для 32-разрядных процессов ARM64 x86 и 64.</span><span class="sxs-lookup"><span data-stu-id="6e08c-119">**Windows 10 on ARM:** This refers to the 32-bit ARM registry view for 32-bit ARM processes and the 32-bit x86 registry view for 32-bit x86 and 64-bit ARM64 processes.</span></span> |



 

<span data-ttu-id="6e08c-120">Эти флаги можно указать в параметре *самдесиред* следующих функций реестра:</span><span class="sxs-lookup"><span data-stu-id="6e08c-120">These flags can be specified in the *samDesired* parameter of the following registry functions:</span></span>

-   [<span data-ttu-id="6e08c-121">**регкреатекэйекс**</span><span class="sxs-lookup"><span data-stu-id="6e08c-121">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="6e08c-122">**регделетекэйекс**</span><span class="sxs-lookup"><span data-stu-id="6e08c-122">**RegDeleteKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [<span data-ttu-id="6e08c-123">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="6e08c-123">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

<span data-ttu-id="6e08c-124">\_Можно указать либо ключ WOW64 \_ 32KEY, либо ключ \_ WOW64 \_ 64KEY.</span><span class="sxs-lookup"><span data-stu-id="6e08c-124">Either KEY\_WOW64\_32KEY or KEY\_WOW64\_64KEY can be specified.</span></span> <span data-ttu-id="6e08c-125">Если указаны оба флага, функция завершается ошибкой с \_ недопустимым \_ параметром.</span><span class="sxs-lookup"><span data-stu-id="6e08c-125">If both flags are specified, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="6e08c-126">Windows **server 2008, Windows Vista, Windows server 2003 и Windows XP:** Если указаны оба флага, поведение функции не определено.</span><span class="sxs-lookup"><span data-stu-id="6e08c-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** If both flags are specified, the function s behavior is undefined.</span></span>

<span data-ttu-id="6e08c-127">Функция [**регделетекэй**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) не может использоваться для доступа к альтернативному представлению реестра.</span><span class="sxs-lookup"><span data-stu-id="6e08c-127">The [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) function cannot be used to access an alternate registry view.</span></span>

<span data-ttu-id="6e08c-128">Ниже приведены рекомендации по доступу к реестру из приложения.</span><span class="sxs-lookup"><span data-stu-id="6e08c-128">The following are best practices when accessing the registry from an application:</span></span>

-   <span data-ttu-id="6e08c-129">После того как приложение попытается получить доступ к альтернативному представлению реестра с помощью одного из флагов, все последующие операции (создание, удаление или открытие) в дочерних разделах реестра должны явно использовать один и тот же флаг.</span><span class="sxs-lookup"><span data-stu-id="6e08c-129">After the application has accessed an alternate registry view using one of the flags, all subsequent operations (create, delete, or open) on child registry keys must explicitly use the same flag.</span></span> <span data-ttu-id="6e08c-130">В противном случае может воздержаться непредвиденное поведение.</span><span class="sxs-lookup"><span data-stu-id="6e08c-130">Otherwise, there can be unexpected behavior.</span></span>
-   <span data-ttu-id="6e08c-131">Чтобы точно перечислить все ключи в обоих представлениях, выполните перечисление в двух проходах.</span><span class="sxs-lookup"><span data-stu-id="6e08c-131">To accurately enumerate all keys in both views, perform the enumeration in two passes.</span></span> <span data-ttu-id="6e08c-132">Первый проход должен использовать открытый маркер с одним из флагов, а другой — маркер, Открытый с другим флагом.</span><span class="sxs-lookup"><span data-stu-id="6e08c-132">The first pass should use a handle opened with one of the flags, and the other pass should use a handle opened with the other flag.</span></span>

> [!Note]  
> <span data-ttu-id="6e08c-133">Ключи **WOW6432Node** и **WowAA32Node** зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="6e08c-133">The **Wow6432Node** and **WowAA32Node** keys are reserved.</span></span> <span data-ttu-id="6e08c-134">В целях совместимости приложения не должны использовать эти ключи напрямую.</span><span class="sxs-lookup"><span data-stu-id="6e08c-134">For compatibility, applications should not use these keys directly.</span></span>

 

<span data-ttu-id="6e08c-135">Сведения о доступе к альтернативному представлению реестра с помощью инструментария WMI см. в разделе [запрос данных WMI на 64-разрядной платформе](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span><span class="sxs-lookup"><span data-stu-id="6e08c-135">For information about accessing the alternate registry view through WMI, see [Requesting WMI Data on a 64-bit Platform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e08c-136">См. также</span><span class="sxs-lookup"><span data-stu-id="6e08c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e08c-137">Перенаправитель реестра</span><span class="sxs-lookup"><span data-stu-id="6e08c-137">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="6e08c-138">Отражение реестра</span><span class="sxs-lookup"><span data-stu-id="6e08c-138">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

