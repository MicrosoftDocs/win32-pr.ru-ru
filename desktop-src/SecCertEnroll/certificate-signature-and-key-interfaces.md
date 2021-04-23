---
description: Для управления подписями сертификатов, а также открытыми и закрытыми ключами можно использовать следующие интерфейсы.
ms.assetid: 628d6629-3ec3-447e-8b60-a2db5b23e780
title: Сигнатуры сертификата и интерфейсы ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35d2f3b1404397b1e6f2e436ef27fb740bbb594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911288"
---
# <a name="certificate-signature-and-key-interfaces"></a><span data-ttu-id="63e51-103">Сигнатуры сертификата и интерфейсы ключей</span><span class="sxs-lookup"><span data-stu-id="63e51-103">Certificate Signature and Key Interfaces</span></span>

<span data-ttu-id="63e51-104">Для управления подписями сертификатов, а также открытыми и закрытыми ключами можно использовать следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="63e51-104">The following interfaces can be used to manage certificate signatures, and public and private keys.</span></span>



| <span data-ttu-id="63e51-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="63e51-105">Interface</span></span>                                                      | <span data-ttu-id="63e51-106">Описание</span><span class="sxs-lookup"><span data-stu-id="63e51-106">Description</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63e51-107">**исигнерцертификате**</span><span class="sxs-lookup"><span data-stu-id="63e51-107">**ISignerCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate)               | <span data-ttu-id="63e51-108">Представляет сертификат подписи, позволяющий подписывать запрос на сертификат.</span><span class="sxs-lookup"><span data-stu-id="63e51-108">Represents a signing certificate that enables you to sign a certificate request.</span></span>                  |
| [<span data-ttu-id="63e51-109">**исигнерцертификатес**</span><span class="sxs-lookup"><span data-stu-id="63e51-109">**ISignerCertificates**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificates)             | <span data-ttu-id="63e51-110">Управляет коллекцией объектов [**исигнерцертификате**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) .</span><span class="sxs-lookup"><span data-stu-id="63e51-110">Manages a collection of [**ISignerCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-isignercertificate) objects.</span></span>                 |
| [<span data-ttu-id="63e51-111">**IX509PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="63e51-111">**IX509PrivateKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509privatekey)                     | <span data-ttu-id="63e51-112">Представляет асимметричный закрытый ключ, который можно использовать для шифрования, подписи и соглашения о ключах.</span><span class="sxs-lookup"><span data-stu-id="63e51-112">Represents an asymmetric private key that can be used for encryption, signing, and key agreement.</span></span> |
| [<span data-ttu-id="63e51-113">**IX509PublicKey**</span><span class="sxs-lookup"><span data-stu-id="63e51-113">**IX509PublicKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509publickey)                       | <span data-ttu-id="63e51-114">Представляет открытый ключ в паре открытого и закрытого ключей.</span><span class="sxs-lookup"><span data-stu-id="63e51-114">Represents a public key in a public/private key pair.</span></span>                                             |
| [<span data-ttu-id="63e51-115">**IX509SignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="63e51-115">**IX509SignatureInformation**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509signatureinformation) | <span data-ttu-id="63e51-116">Представляет сведения, используемые для подписания запроса на сертификат.</span><span class="sxs-lookup"><span data-stu-id="63e51-116">Represents information used to sign a certificate request.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="63e51-117">См. также</span><span class="sxs-lookup"><span data-stu-id="63e51-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63e51-118">Интерфейсы Цертенролл</span><span class="sxs-lookup"><span data-stu-id="63e51-118">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



