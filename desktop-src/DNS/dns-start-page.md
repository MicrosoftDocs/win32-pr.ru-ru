---
title: Система доменных имен
description: Система доменных имен (DNS), служба локатора в Microsoft Windows, является стандартным промышленным протоколом, который находит компьютеры в сети на основе IP-адресов.
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- DNS (см. раздел Система доменных имен)
- Система доменных имен
- Система доменных имен, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104081834"
---
# <a name="domain-name-system"></a><span data-ttu-id="e4c03-107">Система доменных имен</span><span class="sxs-lookup"><span data-stu-id="e4c03-107">Domain Name System</span></span>

## <a name="purpose"></a><span data-ttu-id="e4c03-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="e4c03-108">Purpose</span></span>

<span data-ttu-id="e4c03-109">Система доменных имен (DNS), служба локатора в Microsoft Windows, является стандартным промышленным протоколом, который находит компьютеры в сети на основе IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="e4c03-109">Domain Name System (DNS), a locator service in Microsoft Windows, is an industry-standard protocol that locates computers on an IP-based network.</span></span> <span data-ttu-id="e4c03-110">IP-сети, такие как сети Интернет и Windows, используют адреса на основе чисел для обработки данных.</span><span class="sxs-lookup"><span data-stu-id="e4c03-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to process data.</span></span> <span data-ttu-id="e4c03-111">Однако пользователи могут легко запомнить адреса имен, поэтому необходимо преобразовать понятные имена пользователей (например, `www.microsoft.com` ) в адреса, распознаваемые сетью (например, 207.46.131.137).</span><span class="sxs-lookup"><span data-stu-id="e4c03-111">Users however, can more easily remember name addresses, so it is necessary to translate user-friendly names (such as `www.microsoft.com`) into addresses that the network can recognize (such as 207.46.131.137).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e4c03-112">Где применимо</span><span class="sxs-lookup"><span data-stu-id="e4c03-112">Where applicable</span></span>

<span data-ttu-id="e4c03-113">Windows и Active Directory используют DNS.</span><span class="sxs-lookup"><span data-stu-id="e4c03-113">Windows and Active Directory use DNS.</span></span> <span data-ttu-id="e4c03-114">DNS — это основная служба локатора для Интернета и Active Directory, поэтому DNS считается базовой службой для Windows и Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e4c03-114">DNS is the primary locator service for the Internet and Active Directory, and therefore, DNS is considered a base service for Windows and Active Directory.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e4c03-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="e4c03-115">Developer audience</span></span>

<span data-ttu-id="e4c03-116">Windows предоставляет функции, позволяющие программистам приложений использовать DNS, такие как программный запрос DNS, Сравнение записей и поиск имен.</span><span class="sxs-lookup"><span data-stu-id="e4c03-116">Windows provides functions that enable application programmers to use DNS, such as programmatic DNS query, record compare, and name lookup.</span></span>

<span data-ttu-id="e4c03-117">Программируемые компоненты DNS предназначены для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="e4c03-117">Programmable DNS components are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="e4c03-118">Вам потребуются навыки работы с сетью и DNS.</span><span class="sxs-lookup"><span data-stu-id="e4c03-118">Familiarity with networking and DNS is required.</span></span> <span data-ttu-id="e4c03-119">Программисты должны быть знакомы с набором IP-протоколов, а также с протоколом DNS и операциями DNS.</span><span class="sxs-lookup"><span data-stu-id="e4c03-119">Programmers should be familiar with the IP-protocol suite, as well as the DNS protocol and DNS operations.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e4c03-120">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="e4c03-120">Run-time requirements</span></span>

<span data-ttu-id="e4c03-121">DNS используется во всех IP-сетях, для которых требуется служба локатора, совместимая с Интернетом.</span><span class="sxs-lookup"><span data-stu-id="e4c03-121">DNS is used on all IP networks that require an Internet-compatible locator service.</span></span> <span data-ttu-id="e4c03-122">Однако для API DNS требуется Windows 2000 или более поздняя версия.</span><span class="sxs-lookup"><span data-stu-id="e4c03-122">However, the DNS API requires Windows 2000 or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e4c03-123">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="e4c03-123">In this section</span></span>



| <span data-ttu-id="e4c03-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="e4c03-124">Topic</span></span>                                                             | <span data-ttu-id="e4c03-125">Описание</span><span class="sxs-lookup"><span data-stu-id="e4c03-125">Description</span></span>                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4c03-126">Документы по стандартам DNS</span><span class="sxs-lookup"><span data-stu-id="e4c03-126">DNS Standards Documents</span></span>](dns-standards-documents.md)<br/> | <span data-ttu-id="e4c03-127">Ссылки на общедоступные стандарты DNS.</span><span class="sxs-lookup"><span data-stu-id="e4c03-127">Links to public DNS standards documents.</span></span><br/>                                  |
| [<span data-ttu-id="e4c03-128">Сведения о DNS</span><span class="sxs-lookup"><span data-stu-id="e4c03-128">About DNS</span></span>](about-dns.md)<br/>                             | <span data-ttu-id="e4c03-129">Общие сведения о DNS.</span><span class="sxs-lookup"><span data-stu-id="e4c03-129">General information about DNS.</span></span><br/>                                            |
| [<span data-ttu-id="e4c03-130">Справочник по DNS</span><span class="sxs-lookup"><span data-stu-id="e4c03-130">DNS Reference</span></span>](dns-reference.md)<br/>                     | <span data-ttu-id="e4c03-131">Справочная документация по DNS.</span><span class="sxs-lookup"><span data-stu-id="e4c03-131">Reference documentation for DNS.</span></span><br/>                                          |
| [<span data-ttu-id="e4c03-132">Поставщик WMI для DNS</span><span class="sxs-lookup"><span data-stu-id="e4c03-132">DNS WMI Provider</span></span>](dns-wmi-provider.md)<br/>               | <span data-ttu-id="e4c03-133">Общие сведения и справочная документация по поставщику WMI для DNS.</span><span class="sxs-lookup"><span data-stu-id="e4c03-133">General information and reference documentation for the DNS WMI provider.</span></span><br/> |
| [<span data-ttu-id="e4c03-134">Словарь терминов</span><span class="sxs-lookup"><span data-stu-id="e4c03-134">Glossary</span></span>](glossary-gly.md)<br/>                           | <span data-ttu-id="e4c03-135">Глоссарий терминов и определений DNS.</span><span class="sxs-lookup"><span data-stu-id="e4c03-135">Glossary of DNS terms and definitions.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="e4c03-136">См. также</span><span class="sxs-lookup"><span data-stu-id="e4c03-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4c03-137">DHCP</span><span class="sxs-lookup"><span data-stu-id="e4c03-137">DHCP</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="e4c03-138">Вспомогательный метод протокола Интернета</span><span class="sxs-lookup"><span data-stu-id="e4c03-138">Internet Protocol Helper</span></span>](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

<span data-ttu-id="e4c03-139">[Служба каталогов](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e4c03-139">[Directory Services](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span></span>
</dt> </dl>

 

