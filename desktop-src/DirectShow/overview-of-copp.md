---
description: Общие сведения о Копп
ms.assetid: 4421ab65-e44a-4d1f-8d9b-b187227429c6
title: Общие сведения о Копп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fc83293c1914ed69700cabb9507841d03a7ad3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682241"
---
# <a name="overview-of-copp"></a><span data-ttu-id="5378d-103">Общие сведения о Копп</span><span class="sxs-lookup"><span data-stu-id="5378d-103">Overview of COPP</span></span>

<span data-ttu-id="5378d-104">Ниже приведены основные шаги, которые необходимо выполнить приложению для использования протокола Копп.</span><span class="sxs-lookup"><span data-stu-id="5378d-104">Here are the basic steps that an application must perform to use Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="5378d-105">**Получение цепочки сертификатов драйвера**</span><span class="sxs-lookup"><span data-stu-id="5378d-105">**Get the driver's certificate chain**</span></span>

1.  <span data-ttu-id="5378d-106">Создайте граф воспроизведения DirectShow, который визуализирует видео с помощью формирователя микширования видео (VMR-7 или VMR-9) или [**расширенного**](enhanced-video-renderer-filter.md) фильтра модуля подготовки отчетов (Евр).</span><span class="sxs-lookup"><span data-stu-id="5378d-106">Build a DirectShow playback graph that renders video using the Video Mixing Renderer (VMR-7 or VMR-9) or the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) filter (EVR).</span></span>
2.  <span data-ttu-id="5378d-107">Запросите VMR для интерфейса [**иамцертифиедаутпутпротектион**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) .</span><span class="sxs-lookup"><span data-stu-id="5378d-107">Query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface.</span></span>
3.  <span data-ttu-id="5378d-108">Вызовите [**иамцертифиедаутпутпротектион:: кэйексчанже**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="5378d-108">Call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="5378d-109">Этот метод возвращает 128-разрядное случайное число из драйвера, а также цепочку сертификатов, содержащую 2048-разрядный открытый ключ RSA драйвера.</span><span class="sxs-lookup"><span data-stu-id="5378d-109">This method returns a 128-bit random number from the driver, along with a certificate chain that contains the driver's 2048-bit RSA public key.</span></span>

<span data-ttu-id="5378d-110">**Проверка цепочки сертификатов**</span><span class="sxs-lookup"><span data-stu-id="5378d-110">**Validate the certificate chain**</span></span>

1.  <span data-ttu-id="5378d-111">Проверьте цепочку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="5378d-111">Validate the certificate chain.</span></span> <span data-ttu-id="5378d-112">Если цепочка сертификатов недействительна, прервите ее.</span><span class="sxs-lookup"><span data-stu-id="5378d-112">If the certificate chain is not valid, stop.</span></span>
2.  <span data-ttu-id="5378d-113">Проверьте список отзыва сертификатов (CRL).</span><span class="sxs-lookup"><span data-stu-id="5378d-113">Check the certificate revocation list (CRL).</span></span> <span data-ttu-id="5378d-114">Если какой бы то ни было сертификат в цепочке сертификатов появился в списке отзыва, прервите его.</span><span class="sxs-lookup"><span data-stu-id="5378d-114">If any of the certificates in the certificate chain appears in the revocation list, stop.</span></span>
3.  <span data-ttu-id="5378d-115">Получите открытый ключ RSA из цепочки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="5378d-115">Get the RSA public key from the certificate chain.</span></span>

<span data-ttu-id="5378d-116">**Инициализация сеанса Копп**</span><span class="sxs-lookup"><span data-stu-id="5378d-116">**Initialize the COPP Session**</span></span>

1.  <span data-ttu-id="5378d-117">Создайте 128-разрядный ключ сеанса AES.</span><span class="sxs-lookup"><span data-stu-id="5378d-117">Generate a 128-bit AES session key.</span></span> <span data-ttu-id="5378d-118">Этот ключ используется для подписывания данных и проверки того, что подписанные данные не были изменены.</span><span class="sxs-lookup"><span data-stu-id="5378d-118">This key is used to sign data and to verify that signed data has not been tampered with.</span></span>
2.  <span data-ttu-id="5378d-119">Создание двух криптографических безопасных случайных чисел с защитой 32.</span><span class="sxs-lookup"><span data-stu-id="5378d-119">Generate two cryptographically secure 32-bit random numbers.</span></span> <span data-ttu-id="5378d-120">Первый — это порядковый номер состояния, второй — порядковый номер команды.</span><span class="sxs-lookup"><span data-stu-id="5378d-120">The first is a status sequence number, and the second is a command sequence number.</span></span> <span data-ttu-id="5378d-121">Каждый раз, когда приложение отправляет команду или запрос состояния, оно увеличивает соответствующий порядковый номер и включает этот номер в команду Копп или данные запроса.</span><span class="sxs-lookup"><span data-stu-id="5378d-121">Each time the application sends a command or status request, it increments the corresponding sequence number, and includes this number in the COPP command or request data.</span></span>
3.  <span data-ttu-id="5378d-122">Объедините 128-разрядное случайное число из графического драйвера, ключа сеанса AES, порядкового номера состояния и порядкового номера команды.</span><span class="sxs-lookup"><span data-stu-id="5378d-122">Concatenate the 128-bit random number from the graphics driver, the AES session key, the status sequence number, and the command sequence number.</span></span> <span data-ttu-id="5378d-123">Зашифруйте этот массив байтов с помощью открытого ключа драйвера и передайте результат в [**иамцертифиедаутпутпротектион:: сессионсекуенцестарт**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span><span class="sxs-lookup"><span data-stu-id="5378d-123">Encrypt this byte array using the driver's public key and pass the result to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart).</span></span>

<span data-ttu-id="5378d-124">**Отправка команд Копп и запросов состояния**</span><span class="sxs-lookup"><span data-stu-id="5378d-124">**Send COPP Commands and Status Requests**</span></span>

1.  <span data-ttu-id="5378d-125">Запросите доступные типы защиты и другие сведения, вызвав [**иамцертифиедаутпутпротектион::P ротектионстатус**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span><span class="sxs-lookup"><span data-stu-id="5378d-125">Query for the available protection types and other information by calling [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus).</span></span>
2.  <span data-ttu-id="5378d-126">Задайте требуемые уровни защиты, вызвав [**иамцертифиедаутпутпротектион::P ротектионкомманд**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span><span class="sxs-lookup"><span data-stu-id="5378d-126">Set the desired protection levels by calling [**IAMCertifiedOutputProtection::ProtectionCommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand).</span></span>
3.  <span data-ttu-id="5378d-127">Периодически запрашивает текущий локальный уровень защиты.</span><span class="sxs-lookup"><span data-stu-id="5378d-127">Periodically query for the current local protection level.</span></span> <span data-ttu-id="5378d-128">Остановка воспроизведения при неожиданном изменении локального уровня защиты или обнаружении проблемы.</span><span class="sxs-lookup"><span data-stu-id="5378d-128">Stop playback if the local protection level changes unexpectedly or if a problem is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5378d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5378d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5378d-130">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="5378d-130">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



