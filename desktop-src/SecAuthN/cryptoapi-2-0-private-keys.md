---
description: Учетные данные SChannel представляются внутренне как \_ структуры контекста сертификата.
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 закрытых ключей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647441"
---
# <a name="cryptoapi-20-private-keys"></a><span data-ttu-id="17b3a-103">CryptoAPI 2.0 закрытых ключей</span><span class="sxs-lookup"><span data-stu-id="17b3a-103">CryptoAPI 2.0 Private Keys</span></span>

<span data-ttu-id="17b3a-104">Учетные данные SChannel представляются внутренне как структуры [**\_ контекста сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="17b3a-104">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span> <span data-ttu-id="17b3a-105">Schannel находит [*закрытый ключ*](/windows/desktop/SecGloss/p-gly) , связанный с определенным контекстом сертификата, с помощью \_ \_ \_ свойства ID Prov info ИД сертификата \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="17b3a-105">Schannel locates the [*private key*](/windows/desktop/SecGloss/p-gly) associated with a particular certificate context using the certificate's CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span> <span data-ttu-id="17b3a-106">С помощью этого свойства SChannel обращается к *закрытому ключу* , вызывая функцию [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) .</span><span class="sxs-lookup"><span data-stu-id="17b3a-106">Using this property, Schannel accesses the *private key* by calling the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) function.</span></span> <span data-ttu-id="17b3a-107">Дополнительные сведения см. в разделе [пары открытого и закрытого ключей](/windows/desktop/SecCrypto/public-private-key-pairs).</span><span class="sxs-lookup"><span data-stu-id="17b3a-107">For additional details, see [Public/Private Key Pairs](/windows/desktop/SecCrypto/public-private-key-pairs).</span></span>

<span data-ttu-id="17b3a-108">Все учетные данные SChannel содержат ссылку на один или несколько закрытых ключей, каждый из которых связан с определенным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="17b3a-108">Every Schannel credential contains a reference to one or more private keys, each associated with a particular certificate.</span></span> <span data-ttu-id="17b3a-109">[*Закрытые ключи*](/windows/desktop/SecGloss/p-gly) обрабатываются совершенно по-разному в зависимости от того, предназначены ли учетные данные для клиента или сервера.</span><span class="sxs-lookup"><span data-stu-id="17b3a-109">The [*private keys*](/windows/desktop/SecGloss/p-gly) are handled quite differently depending on whether the credential is for a client or a server.</span></span>

## <a name="client-private-keys"></a><span data-ttu-id="17b3a-110">Закрытые ключи клиента</span><span class="sxs-lookup"><span data-stu-id="17b3a-110">Client Private Keys</span></span>

<span data-ttu-id="17b3a-111">[*Закрытые ключи*](/windows/desktop/SecGloss/p-gly) клиента управляются [*поставщиком служб шифрования*](/windows/desktop/SecGloss/c-gly) (CSP).</span><span class="sxs-lookup"><span data-stu-id="17b3a-111">Client [*private keys*](/windows/desktop/SecGloss/p-gly) are managed by the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) in use.</span></span> <span data-ttu-id="17b3a-112">Закрытые ключи клиента обычно хранятся CSP типа [Prov \_ RSA \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) или Prov \_ RSA \_ Signature.</span><span class="sxs-lookup"><span data-stu-id="17b3a-112">Client private keys are typically stored by CSPs of type [PROV\_RSA\_FULL](/windows/desktop/SecCrypto/prov-rsa-full) or PROV\_RSA\_SIGNATURE.</span></span>

<span data-ttu-id="17b3a-113">Если клиентское приложение выполняет вызов [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) вручную перед вызовом [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), клиент должен привязать маркер CSP к контексту сертификата, используя \_ \_ \_ \_ \_ свойство идентификатора свойства ID Prov Handle.</span><span class="sxs-lookup"><span data-stu-id="17b3a-113">If the client application makes the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) call manually then before calling [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), the client must bind the CSP's handle to the certificate context using the CERT\_KEY\_PROV\_HANDLE\_PROP\_ID property.</span></span> <span data-ttu-id="17b3a-114">Если канал Schannel находит этот набор свойств, он не использует \_ \_ \_ \_ \_ свойство ID Prov info ИД параметра CERT.</span><span class="sxs-lookup"><span data-stu-id="17b3a-114">If Schannel finds this property set, it does not use the CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span>

## <a name="server-private-keys"></a><span data-ttu-id="17b3a-115">Закрытые ключи сервера</span><span class="sxs-lookup"><span data-stu-id="17b3a-115">Server Private Keys</span></span>

<span data-ttu-id="17b3a-116">Закрытые ключи сервера хранятся одним из следующих CSP:</span><span class="sxs-lookup"><span data-stu-id="17b3a-116">Server private keys are stored by one of the following CSPs:</span></span>

-   <span data-ttu-id="17b3a-117">PROV \_ RSA \_ SChannel</span><span class="sxs-lookup"><span data-stu-id="17b3a-117">PROV\_RSA\_SCHANNEL</span></span>
-   <span data-ttu-id="17b3a-118">PROV \_ DH \_ SChannel</span><span class="sxs-lookup"><span data-stu-id="17b3a-118">PROV\_DH\_SCHANNEL</span></span>
-   <span data-ttu-id="17b3a-119">PROV \_ Fortezza CSP</span><span class="sxs-lookup"><span data-stu-id="17b3a-119">PROV\_FORTEZZA CSP</span></span>

<span data-ttu-id="17b3a-120">Выбор CSP зависит от выбранного [*алгоритма обмена ключами*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="17b3a-120">The choice of CSP depends on the selected [*key exchange algorithm*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="17b3a-121">Закрытые ключи сервера должны иметь тип по адресу \_ кэйексчанже.</span><span class="sxs-lookup"><span data-stu-id="17b3a-121">Server private keys must be of type AT\_KEYEXCHANGE.</span></span>

 

 
