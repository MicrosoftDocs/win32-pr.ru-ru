---
title: Сведения об элементах управления SysLink
description: Элемент управления SysLink — это окно, которое отображает помеченный текст и уведомляет приложение, когда пользователи щелкают внедренные гиперссылки. Этот элемент управления предоставляет удобную альтернативу использованию кнопки ссылка на команду. Дополнительные сведения см. в разделе Типы кнопок.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070685"
---
# <a name="about-syslink-controls"></a><span data-ttu-id="3fa93-105">Сведения об элементах управления SysLink</span><span class="sxs-lookup"><span data-stu-id="3fa93-105">About SysLink Controls</span></span>

<span data-ttu-id="3fa93-106">Элемент управления SysLink — это окно, которое отображает помеченный текст и уведомляет приложение, когда пользователи щелкают внедренные гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="3fa93-106">A SysLink control is a window that renders marked-up text, and notifies the application when users click its embedded hyperlinks.</span></span> <span data-ttu-id="3fa93-107">Этот элемент управления предоставляет удобную альтернативу использованию [**кнопки ссылка на команду**](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="3fa93-107">This control provides a convenient alternative to using the [**Command link button**](button-styles.md).</span></span> <span data-ttu-id="3fa93-108">Дополнительные сведения см. в разделе [типы кнопок](button-types-and-styles.md).</span><span class="sxs-lookup"><span data-stu-id="3fa93-108">For more information, see [Button Types](button-types-and-styles.md).</span></span>

<span data-ttu-id="3fa93-109">Каждый элемент управления SysLink может поддерживать несколько гиперссылок, и вы можете получить доступ к каждой гиперссылке с помощью индекса, начинающегося с нуля.</span><span class="sxs-lookup"><span data-stu-id="3fa93-109">Each SysLink control can support multiple hyperlinks, and you can access each hyperlink through a zero-based index.</span></span> <span data-ttu-id="3fa93-110">Элемент управления SysLink определен в ComCtl32.dll версии 6, и для него требуется манифест или директива, указывающая, что следует использовать версию 6 библиотеки DLL, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="3fa93-110">The SysLink control is defined in the ComCtl32.dll version 6, and it requires a manifest or directive that specifies that version 6 of the DLL should be used if it is available.</span></span> <span data-ttu-id="3fa93-111">Дополнительные сведения см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3fa93-111">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

<span data-ttu-id="3fa93-112">Эта статья состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="3fa93-112">This article contains the following sections.</span></span>

-   [<span data-ttu-id="3fa93-113">Разметка SysLink</span><span class="sxs-lookup"><span data-stu-id="3fa93-113">SysLink Markup</span></span>](#syslink-markup)
-   [<span data-ttu-id="3fa93-114">Атрибуты ссылки</span><span class="sxs-lookup"><span data-stu-id="3fa93-114">Link Attributes</span></span>](#link-attributes)
-   [<span data-ttu-id="3fa93-115">Состояния связей</span><span class="sxs-lookup"><span data-stu-id="3fa93-115">Link States</span></span>](#link-states)
-   [<span data-ttu-id="3fa93-116">Ограничения на отображение двунаправленного текста</span><span class="sxs-lookup"><span data-stu-id="3fa93-116">Limitations on Bidirectional Text Display</span></span>](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a><span data-ttu-id="3fa93-117">Разметка SysLink</span><span class="sxs-lookup"><span data-stu-id="3fa93-117">SysLink Markup</span></span>

<span data-ttu-id="3fa93-118">Элемент управления SysLink поддерживает тег привязки ( &lt; a &gt; ) вместе с атрибутами **href** и **ID**.</span><span class="sxs-lookup"><span data-stu-id="3fa93-118">The SysLink control supports the anchor tag(&lt;a&gt;) along with the attributes **HREF** and **ID**.</span></span> <span data-ttu-id="3fa93-119">**Href** может быть любым протоколом, таким как HTTP, FTP и mailto.</span><span class="sxs-lookup"><span data-stu-id="3fa93-119">An **HREF** can be any protocol, such as http, ftp, and mailto.</span></span> <span data-ttu-id="3fa93-120">**Идентификатор** — это необязательное имя, уникальное в пределах элемента управления Syslink и связанное с отдельным каналом.</span><span class="sxs-lookup"><span data-stu-id="3fa93-120">An **ID** is an optional name, unique within a SysLink control, and it is associated with an individual link.</span></span> <span data-ttu-id="3fa93-121">Ссылкам также назначается Отсчитываемый от нуля индекс в соответствии с их позицией в строке.</span><span class="sxs-lookup"><span data-stu-id="3fa93-121">Links are also assigned a zero-based index according to their position within the string.</span></span> <span data-ttu-id="3fa93-122">Этот индекс используется для доступа к ссылке.</span><span class="sxs-lookup"><span data-stu-id="3fa93-122">This index is used to access a link.</span></span>

## <a name="link-attributes"></a><span data-ttu-id="3fa93-123">Атрибуты ссылки</span><span class="sxs-lookup"><span data-stu-id="3fa93-123">Link Attributes</span></span>

<span data-ttu-id="3fa93-124">Атрибуты каждой ссылки можно задать либо в теге привязки для каждой ссылки, либо путем отправки сообщения [**LM \_ сетитем**](lm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa93-124">Each link's attributes can be set either within the anchor tag for each link or by sending the [**LM\_SETITEM**](lm-setitem.md) message.</span></span> <span data-ttu-id="3fa93-125">Задание атрибута путем его указания в строке инициализации просто инициализирует значение.</span><span class="sxs-lookup"><span data-stu-id="3fa93-125">Setting an attribute by specifying it within the initialization string merely initializes the value.</span></span> <span data-ttu-id="3fa93-126">Вы можете изменить значение атрибута, используя последующее использование сообщения **LM \_ сетитем** .</span><span class="sxs-lookup"><span data-stu-id="3fa93-126">You can change the value of an attribute through subsequent use of the **LM\_SETITEM** message.</span></span>

## <a name="link-states"></a><span data-ttu-id="3fa93-127">Состояния связей</span><span class="sxs-lookup"><span data-stu-id="3fa93-127">Link States</span></span>

<span data-ttu-id="3fa93-128">Элементы Link могут находиться в одном из трех состояний, представленных флагами, приведенными в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="3fa93-128">Link items can be in any one of three states, represented by the flags in the following table.</span></span>



| <span data-ttu-id="3fa93-129">Флаг состояния</span><span class="sxs-lookup"><span data-stu-id="3fa93-129">State flag</span></span>   | <span data-ttu-id="3fa93-130">Внешний вид и значение</span><span class="sxs-lookup"><span data-stu-id="3fa93-130">Appearance and meaning</span></span>                                            |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="3fa93-131">LIS \_</span><span class="sxs-lookup"><span data-stu-id="3fa93-131">LIS\_FOCUSED</span></span> | <span data-ttu-id="3fa93-132">Ссылка имеет фокус клавиатуры и нажатие клавиши Ввод активирует ее.</span><span class="sxs-lookup"><span data-stu-id="3fa93-132">The link has the keyboard focus, and pressing Enter activates it.</span></span> |
| <span data-ttu-id="3fa93-133">LIS \_ включен</span><span class="sxs-lookup"><span data-stu-id="3fa93-133">LIS\_ENABLED</span></span> | <span data-ttu-id="3fa93-134">Ссылка включена.</span><span class="sxs-lookup"><span data-stu-id="3fa93-134">The link is enabled.</span></span>                                              |
| <span data-ttu-id="3fa93-135">\_Посещенные LIS</span><span class="sxs-lookup"><span data-stu-id="3fa93-135">LIS\_VISITED</span></span> | <span data-ttu-id="3fa93-136">Пользователь уже посетит URL-адрес, представленный ссылкой.</span><span class="sxs-lookup"><span data-stu-id="3fa93-136">The user has already visited the URL represented by the link.</span></span>     |



 

## <a name="limitations-on-bidirectional-text-display"></a><span data-ttu-id="3fa93-137">Ограничения на отображение двунаправленного текста</span><span class="sxs-lookup"><span data-stu-id="3fa93-137">Limitations on Bidirectional Text Display</span></span>

<span data-ttu-id="3fa93-138">Некоторые языки, такие как арабский или иврит, записываются справа налево (RTL). Английский написано слева направо (LTR).</span><span class="sxs-lookup"><span data-stu-id="3fa93-138">Some languages, such as Arabic or Hebrew, are written right-to-left (RTL); English is written left-to-right (LTR).</span></span> <span data-ttu-id="3fa93-139">Сочетание RTL с LTR называется двунаправленным текстом.</span><span class="sxs-lookup"><span data-stu-id="3fa93-139">Combining RTL with LTR is called bidirectional text.</span></span> <span data-ttu-id="3fa93-140">Смешивание конструкций разметки LTR и RTL в Юникоде или HTML в строках ресурсов в качестве маркеров двунаправленного потока для управления потоком строк, может не давать ожидаемый результат при использовании элемента управления SysLink.</span><span class="sxs-lookup"><span data-stu-id="3fa93-140">Mixing LTR and RTL Unicode or HTML directional markup constructs in resource strings, as bidirectional flow markers to control the flow of strings, may not produce the expected result when using a SysLink control.</span></span> <span data-ttu-id="3fa93-141">Например, предложение, помеченное как LTR, может отображаться неправильно в контексте RTL.</span><span class="sxs-lookup"><span data-stu-id="3fa93-141">For instance, an LTR-marked sentence may not display correctly in RTL context.</span></span>

> [!Note]  
> <span data-ttu-id="3fa93-142">Элементы управления SysLink не поддерживают двунаправленное отображение во всех сценариях.</span><span class="sxs-lookup"><span data-stu-id="3fa93-142">SysLink controls do not support bidirectional display under all scenarios.</span></span> <span data-ttu-id="3fa93-143">Используйте элемент управления SysLink только в том случае, если известно, что у вас достаточно простой макет LTR или RTL.</span><span class="sxs-lookup"><span data-stu-id="3fa93-143">Use a SysLink control only if you know that a simple LTR or RTL layout is adequate.</span></span> <span data-ttu-id="3fa93-144">В противном случае рассмотрите возможность использования более сложных технологий, таких как [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3fa93-144">Otherwise, consider using a more advanced technology such as [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span></span>

 

 

 