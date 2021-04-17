---
title: службы удаленных рабочих столов рекомендации по программированию
description: Разделы, содержащие рекомендации по разработке приложений в среде службы удаленных рабочих столов.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Службы удаленных рабочих столов службы удаленных рабочих столов, рекомендации по программированию
- рекомендации по программированию службы удаленных рабочих столов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672310"
---
# <a name="remote-desktop-services-programming-guidelines"></a><span data-ttu-id="68819-105">службы удаленных рабочих столов рекомендации по программированию</span><span class="sxs-lookup"><span data-stu-id="68819-105">Remote Desktop Services programming guidelines</span></span>

<span data-ttu-id="68819-106">Большинство существующих 32-разрядных или 64-разрядных приложений Windows выполняются "как есть" в службы удаленных рабочих столов (прежнее название — службы терминалов).</span><span class="sxs-lookup"><span data-stu-id="68819-106">Most existing 32-bit or 64-bit Windows-based applications run "as is" in a Remote Desktop Services (formerly known as Terminal Services) environment.</span></span> <span data-ttu-id="68819-107">Однако некоторые приложения работают правильно и хорошо работают в среде службы удаленных рабочих столов, а другие — нет.</span><span class="sxs-lookup"><span data-stu-id="68819-107">However, some applications function correctly and perform well in a Remote Desktop Services environment, while others do not.</span></span> <span data-ttu-id="68819-108">В следующих разделах приводятся рекомендации по разработке приложений в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="68819-108">The following topics provide guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="68819-109">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="68819-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="68819-110">Рекомендации для нескольких пользователей</span><span class="sxs-lookup"><span data-stu-id="68819-110">Multiple-user guidelines</span></span>](multiple-user-guidelines.md)
</dt> <dd>

<span data-ttu-id="68819-111">Рекомендации по разработке приложений для нескольких пользователей в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="68819-111">Guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="68819-112">Рекомендации по производительности</span><span class="sxs-lookup"><span data-stu-id="68819-112">Performance guidelines</span></span>](performance-guidelines.md)
</dt> <dd>

<span data-ttu-id="68819-113">Рекомендации по разработке приложений, которые хорошо работают в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="68819-113">Guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="68819-114">Общие рекомендации по программированию</span><span class="sxs-lookup"><span data-stu-id="68819-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> <dd>

<span data-ttu-id="68819-115">Рекомендации по разработке приложений в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="68819-115">Guidelines for developing applications in a Remote Desktop Services environment.</span></span>

</dd> </dl>

<span data-ttu-id="68819-116">Многие из этих рекомендаций являются хорошими приемами программирования, которые могут принести пользу приложений, работающих в любой среде Windows.</span><span class="sxs-lookup"><span data-stu-id="68819-116">Many of these guidelines are good programming practices that will benefit applications running in any Windows environment.</span></span> <span data-ttu-id="68819-117">Однако некоторые рекомендованные оптимизации, такие как ограничение графических эффектов, являются оптимизацией, которые нужны только при выполнении приложения с службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="68819-117">However, some recommended optimizations, such as limiting graphic effects, are optimizations that you would want only when your application is running under Remote Desktop Services.</span></span> <span data-ttu-id="68819-118">Пример кода, демонстрирующий обнаружение среды службы удаленных рабочих столов, см. в разделе [Обнаружение среды службы удаленных рабочих столов](detecting-the-terminal-services-environment.md).</span><span class="sxs-lookup"><span data-stu-id="68819-118">For a code example that shows how to detect a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="68819-119">См. также</span><span class="sxs-lookup"><span data-stu-id="68819-119">Related topics</span></span>

<dl> <span data-ttu-id="68819-120"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="68819-120"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="68819-121">Службы терминалов теперь службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="68819-121">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="68819-122">Формат файла административного шаблона</span><span class="sxs-lookup"><span data-stu-id="68819-122">Administrative Template File Format</span></span>](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[<span data-ttu-id="68819-123">Безопасность раздела реестра и права доступа</span><span class="sxs-lookup"><span data-stu-id="68819-123">Registry Key Security and Access Rights</span></span>](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[<span data-ttu-id="68819-124">Кусты реестра</span><span class="sxs-lookup"><span data-stu-id="68819-124">Registry Hives</span></span>](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[<span data-ttu-id="68819-125">Дескрипторы безопасности</span><span class="sxs-lookup"><span data-stu-id="68819-125">Security Descriptors</span></span>](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[<span data-ttu-id="68819-126">Стандартные права доступа</span><span class="sxs-lookup"><span data-stu-id="68819-126">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="68819-127">Модель контроля доступа</span><span class="sxs-lookup"><span data-stu-id="68819-127">Access Control Model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 