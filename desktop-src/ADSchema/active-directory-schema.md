---
title: Схема Active Directory (схема AD)
description: Схема Microsoft Active Directory содержит формальные определения всех классов объектов, которые могут быть созданы в лесу Active Directory.
ms.assetid: b3da4519-d0c6-47eb-9455-ada653ad5c9e
ms.tgt_platform: multiple
keywords:
- Схема Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3393a6da1b8d1bd2c2418084c8f7fc657732
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105654307"
---
# <a name="active-directory-schema-ad-schema"></a><span data-ttu-id="f2c6c-104">Схема Active Directory (схема AD)</span><span class="sxs-lookup"><span data-stu-id="f2c6c-104">Active Directory Schema (AD Schema)</span></span>

<span data-ttu-id="f2c6c-105">Схема Microsoft Active Directory содержит формальные определения всех классов объектов, которые могут быть созданы в лесу Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-105">The Microsoft Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="f2c6c-106">Схема также содержит формальные определения всех атрибутов, которые могут существовать в объекте Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-106">The schema also contains formal definitions of every attribute that can exist in an Active Directory object.</span></span> <span data-ttu-id="f2c6c-107">В этом разделе содержится ссылка на каждый объект схемы и приводится краткое описание атрибутов, классов и других объектов, составляющих схему Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-107">This section provides the reference for each schema object and provides a brief explanation of the attributes, classes, and other objects that make up the Active Directory schema.</span></span>

> [!Note]  
> <span data-ttu-id="f2c6c-108">В следующей документации содержится справочник по программированию для схемы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-108">The following documentation contains the programming reference for Active Directory schema.</span></span> <span data-ttu-id="f2c6c-109">Если пользователь пытается выполнить отладку ошибки принтера, попробуйте выполнить поиск на [веб-сайте сообщества Майкрософт](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="f2c6c-109">If you are an end-user attempting to debug a printer error, try searching on the [Microsoft community site](https://answers.microsoft.com).</span></span> <span data-ttu-id="f2c6c-110">Если вы разработчик ищете общие сведения о Active Directory схеме, см. раздел Обзор [схемы Active Directory](/windows/desktop/AD/active-directory-schema) .</span><span class="sxs-lookup"><span data-stu-id="f2c6c-110">If you are a developer looking for a general overview of Active Directory schema, see the [Active Directory Schema](/windows/desktop/AD/active-directory-schema) overview topics.</span></span> <span data-ttu-id="f2c6c-111">Если вы ищете рекомендации по программированию для обновления или изменения схемы, дополнительные сведения о расширении и настройке схемы см. в разделах [расширение схемы](/windows/desktop/AD/extending-the-schema), а также многие статьи в руководствах по программированию [домен Active Directory Services](/windows/desktop/AD/active-directory-domain-services) и [службы Active Directory облегченного доступа к каталогам](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) .</span><span class="sxs-lookup"><span data-stu-id="f2c6c-111">If you are looking for programming guidelines for updating or modifying the schema, For more information about extending and customizing the schema, see [Extending the Schema](/windows/desktop/AD/extending-the-schema), as well as many of the topics in the [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) and [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) programming guides.</span></span>

 

<span data-ttu-id="f2c6c-112">В каждом из справочных разделов есть раздел для каждой операционной системы, к которой относится этот раздел.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-112">In each of the reference topics, there is a section for each operating system that the topic applies to.</span></span> <span data-ttu-id="f2c6c-113">В настоящее время поддерживаются следующие операционные системы.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-113">The following operating systems are currently supported.</span></span> 

| <span data-ttu-id="f2c6c-114">Платформа</span><span class="sxs-lookup"><span data-stu-id="f2c6c-114">Platform</span></span>                                                      | <span data-ttu-id="f2c6c-115">Имя в разделе</span><span class="sxs-lookup"><span data-stu-id="f2c6c-115">Name in topic</span></span>                               |
|---------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="f2c6c-116">Microsoft Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2c6c-116">Microsoft Windows Server 2003</span></span><br/>                      | <span data-ttu-id="f2c6c-117">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2c6c-117">Windows Server 2003</span></span><br/>              |
| <span data-ttu-id="f2c6c-118">Режим приложений Microsoft Active Directory (ADAM)</span><span class="sxs-lookup"><span data-stu-id="f2c6c-118">Microsoft Active Directory Application Mode (ADAM)</span></span><br/> | <span data-ttu-id="f2c6c-119">ADAM</span><span class="sxs-lookup"><span data-stu-id="f2c6c-119">ADAM</span></span><br/>                             |
| <span data-ttu-id="f2c6c-120">Microsoft Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f2c6c-120">Microsoft Windows Server 2003 R2</span></span><br/>                   | <span data-ttu-id="f2c6c-121">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f2c6c-121">Windows Server 2003 R2</span></span><br/>           |
| <span data-ttu-id="f2c6c-122">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2c6c-122">Microsoft Windows Server 2008</span></span><br/>                      | <span data-ttu-id="f2c6c-123">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2c6c-123">Microsoft Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="f2c6c-124">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2c6c-124">Microsoft Windows Server 2008 R2</span></span><br/>                   | <span data-ttu-id="f2c6c-125">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2c6c-125">Microsoft Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="f2c6c-126">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2c6c-126">Microsoft Windows Server 2012</span></span><br/>                      | <span data-ttu-id="f2c6c-127">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2c6c-127">Microsoft Windows Server 2012</span></span><br/>    |



 

<span data-ttu-id="f2c6c-128">Если операционная система не указана в разделе, этот раздел не поддерживается в этой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-128">If an operating system is not listed in the topic, the topic is not supported on that operating system.</span></span> <span data-ttu-id="f2c6c-129">Например, если в разделе перечислены только Windows Server 2003 и Адам, то раздел не относится к Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-129">For example, if a topic only lists Windows Server 2003 and ADAM, then the topic does not apply to Windows Server 2003 R2.</span></span>

<span data-ttu-id="f2c6c-130">В следующих разделах содержатся подробные сведения об элементах схемы Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-130">The following sections contain detailed information about the Active Directory schema elements.</span></span>

-   [<span data-ttu-id="f2c6c-131">Терминология схемы Active Directory</span><span class="sxs-lookup"><span data-stu-id="f2c6c-131">Active Directory Schema Terminology</span></span>](active-directory-schema-site.md)
-   [<span data-ttu-id="f2c6c-132">Классы</span><span class="sxs-lookup"><span data-stu-id="f2c6c-132">Classes</span></span>](classes.md)
-   [<span data-ttu-id="f2c6c-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f2c6c-133">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="f2c6c-134">Вариантов синтаксиса</span><span class="sxs-lookup"><span data-stu-id="f2c6c-134">Syntaxes</span></span>](syntaxes.md)
-   [<span data-ttu-id="f2c6c-135">Управление правами доступа</span><span class="sxs-lookup"><span data-stu-id="f2c6c-135">Control Access Rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="f2c6c-136">RootDSE</span><span class="sxs-lookup"><span data-stu-id="f2c6c-136">RootDSE</span></span>](rootdse.md)

 

