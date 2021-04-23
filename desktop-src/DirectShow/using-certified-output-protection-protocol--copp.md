---
description: Использование протокола сертифицированной выходной защиты (Копп)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Использование протокола сертифицированной выходной защиты (Копп)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673991"
---
# <a name="using-certified-output-protection-protocol-copp"></a><span data-ttu-id="e589b-103">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="e589b-103">Using Certified Output Protection Protocol (COPP)</span></span>

<span data-ttu-id="e589b-104">Протокол сертифицированного выхода (Копп) позволяет приложению защищать поток видео по мере его передачи из графического адаптера на устройство дисплея.</span><span class="sxs-lookup"><span data-stu-id="e589b-104">Certified Output Protection Protocol (COPP) enables an application to protect a video stream as it travels from the graphics adapter to the display device.</span></span> <span data-ttu-id="e589b-105">Приложение может использовать Копп для определения типа физического соединителя, подключенного к устройству вывода, и доступных типов защиты выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e589b-105">An application can use COPP to discover what kind of physical connector is attached to the display device, and what types of output protection are available.</span></span> <span data-ttu-id="e589b-106">К механизмам защиты относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="e589b-106">Protection mechanisms include the following:</span></span>

-   <span data-ttu-id="e589b-107">High-Bandwidth цифровой Защита содержимого (HDCP)</span><span class="sxs-lookup"><span data-stu-id="e589b-107">High-Bandwidth Digital Content Protection (HDCP)</span></span>
-   <span data-ttu-id="e589b-108">Система управления поколением копий — аналоговая (CGMS-A)</span><span class="sxs-lookup"><span data-stu-id="e589b-108">Copy Generation Management System — Analog (CGMS-A)</span></span>
-   <span data-ttu-id="e589b-109">Аналоговая защита от копирования (ACP)</span><span class="sxs-lookup"><span data-stu-id="e589b-109">Analog Copy Protection (ACP)</span></span>

<span data-ttu-id="e589b-110">Если графический адаптер поддерживает один из этих механизмов, приложение может использовать Копп для установки уровня защиты.</span><span class="sxs-lookup"><span data-stu-id="e589b-110">If the graphics adapter supports one of these mechanisms, the application can use COPP to set the protection level.</span></span>

<span data-ttu-id="e589b-111">Копп определяет протокол, используемый для установления безопасного канала связи с драйвером графики.</span><span class="sxs-lookup"><span data-stu-id="e589b-111">COPP defines a protocol that is used to establish a secure communications channel with the graphics driver.</span></span> <span data-ttu-id="e589b-112">Он использует коды проверки подлинности сообщений (Mac) для проверки целостности команд Копп, передаваемых между приложением и драйвером экрана.</span><span class="sxs-lookup"><span data-stu-id="e589b-112">It uses Message Authentication Codes (MACs) to verify the integrity of the COPP commands that are passed between the application and the display driver.</span></span> <span data-ttu-id="e589b-113">Приложение использует Копп, вызывая методы в интерфейсе [**иамцертифиедаутпутпротектион**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) фильтра прорисовки формирователя видео в DIRECTSHOW (VMR-7 или VMR-9).</span><span class="sxs-lookup"><span data-stu-id="e589b-113">The application uses COPP by calling methods on the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface of the DirectShow Video Mixing Renderer filter (VMR-7 or VMR-9).</span></span>

<span data-ttu-id="e589b-114">Копп не определяет никаких сведений о политиках цифровых прав, которые могут применяться к цифровому содержимому мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e589b-114">COPP does not define anything about the digital rights policies that might apply to digital media content.</span></span> <span data-ttu-id="e589b-115">Кроме того, сам Копп не реализует никаких систем защиты выхода.</span><span class="sxs-lookup"><span data-stu-id="e589b-115">Also, COPP itself does not implement any output protection systems.</span></span> <span data-ttu-id="e589b-116">Протокол Копп просто предоставляет способ установки и запроса уровней защиты графического адаптера с помощью систем защиты, предоставляемых адаптером.</span><span class="sxs-lookup"><span data-stu-id="e589b-116">The COPP protocol simply provides a way to set and query protection levels on the graphics adapter, using the protection systems provided by the adapter.</span></span>

<span data-ttu-id="e589b-117">В этом разделе предполагается, что вы знакомы со следующими технологиями:</span><span class="sxs-lookup"><span data-stu-id="e589b-117">This section assumes that you are familiar with the following technologies:</span></span>

-   <span data-ttu-id="e589b-118">DirectShow</span><span class="sxs-lookup"><span data-stu-id="e589b-118">DirectShow</span></span>
-   <span data-ttu-id="e589b-119">Пакет SDK для формата Windows Media</span><span class="sxs-lookup"><span data-stu-id="e589b-119">Windows Media Format SDK</span></span>
-   <span data-ttu-id="e589b-120">XML</span><span class="sxs-lookup"><span data-stu-id="e589b-120">XML</span></span>
-   <span data-ttu-id="e589b-121">Шифрование с открытым ключом и симметричное шифрование</span><span class="sxs-lookup"><span data-stu-id="e589b-121">Public-key cryptography and symmetric cryptography</span></span>

<span data-ttu-id="e589b-122">В примерах кода в этом разделе для выполнения криптографических операций используется CryptoAPI Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="e589b-122">The code examples in this section use Microsoft's CryptoAPI to perform cryptographic operations.</span></span> <span data-ttu-id="e589b-123">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="e589b-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="e589b-124">Общие сведения о Копп</span><span class="sxs-lookup"><span data-stu-id="e589b-124">Overview of COPP</span></span>](overview-of-copp.md)
-   [<span data-ttu-id="e589b-125">Получение цепочки сертификатов драйвера</span><span class="sxs-lookup"><span data-stu-id="e589b-125">Obtaining the Driver's Certificate Chain</span></span>](obtaining-the-drivers-certificate-chain.md)
-   [<span data-ttu-id="e589b-126">Проверка цепочки сертификатов</span><span class="sxs-lookup"><span data-stu-id="e589b-126">Validating the Certificate Chain</span></span>](validating-the-certificate-chain.md)
-   [<span data-ttu-id="e589b-127">Списки отзыва сертификатов</span><span class="sxs-lookup"><span data-stu-id="e589b-127">Certificate Revocation Lists</span></span>](certificate-revocation-lists.md)
-   [<span data-ttu-id="e589b-128">Импорт открытого ключа драйвера</span><span class="sxs-lookup"><span data-stu-id="e589b-128">Importing the Driver's Public Key</span></span>](importing-the-drivers-public-key.md)
-   [<span data-ttu-id="e589b-129">Запуск сеанса Копп</span><span class="sxs-lookup"><span data-stu-id="e589b-129">Initiating a COPP Session</span></span>](initiating-a-copp-session.md)
-   [<span data-ttu-id="e589b-130">Отправка запросов состояния Копп</span><span class="sxs-lookup"><span data-stu-id="e589b-130">Sending COPP Status Requests</span></span>](sending-copp-status-requests.md)
-   [<span data-ttu-id="e589b-131">Отправка команд Копп</span><span class="sxs-lookup"><span data-stu-id="e589b-131">Sending COPP Commands</span></span>](sending-copp-commands.md)
-   [<span data-ttu-id="e589b-132">Проверка того, поддерживает ли графический драйвер Копп</span><span class="sxs-lookup"><span data-stu-id="e589b-132">Testing Whether a Graphics Driver Supports COPP</span></span>](testing-whether-a-graphics-driver-supports-copp.md)
-   [<span data-ttu-id="e589b-133">Справочник по запросам Копп</span><span class="sxs-lookup"><span data-stu-id="e589b-133">COPP Query Reference</span></span>](copp-query-reference.md)
-   [<span data-ttu-id="e589b-134">Справочник по командам Копп</span><span class="sxs-lookup"><span data-stu-id="e589b-134">COPP Command Reference</span></span>](copp-command-reference.md)

## <a name="related-topics"></a><span data-ttu-id="e589b-135">См. также</span><span class="sxs-lookup"><span data-stu-id="e589b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e589b-136">Использование модуля подготовки видео для микширования</span><span class="sxs-lookup"><span data-stu-id="e589b-136">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



