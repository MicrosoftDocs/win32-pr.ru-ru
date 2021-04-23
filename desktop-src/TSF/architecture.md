---
title: Архитектура (платформа текстовых служб)
description: Архитектура
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Платформа текстовых служб (TSF), архитектура
- TSF (платформа текстовых служб), архитектура
- текстовые службы, архитектура
- Приложения, поддерживающие TSF, архитектура
- Платформа текстовых служб (TSF), компоненты
- TSF (платформа текстовых служб), компоненты
- текстовые службы, компоненты
- Приложения, поддерживающие TSF, компоненты
- Платформа текстовых служб (TSF), приложения
- TSF (платформа текстовых служб), приложения
- текстовые службы, приложения
- Приложения с поддержкой TSF, сведения
- Платформа текстовых служб (TSF), текстовые службы
- TSF (платформа текстовых служб), текстовые службы
- службы текстового ввода, сведения
- Приложения с поддержкой TSF, текстовые службы
- Платформа текстовых служб (TSF), диспетчер TSF
- TSF (платформа текстовых служб), диспетчер TSF
- текстовые службы, диспетчер TSF
- Приложения с поддержкой TSF, диспетчер TSF
- Диспетчер TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104550114"
---
# <a name="architecture-text-services-framework"></a><span data-ttu-id="c22e7-124">Архитектура (платформа текстовых служб)</span><span class="sxs-lookup"><span data-stu-id="c22e7-124">Architecture (Text Services Framework)</span></span>

<span data-ttu-id="c22e7-125">Платформа текстовых служб включает три основных компонента:</span><span class="sxs-lookup"><span data-stu-id="c22e7-125">Text Services Framework includes three primary components:</span></span>

-   <span data-ttu-id="c22e7-126">**Приложения:** Операции приложения обычно включают отображение, прямое редактирование и хранение текста.</span><span class="sxs-lookup"><span data-stu-id="c22e7-126">**Applications:** Application operations typically include display, direct editing, and storage of text.</span></span> <span data-ttu-id="c22e7-127">Приложение предоставляет доступ к тексту путем реализации COM-сервера, поддерживающего определенные интерфейсы, и взаимодействия с TSF с помощью интерфейсов, предоставляемых диспетчером TSF.</span><span class="sxs-lookup"><span data-stu-id="c22e7-127">An application provides access to text by implementing a COM server that supports certain interfaces and communicates with TSF using interfaces that the TSF manager exposes.</span></span> <span data-ttu-id="c22e7-128">В этой документации термин, приложение, ссылается на приложение с поддержкой TSF, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="c22e7-128">Throughout this documentation, the term, application, refers to a TSF-enabled application, unless otherwise specified.</span></span>
-   <span data-ttu-id="c22e7-129">**Текстовые службы:** Служба текстового ввода работает в качестве поставщика текста для приложения.</span><span class="sxs-lookup"><span data-stu-id="c22e7-129">**Text Services:** A text service functions as a text provider to an application.</span></span> <span data-ttu-id="c22e7-130">Служба текстового ввода может получать текст из приложения и записывать в него текст.</span><span class="sxs-lookup"><span data-stu-id="c22e7-130">A text service can obtain text from, and write text to, an application.</span></span> <span data-ttu-id="c22e7-131">Служба текстового ввода также может связывать данные и свойства с блоком текста.</span><span class="sxs-lookup"><span data-stu-id="c22e7-131">A text service can also associate data and properties with a block of text.</span></span> <span data-ttu-id="c22e7-132">Текстовая служба реализуется как внутрипроцессный сервер COM, который регистрируется в TSF.</span><span class="sxs-lookup"><span data-stu-id="c22e7-132">A text service is implemented as a COM in-proc server that registers itself with TSF.</span></span> <span data-ttu-id="c22e7-133">При регистрации пользователь взаимодействует с текстовой службой с помощью языковой панели или сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="c22e7-133">When registered, the user interacts with the text service using the language bar or keyboard shortcuts.</span></span> <span data-ttu-id="c22e7-134">Можно установить несколько служб текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="c22e7-134">Multiple text services can be installed.</span></span>
-   <span data-ttu-id="c22e7-135">**Диспетчер TSF:** Диспетчер TSF функционирует как медиатора между приложением и одной или несколькими текстовыми службами.</span><span class="sxs-lookup"><span data-stu-id="c22e7-135">**TSF Manager:** The TSF manager functions as a mediator between an application and one or more text services.</span></span> <span data-ttu-id="c22e7-136">Служба текстового ввода никогда не взаимодействует напрямую с приложением.</span><span class="sxs-lookup"><span data-stu-id="c22e7-136">A text service never interacts directly with an application.</span></span> <span data-ttu-id="c22e7-137">Все связи проходят через диспетчер TSF.</span><span class="sxs-lookup"><span data-stu-id="c22e7-137">All communication passes through the TSF manager.</span></span> <span data-ttu-id="c22e7-138">Диспетчер TSF реализуется операционной системой и не может быть заменен.</span><span class="sxs-lookup"><span data-stu-id="c22e7-138">The TSF manager is implemented by the operating system and cannot be replaced.</span></span> <span data-ttu-id="c22e7-139">В этой документации термин «руководитель» относится к диспетчеру TSF, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="c22e7-139">Throughout this documentation, the term, manager, refers to the TSF manager, unless otherwise specified.</span></span>

<span data-ttu-id="c22e7-140">На следующем рисунке показаны основные элементы архитектуры TSF.</span><span class="sxs-lookup"><span data-stu-id="c22e7-140">The following illustration shows the primary architectural elements of TSF.</span></span>

![Архитектура платформы текстовых служб](images/tsf-arch.gif)

<span data-ttu-id="c22e7-142">В этой архитектуре диспетчер TSF предоставляет уровень абстракции между приложениями и текстовыми службами.</span><span class="sxs-lookup"><span data-stu-id="c22e7-142">With this architecture, the TSF manager provides an abstraction layer between applications and text services.</span></span> <span data-ttu-id="c22e7-143">Этот слой абстракции позволяет приложению и одной или нескольким текстовым службам обмениваться текстом и позволяет диспетчеру TSF управлять текстовыми службами.</span><span class="sxs-lookup"><span data-stu-id="c22e7-143">This abstraction layer enables an application and one or more text services to share text, and it enables the TSF manager to manage text services.</span></span>

 

 




