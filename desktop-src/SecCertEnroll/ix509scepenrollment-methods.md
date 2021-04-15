---
description: Интерфейс IX509SCEPEnrollment предоставляет следующие методы.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Методы IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683827"
---
# <a name="ix509scepenrollment-methods"></a><span data-ttu-id="f4daf-103">Методы IX509SCEPEnrollment</span><span class="sxs-lookup"><span data-stu-id="f4daf-103">IX509SCEPEnrollment Methods</span></span>

<span data-ttu-id="f4daf-104">Интерфейс [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f4daf-104">The [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f4daf-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="f4daf-105">In this section</span></span>



| <span data-ttu-id="f4daf-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="f4daf-106">Topic</span></span>                                                                                                              | <span data-ttu-id="f4daf-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f4daf-107">Description</span></span>                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4daf-108">**Метод Креатерекуестмессаже**</span><span class="sxs-lookup"><span data-stu-id="f4daf-108">**CreateRequestMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | <span data-ttu-id="f4daf-109">Создайте сообщение запроса PKCS10 с паролем вызова.</span><span class="sxs-lookup"><span data-stu-id="f4daf-109">Create a PKCS10 request message with a challenge password.</span></span> <span data-ttu-id="f4daf-110">Сообщение запроса находится в конверте PKCS7, зашифрованном с помощью сертификата шифрования сервера SCEP и подписанного сертификатом подписи сервера.</span><span class="sxs-lookup"><span data-stu-id="f4daf-110">The request message is in an enveloped PKCS7 encrypted with the SCEP server encryption certificate and signed by the server signing certificate.</span></span><br/> |
| [<span data-ttu-id="f4daf-111">**Метод Креатеретриевецертификатемессаже**</span><span class="sxs-lookup"><span data-stu-id="f4daf-111">**CreateRetrieveCertificateMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | <span data-ttu-id="f4daf-112">Получение ранее выданного сертификата.</span><span class="sxs-lookup"><span data-stu-id="f4daf-112">Retrieve a previously issued certificate.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="f4daf-113">**Метод Креатеретриевепендингмессаже**</span><span class="sxs-lookup"><span data-stu-id="f4daf-113">**CreateRetrievePendingMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | <span data-ttu-id="f4daf-114">Создайте сообщение для опроса сертификатов (регистрация вручную).</span><span class="sxs-lookup"><span data-stu-id="f4daf-114">Create a message for certificate polling (manual enrollment).</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="f4daf-115">**Метод Делетерекуест**</span><span class="sxs-lookup"><span data-stu-id="f4daf-115">**DeleteRequest method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | <span data-ttu-id="f4daf-116">Удалите все сертификаты или ключи, созданные для запроса.</span><span class="sxs-lookup"><span data-stu-id="f4daf-116">Delete any certificates or keys created for the request.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="f4daf-117">**Метод Initialize**</span><span class="sxs-lookup"><span data-stu-id="f4daf-117">**Initialize method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | <span data-ttu-id="f4daf-118">Инициализируйте экземпляр при подготовке для нового запроса.</span><span class="sxs-lookup"><span data-stu-id="f4daf-118">Initialize the instance in preparation for a new request.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="f4daf-119">**Метод Инитиализефорпендинг**</span><span class="sxs-lookup"><span data-stu-id="f4daf-119">**InitializeForPending method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | <span data-ttu-id="f4daf-120">Инициализируйте экземпляр, чтобы подготовиться к формированию сообщения для получения выданного сертификата, или установите ответ на предыдущий запрос от издателя.</span><span class="sxs-lookup"><span data-stu-id="f4daf-120">Initialize the instance to prepare to generate a message to either retrieve an issued certificate, or install a response for a previous request by the issuer.</span></span><br/>                                              |
| [<span data-ttu-id="f4daf-121">**Метод Процессреспонсемессаже**</span><span class="sxs-lookup"><span data-stu-id="f4daf-121">**ProcessResponseMessage method**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | <span data-ttu-id="f4daf-122">Обработка ответного сообщения и возврат метода обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="f4daf-122">Process a response message and return the disposition of the message.</span></span><br/>                                                                                                                                       |



 

 

 




