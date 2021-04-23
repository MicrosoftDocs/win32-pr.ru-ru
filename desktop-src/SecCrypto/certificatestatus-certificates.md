---
description: Задает или получает коллекцию сертификатов, которые можно использовать для построения цепочки сертификатов.
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: Цертификатестатус. Certificates, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665355"
---
# <a name="certificatestatuscertificates-property"></a><span data-ttu-id="a88c3-103">Цертификатестатус. Certificates, свойство</span><span class="sxs-lookup"><span data-stu-id="a88c3-103">CertificateStatus.Certificates property</span></span>

<span data-ttu-id="a88c3-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a88c3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a88c3-105">Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a88c3-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a88c3-106">Свойство **Certificates** задает или получает коллекцию сертификатов, которые могут использоваться для построения цепочки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a88c3-106">The **Certificates** property sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a88c3-107">Syntax</span></span>


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="a88c3-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a88c3-108">Property value</span></span>

<span data-ttu-id="a88c3-109">Объект [**Certificates**](certificates.md) , представляющий коллекцию сертификатов, которые могут использоваться для создания цепочки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="a88c3-109">A [**Certificates**](certificates.md) object that represents the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="a88c3-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a88c3-110">Requirements</span></span>



| <span data-ttu-id="a88c3-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a88c3-111">Requirement</span></span> | <span data-ttu-id="a88c3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a88c3-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a88c3-113">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a88c3-113">End of client support</span></span><br/> | <span data-ttu-id="a88c3-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a88c3-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a88c3-115">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a88c3-115">End of server support</span></span><br/> | <span data-ttu-id="a88c3-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a88c3-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a88c3-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a88c3-117">Redistributable</span></span><br/>       | <span data-ttu-id="a88c3-118">CAPICOM 2,1 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a88c3-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a88c3-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a88c3-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a88c3-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a88c3-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
