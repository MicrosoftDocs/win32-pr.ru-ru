---
description: Установка нового поставщика услуг — это высокопроизводительное устройство и операционная система, поэтому подробные сведения выходят за рамки этого пакета SDK.
ms.assetid: 5b48e144-5092-4462-b74c-d3295d23afe1
title: Установка и инициализация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4391f8453d17cc70382d3ecb0dff65189b61c310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684322"
---
# <a name="installation-and-initialization"></a><span data-ttu-id="4f68b-103">Установка и инициализация</span><span class="sxs-lookup"><span data-stu-id="4f68b-103">Installation and Initialization</span></span>

<span data-ttu-id="4f68b-104">Установка нового поставщика услуг — это высокопроизводительное устройство и операционная система, поэтому подробные сведения выходят за рамки этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="4f68b-104">Installation of a new service provider is highly device- and operating-system-specific, so the details are outside the scope of this SDK.</span></span> <span data-ttu-id="4f68b-105">Как правило, целью установки является настройка поставщика услуг для текущей среды связи.</span><span class="sxs-lookup"><span data-stu-id="4f68b-105">Generally speaking, the goal of installation is configuration of the service provider for the current communications environment.</span></span> <span data-ttu-id="4f68b-106">Обычно это касается записей реестра и настройки зависимостей служб.</span><span class="sxs-lookup"><span data-stu-id="4f68b-106">This usually involves registry entries and the setting of service dependencies.</span></span>

<span data-ttu-id="4f68b-107">Инициализация поставщика услуг телефонии начинается с согласования версий.</span><span class="sxs-lookup"><span data-stu-id="4f68b-107">Initialization of a telephony service provider starts with version negotiation.</span></span> <span data-ttu-id="4f68b-108">Описание согласования версий и текущей версии см. в разделе [Тспи управление версиями](tspi-versioning.md) .</span><span class="sxs-lookup"><span data-stu-id="4f68b-108">See [TSPI Versioning](tspi-versioning.md) for a discussion of version negotiation and current version.</span></span>

<span data-ttu-id="4f68b-109">Затем TAPI вызывает [**тспи \_ провидеринит**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), который передает поставщику указатель на функцию обратного вызова, используемую для отчета о ходе выполнения асинхронных функций.</span><span class="sxs-lookup"><span data-stu-id="4f68b-109">TAPI then calls [**TSPI\_providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit), which passes the provider a pointer to a callback function used to report on asynchronous functions progress.</span></span> <span data-ttu-id="4f68b-110">TSP возвращает количество линий и телефонных устройств, связанных с текущим идентификатором устройства.</span><span class="sxs-lookup"><span data-stu-id="4f68b-110">The TSP returns a count of line and phone devices associated with the current device identifier.</span></span>

<span data-ttu-id="4f68b-111">Как правило, на следующем шаге будет проведена инвентаризация ресурсов, осуществляемая TAPI при вызове [**тспи \_ Линежетдевкапс**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) и [**тспи \_ линежетаддресскапс**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span><span class="sxs-lookup"><span data-stu-id="4f68b-111">Typically, the next step will be resource inventory, conducted by TAPI invoking [**TSPI\_lineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) and [**TSPI\_lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps).</span></span> <span data-ttu-id="4f68b-112">Предполагается, что поставщик услуг заполнит эти элементы структур данных, которые относятся к поддерживаемым им возможностям устройства и сеанса.</span><span class="sxs-lookup"><span data-stu-id="4f68b-112">The service provider is expected to fill in those elements of the data structures involved that pertain to device and session capabilities it supports.</span></span>

<span data-ttu-id="4f68b-113">TAPI собирает информацию из различных приложений, касающихся требований к уведомлениям о событиях, и инструктирует TSP с помощью [**тспи \_ линесетдефаултмедиадетектион**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) , чтобы указать, какие типы мультимедиа следует обнаружить для строки, и [**тспи \_ линесетстатусмессажес**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) , чтобы указать, какие строки и адреса должны быть переданы.</span><span class="sxs-lookup"><span data-stu-id="4f68b-113">TAPI collects information from the various applications concerning event notification requirements, and instructs the TSP using [**TSPI\_lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) to indicate which media types to detect for a line and [**TSPI\_lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages) to indicate which line and address events should be reported.</span></span>

 

 
