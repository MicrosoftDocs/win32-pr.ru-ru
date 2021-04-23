---
title: Руководство обзор ADSI с Visual Basic
description: Active Directory является базой данных специального назначения \ 8212; Это не замена реестра.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104557430"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a><span data-ttu-id="45325-103">Обзор учебника: ADSI с Visual Basic</span><span class="sxs-lookup"><span data-stu-id="45325-103">Tutorial Overview: ADSI with Visual Basic</span></span>

> [!Note]  
> <span data-ttu-id="45325-104">Следующая документация является частью описания расширенного сценария для Visual Basic разработчиков.</span><span class="sxs-lookup"><span data-stu-id="45325-104">The following documentation is part of an extended scenario description for Visual Basic developers.</span></span> <span data-ttu-id="45325-105">Общие сведения о Active Directory см. в документации по [ИТ-специалистам на сайте TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="45325-105">If you are looking for a general overview of Active Directory, see the [IT Pro docs on Technet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span></span> <span data-ttu-id="45325-106">Более подробные сведения о разработке Active Directory см. в разделе [домен Active Directory Services](/windows/desktop/AD/active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="45325-106">For a more in-depth look at the development side of Active Directory, see [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span></span> <span data-ttu-id="45325-107">Дополнительные сведения об интерфейсах служб Active Directory см. в разделе "родительский раздел" этой статьи: [интерфейсы служб Active Directory](active-directory-service-interfaces-adsi.md), а также родственный раздел: [о Active Directory интерфейсах службы](about-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="45325-107">For a larger introduction to Active Directory Service Interfaces, see this topic's parent topic: [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md), as well as the sibling topic: [About Active Directory Service Interfaces](about-adsi.md).</span></span>

 

<span data-ttu-id="45325-108">Active Directory является базой данных специального назначения — это не замена реестра.</span><span class="sxs-lookup"><span data-stu-id="45325-108">Active Directory is a special-purpose database — it is not a registry replacement.</span></span> <span data-ttu-id="45325-109">Каталог предназначен для выполнения большого количества операций чтения и поиска и значительно меньшего количества изменений и обновлений.</span><span class="sxs-lookup"><span data-stu-id="45325-109">The directory is designed to handle a large number of read and search operations and a significantly smaller number of changes and updates.</span></span> <span data-ttu-id="45325-110">Active Directory данные являются иерархическими, реплицируемыми и расширяемыми.</span><span class="sxs-lookup"><span data-stu-id="45325-110">Active Directory data is hierarchical, replicated, and extensible.</span></span> <span data-ttu-id="45325-111">Так как он реплицируется, вы не хотите хранить динамические данные, например стоимость корпоративных акций или производительность ЦП.</span><span class="sxs-lookup"><span data-stu-id="45325-111">Because it is replicated, you do not want to store dynamic data, such as corporate stock prices or CPU performance.</span></span> <span data-ttu-id="45325-112">Если данные зависят от компьютера, храните их в реестре.</span><span class="sxs-lookup"><span data-stu-id="45325-112">If your data is machine-specific, store the data in the registry.</span></span> <span data-ttu-id="45325-113">Типичными примерами данных, хранящихся в каталоге, являются данные очереди печати, контактные данные пользователя и данные конфигурации сети или компьютера.</span><span class="sxs-lookup"><span data-stu-id="45325-113">Typical examples of data stored in the directory include printer queue data, user contact data, and network/computer configuration data.</span></span> <span data-ttu-id="45325-114">База данных Active Directory состоит из объектов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="45325-114">The Active Directory database consists of objects and attributes.</span></span> <span data-ttu-id="45325-115">Определения объектов и атрибутов хранятся в схеме Active Directory.</span><span class="sxs-lookup"><span data-stu-id="45325-115">Objects and attribute definitions are stored in the Active Directory schema.</span></span>

<span data-ttu-id="45325-116">Возможно, вас интересует, какие объекты в данный момент хранятся в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="45325-116">You may be wondering what objects are currently stored in Active Directory.</span></span> <span data-ttu-id="45325-117">Active Directory содержит три секции.</span><span class="sxs-lookup"><span data-stu-id="45325-117">Active Directory has three partitions.</span></span> <span data-ttu-id="45325-118">Они также называются контекстами именования: домен, схема и конфигурация.</span><span class="sxs-lookup"><span data-stu-id="45325-118">These are also known as naming contexts: domain, schema, and configuration.</span></span> <span data-ttu-id="45325-119">Раздел домена содержит пользователей, группы, контакты, компьютеры, подразделения и многие другие типы объектов.</span><span class="sxs-lookup"><span data-stu-id="45325-119">The domain partition contains users, groups, contacts, computers, organizational units, and many other object types.</span></span> <span data-ttu-id="45325-120">Поскольку Active Directory является расширяемой, можно также добавить собственные классы и атрибуты.</span><span class="sxs-lookup"><span data-stu-id="45325-120">Because Active Directory is extensible, you can also add your own classes and/or attributes.</span></span> <span data-ttu-id="45325-121">Секция схемы содержит классы и определения атрибутов.</span><span class="sxs-lookup"><span data-stu-id="45325-121">The schema partition contains classes and attribute definitions.</span></span> <span data-ttu-id="45325-122">Раздел конфигурации включает данные конфигурации для служб, секций и сайтов.</span><span class="sxs-lookup"><span data-stu-id="45325-122">The configuration partition includes configuration data for services, partitions, and sites.</span></span>

<span data-ttu-id="45325-123">На следующем снимке экрана показан Active Directory раздел домена.</span><span class="sxs-lookup"><span data-stu-id="45325-123">The following screen shot shows the Active Directory domain partition.</span></span>

![раздел домена Active Directory](images/adadsi1.png)

## <a name="related-topics"></a><span data-ttu-id="45325-125">См. также</span><span class="sxs-lookup"><span data-stu-id="45325-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45325-126">Доступ к Active Directory с помощью Visual Basic</span><span class="sxs-lookup"><span data-stu-id="45325-126">Accessing Active Directory Using Visual Basic</span></span>](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[<span data-ttu-id="45325-127">Сценарий: Корпорация Fabrikam</span><span class="sxs-lookup"><span data-stu-id="45325-127">Scenario: The Fabrikam Corporation</span></span>](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[<span data-ttu-id="45325-128">Дополнительные разделы</span><span class="sxs-lookup"><span data-stu-id="45325-128">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 