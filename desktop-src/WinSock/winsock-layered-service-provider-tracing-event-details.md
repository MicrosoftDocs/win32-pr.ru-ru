---
description: Сведения о трассировке изменений каталога Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Сведения о трассировке изменений каталога Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155250"
---
# <a name="winsock-catalog-change-tracing-details"></a><span data-ttu-id="6200c-103">Сведения о трассировке изменений каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="6200c-103">Winsock Catalog Change Tracing Details</span></span>

> [!Note]  
> <span data-ttu-id="6200c-104">Многоуровневые поставщики служб являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="6200c-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="6200c-105">Начиная с Windows 8 и Windows Server 2012, используйте [платформу фильтрации Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="6200c-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="6200c-106">Трассировка событий изменения каталога Winsock для многоуровневых поставщиков служб (LSP) связана с установкой LSP, удалением LSP, антивирусными ключами и операциями сброса каталога Winsock.</span><span class="sxs-lookup"><span data-stu-id="6200c-106">Winsock Catalog Change event tracing for layered Service providers (LSPs) is related to LSP installation, LSP removal, LSP disable, and Winsock catalog reset operations.</span></span> <span data-ttu-id="6200c-107">Все следующие события записываются в канал *Microsoft-Windows-Winsock-WS2HELP/* Operation, который отличается от трассировки событий сети Winsock, зарегистрированной в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="6200c-107">All of the following events are written to the *Microsoft-Windows-Winsock-WS2HELP/Operational* channel which is different from the other Winsock network event tracing logged on Windows Vista and later.</span></span>

<span data-ttu-id="6200c-108">Ниже приведены сведения о каждом из событий LSP Winsock, которые можно отслеживать, и описание параметров и сведений, регистрируемых в журнале.</span><span class="sxs-lookup"><span data-stu-id="6200c-108">The following details each of the Winsock LSP events that can be traced and describes which parameters and information are logged.</span></span>

## <a name="lsp-install"></a><span data-ttu-id="6200c-109">Установка LSP</span><span class="sxs-lookup"><span data-stu-id="6200c-109">LSP Install</span></span>

<span data-ttu-id="6200c-110">ИД события = 1</span><span class="sxs-lookup"><span data-stu-id="6200c-110">Event ID = 1</span></span>

<span data-ttu-id="6200c-111">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="6200c-111">Level = 4 (Information)</span></span>

<span data-ttu-id="6200c-112">Для операции установки LSP отслеживаются следующие события LSP Winsock:</span><span class="sxs-lookup"><span data-stu-id="6200c-112">The following Winsock LSP events are traced for an LSP install operation:</span></span>

-   <span data-ttu-id="6200c-113">Запись протокола устанавливается в каталог Winsock.</span><span class="sxs-lookup"><span data-stu-id="6200c-113">A protocol entry is installed into the Winsock catalog.</span></span>

<span data-ttu-id="6200c-114">Для события установки LSP регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="6200c-114">The following parameters are logged for a LSP install event:</span></span>



| <span data-ttu-id="6200c-115">Параметр</span><span class="sxs-lookup"><span data-stu-id="6200c-115">Parameter</span></span>                                                                                                | <span data-ttu-id="6200c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6200c-116">Description</span></span>                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6200c-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Имя LSP</span><span class="sxs-lookup"><span data-stu-id="6200c-117"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="6200c-118">Имя LSP, полученное из элемента **сзпротокол** структуры [**\_ сведений о ВСАПРОТОКОЛ**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для устанавливаемого LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-118">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/> |
| <span data-ttu-id="6200c-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Каталога</span><span class="sxs-lookup"><span data-stu-id="6200c-119"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="6200c-120">Каталог Winsock (32-разрядный или 64-bit), где устанавливается LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-120">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="6200c-121">Это целочисленное значение, равное 32 или 64.</span><span class="sxs-lookup"><span data-stu-id="6200c-121">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="6200c-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Необходимость</span><span class="sxs-lookup"><span data-stu-id="6200c-122"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="6200c-123">Имя файла модуля приложения, выполняющего вызов установки LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-123">The module filename of the application making the LSP install call.</span></span><br/>                                                                                          |
| <span data-ttu-id="6200c-124"><span id="GUID"></span><span id="guid"></span>УСТРОЙСТВА</span><span class="sxs-lookup"><span data-stu-id="6200c-124"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="6200c-125">Значение идентификатора GUID поставщика транспорта Winsock, в котором устанавливается LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-125">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span><br/>                                                                      |
| <span data-ttu-id="6200c-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Категори</span><span class="sxs-lookup"><span data-stu-id="6200c-126"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="6200c-127">Элемент **двкаталожентрид** структуры сведений о [**всапротокол \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для устанавливаемого LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-127">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span><br/>                                |



 

## <a name="lsp-uninstall"></a><span data-ttu-id="6200c-128">Удаление LSP</span><span class="sxs-lookup"><span data-stu-id="6200c-128">LSP Uninstall</span></span>

<span data-ttu-id="6200c-129">ИД события = 2</span><span class="sxs-lookup"><span data-stu-id="6200c-129">Event ID = 2</span></span>

<span data-ttu-id="6200c-130">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="6200c-130">Level = 4 (Information)</span></span>

<span data-ttu-id="6200c-131">Ниже перечислены события LSP Winsock, которые отслеживаются для операции удаления LSP:</span><span class="sxs-lookup"><span data-stu-id="6200c-131">The following Winsock LSP events are traced for an LSP uninstall operation:</span></span>

-   <span data-ttu-id="6200c-132">Запись протокола удаляется из каталога Winsock.</span><span class="sxs-lookup"><span data-stu-id="6200c-132">A protocol entry is removed from the Winsock catalog.</span></span>

<span data-ttu-id="6200c-133">Для события удаления LSP регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="6200c-133">The following parameters are logged for a LSP uninstall event:</span></span>



| <span data-ttu-id="6200c-134">Параметр</span><span class="sxs-lookup"><span data-stu-id="6200c-134">Parameter</span></span>                                                                                                | <span data-ttu-id="6200c-135">Описание</span><span class="sxs-lookup"><span data-stu-id="6200c-135">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6200c-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Имя LSP</span><span class="sxs-lookup"><span data-stu-id="6200c-136"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="6200c-137">Имя LSP, полученное из элемента **сзпротокол** структуры [**\_ сведений о ВСАПРОТОКОЛ**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для удаляемого LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-137">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/> |
| <span data-ttu-id="6200c-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Каталога</span><span class="sxs-lookup"><span data-stu-id="6200c-138"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="6200c-139">Каталог Winsock (32-разрядный или 64-бит), в который удаляется LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-139">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="6200c-140">Это целочисленное значение, равное 32 или 64.</span><span class="sxs-lookup"><span data-stu-id="6200c-140">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="6200c-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Необходимость</span><span class="sxs-lookup"><span data-stu-id="6200c-141"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="6200c-142">Имя файла модуля приложения, вызывающего удаление LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-142">The module filename of the application making the LSP remove call.</span></span><br/>                                                                                         |
| <span data-ttu-id="6200c-143"><span id="GUID"></span><span id="guid"></span>УСТРОЙСТВА</span><span class="sxs-lookup"><span data-stu-id="6200c-143"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="6200c-144">Значение идентификатора GUID поставщика транспорта Winsock, из которого удаляется LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-144">The GUID value of the Winsock transport provider that the LSP is removed from.</span></span><br/>                                                                             |
| <span data-ttu-id="6200c-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Категори</span><span class="sxs-lookup"><span data-stu-id="6200c-145"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="6200c-146">Элемент **двкаталожентрид** структуры сведений о [**всапротокол \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для удаляемого LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-146">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span><br/>                                |



 

## <a name="lsp-disable"></a><span data-ttu-id="6200c-147">Отключение LSP</span><span class="sxs-lookup"><span data-stu-id="6200c-147">LSP Disable</span></span>

<span data-ttu-id="6200c-148">ИД события = 3</span><span class="sxs-lookup"><span data-stu-id="6200c-148">Event ID = 3</span></span>

<span data-ttu-id="6200c-149">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="6200c-149">Level = 4 (Information)</span></span>

<span data-ttu-id="6200c-150">Следующие события LSP Winsock являются отслеживаемыми для операции отключения LSP:</span><span class="sxs-lookup"><span data-stu-id="6200c-150">The following Winsock LSP events are traced for an LSP disable operation:</span></span>

-   <span data-ttu-id="6200c-151">Запись протокола отключена в каталоге Winsock.</span><span class="sxs-lookup"><span data-stu-id="6200c-151">A protocol entry is disabled in the Winsock catalog.</span></span>

<span data-ttu-id="6200c-152">Для события отключения LSP регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="6200c-152">The following parameters are logged for a LSP disable event:</span></span>



| <span data-ttu-id="6200c-153">Параметр</span><span class="sxs-lookup"><span data-stu-id="6200c-153">Parameter</span></span>                                                                                                | <span data-ttu-id="6200c-154">Описание</span><span class="sxs-lookup"><span data-stu-id="6200c-154">Description</span></span>                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6200c-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Имя LSP</span><span class="sxs-lookup"><span data-stu-id="6200c-155"><span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>LSP Name</span></span><br/>     | <span data-ttu-id="6200c-156">Имя LSP, полученное из элемента **сзпротокол** структуры [**\_ сведений о всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для неактивного LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-156">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/> |
| <span data-ttu-id="6200c-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Каталога</span><span class="sxs-lookup"><span data-stu-id="6200c-157"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/>         | <span data-ttu-id="6200c-158">Каталог Winsock (32-разрядный или 64-бит), в котором отключается LSP.</span><span class="sxs-lookup"><span data-stu-id="6200c-158">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="6200c-159">Это целочисленное значение, равное 32 или 64.</span><span class="sxs-lookup"><span data-stu-id="6200c-159">This is an integer value that is either 32 or 64.</span></span><br/>                                   |
| <span data-ttu-id="6200c-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Необходимость</span><span class="sxs-lookup"><span data-stu-id="6200c-160"><span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Installer</span></span><br/> | <span data-ttu-id="6200c-161">Имя файла модуля приложения, которое делает вызов функции LSP отключить.</span><span class="sxs-lookup"><span data-stu-id="6200c-161">The module filename of the application making the LSP disable call.</span></span><br/>                                                                                         |
| <span data-ttu-id="6200c-162"><span id="GUID"></span><span id="guid"></span>УСТРОЙСТВА</span><span class="sxs-lookup"><span data-stu-id="6200c-162"><span id="GUID"></span><span id="guid"></span>GUID</span></span><br/>                                            | <span data-ttu-id="6200c-163">Значение идентификатора GUID поставщика транспорта Winsock, в котором отключена LSP-версия.</span><span class="sxs-lookup"><span data-stu-id="6200c-163">The GUID value of the Winsock transport provider where the LSP is being disabled.</span></span><br/>                                                                           |
| <span data-ttu-id="6200c-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Категори</span><span class="sxs-lookup"><span data-stu-id="6200c-164"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span><br/>     | <span data-ttu-id="6200c-165">Элемент **двкаталожентрид** структуры [**\_ сведений о всапротокол**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для LSP, который был отключен.</span><span class="sxs-lookup"><span data-stu-id="6200c-165">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span><br/>                                |



 

## <a name="winsock-catalog-reset"></a><span data-ttu-id="6200c-166">Сброс каталога Winsock</span><span class="sxs-lookup"><span data-stu-id="6200c-166">Winsock Catalog Reset</span></span>

<span data-ttu-id="6200c-167">ИД события = 4</span><span class="sxs-lookup"><span data-stu-id="6200c-167">Event ID = 4</span></span>

<span data-ttu-id="6200c-168">Уровень = 4 (сведения)</span><span class="sxs-lookup"><span data-stu-id="6200c-168">Level = 4 (Information)</span></span>

<span data-ttu-id="6200c-169">Для операции сброса каталога Winsock отслеживаются следующие события LSP для Winsock:</span><span class="sxs-lookup"><span data-stu-id="6200c-169">The following Winsock LSP events are traced for a Winsock catalog reset operation:</span></span>

-   <span data-ttu-id="6200c-170">Каталог Winsock сброшен.</span><span class="sxs-lookup"><span data-stu-id="6200c-170">The Winsock catalog is reset.</span></span>

<span data-ttu-id="6200c-171">Для события сброса каталога Winsock регистрируются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="6200c-171">The following parameters are logged for a Winsock catalog reset event:</span></span>



| <span data-ttu-id="6200c-172">Параметр</span><span class="sxs-lookup"><span data-stu-id="6200c-172">Parameter</span></span>                                                                                        | <span data-ttu-id="6200c-173">Описание</span><span class="sxs-lookup"><span data-stu-id="6200c-173">Description</span></span>                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6200c-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Каталога</span><span class="sxs-lookup"><span data-stu-id="6200c-174"><span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog</span></span><br/> | <span data-ttu-id="6200c-175">Каталог Winsock (32-разрядный или 64-разрядный), который сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="6200c-175">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="6200c-176">Это целочисленное значение, равное 32 или 64.</span><span class="sxs-lookup"><span data-stu-id="6200c-176">This is an integer value that is either 32 or 64.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="6200c-177">См. также</span><span class="sxs-lookup"><span data-stu-id="6200c-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6200c-178">Управление трассировкой Winsock</span><span class="sxs-lookup"><span data-stu-id="6200c-178">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="6200c-179">Трассировка Winsock</span><span class="sxs-lookup"><span data-stu-id="6200c-179">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="6200c-180">Уровни трассировки Winsock</span><span class="sxs-lookup"><span data-stu-id="6200c-180">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="6200c-181">Сведения о трассировке событий сети Winsock</span><span class="sxs-lookup"><span data-stu-id="6200c-181">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
