---
description: Интерфейс IX509SCEPEnrollment предоставляет следующие свойства.
ms.assetid: 53BE8DE9-87AC-41D1-B1B5-2FEC72F5FCEA
title: Свойства IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fd9b4cbf9df87f898e61ce0220243044b24607d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683826"
---
# <a name="ix509scepenrollment-properties"></a><span data-ttu-id="882c0-103">Свойства IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="882c0-103">IX509SCEPEnrollment Properties</span></span>

<span data-ttu-id="882c0-104">Интерфейс [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="882c0-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="882c0-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="882c0-105">In this section</span></span>



| <span data-ttu-id="882c0-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="882c0-106">Topic</span></span>                                                                                              | <span data-ttu-id="882c0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="882c0-107">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="882c0-108">**Свойство Certificate**</span><span class="sxs-lookup"><span data-stu-id="882c0-108">**Certificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificate)<br/>                         | <span data-ttu-id="882c0-109">Возвращает сертификат для запроса.</span><span class="sxs-lookup"><span data-stu-id="882c0-109">Gets the certificate for the request.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="882c0-110">**CertificateFriendlyName, свойство**</span><span class="sxs-lookup"><span data-stu-id="882c0-110">**CertificateFriendlyName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_certificatefriendlyname)<br/> | <span data-ttu-id="882c0-111">Возвращает или задает понятное имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="882c0-111">Gets or sets the friendly name for the certificate.</span></span><br/>                                                                                         |
| [<span data-ttu-id="882c0-112">**Фаилинфо, свойство**</span><span class="sxs-lookup"><span data-stu-id="882c0-112">**FailInfo property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_failinfo)<br/>                               | <span data-ttu-id="882c0-113">Получает сведения, когда метод [**процессреспонсемессаже**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) обнаруживает сбойную среду.</span><span class="sxs-lookup"><span data-stu-id="882c0-113">Gets information when the [**ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage) method detects a failed environment.</span></span><br/> |
| [<span data-ttu-id="882c0-114">**Олдцертификате, свойство**</span><span class="sxs-lookup"><span data-stu-id="882c0-114">**OldCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_oldcertificate)<br/>                   | <span data-ttu-id="882c0-115">Возвращает или задает старый сертификат, который должен быть заменен запросом.</span><span class="sxs-lookup"><span data-stu-id="882c0-115">Gets or sets an old certificate that a request is intended to replace.</span></span><br/>                                                                      |
| [<span data-ttu-id="882c0-116">**Свойство запроса**</span><span class="sxs-lookup"><span data-stu-id="882c0-116">**Request property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_request)<br/>                                 | <span data-ttu-id="882c0-117">Получает внутренний запрос PKCS10.</span><span class="sxs-lookup"><span data-stu-id="882c0-117">Gets the inner PKCS10 request.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="882c0-118">**Серверкапабилитиес, свойство**</span><span class="sxs-lookup"><span data-stu-id="882c0-118">**ServerCapabilities property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_servercapabilities)<br/>           | <span data-ttu-id="882c0-119">Задает предпочтительные алгоритмы хэширования и шифрования для запроса.</span><span class="sxs-lookup"><span data-stu-id="882c0-119">Sets the preferred hash and encryption algorithms for the request.</span></span><br/>                                                                          |
| [<span data-ttu-id="882c0-120">**Сигнерцертификате, свойство**</span><span class="sxs-lookup"><span data-stu-id="882c0-120">**SignerCertificate property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_signercertificate)<br/>             | <span data-ttu-id="882c0-121">Возвращает или задает сертификат подписи для запроса.</span><span class="sxs-lookup"><span data-stu-id="882c0-121">Gets or sets the signer certificate for the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="882c0-122">**Свойство без уведомления**</span><span class="sxs-lookup"><span data-stu-id="882c0-122">**Silent property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-put_silent)<br/>                                   | <span data-ttu-id="882c0-123">Возвращает или задает значение, указывающее, следует ли разрешить пользовательский интерфейс во время запроса.</span><span class="sxs-lookup"><span data-stu-id="882c0-123">Gets or sets whether to allow UI during the request.</span></span><br/>                                                                                        |
| [<span data-ttu-id="882c0-124">**Свойство Status**</span><span class="sxs-lookup"><span data-stu-id="882c0-124">**Status property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_status)<br/>                                   | <span data-ttu-id="882c0-125">Возвращает состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="882c0-125">Gets the status of the request.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="882c0-126">**ИД транзакции, свойство**</span><span class="sxs-lookup"><span data-stu-id="882c0-126">**TransactionId property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-get_transactionid)<br/>                     | <span data-ttu-id="882c0-127">Возвращает или задает идентификатор транзакции для запроса.</span><span class="sxs-lookup"><span data-stu-id="882c0-127">Gets or sets the transaction id for the request.</span></span><br/>                                                                                            |



 

 

 




