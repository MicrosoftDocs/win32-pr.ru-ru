---
description: Свойство Result получает значение, указывающее, действителен ли сертификат. Это свойство по умолчанию.
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: Цертификатестатус. Result, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665073"
---
# <a name="certificatestatusresult-property"></a><span data-ttu-id="a61ae-104">Цертификатестатус. Result, свойство</span><span class="sxs-lookup"><span data-stu-id="a61ae-104">CertificateStatus.Result property</span></span>

<span data-ttu-id="a61ae-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a61ae-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a61ae-106">Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a61ae-106">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a61ae-107">Свойство **result** получает значение, указывающее, действителен ли сертификат.</span><span class="sxs-lookup"><span data-stu-id="a61ae-107">The **Result** property retrieves a value that indicates whether the certificate is valid.</span></span> <span data-ttu-id="a61ae-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a61ae-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a61ae-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a61ae-109">Syntax</span></span>


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a61ae-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a61ae-110">Property value</span></span>

<span data-ttu-id="a61ae-111">**Значение true** показывает, что сертификат действителен.</span><span class="sxs-lookup"><span data-stu-id="a61ae-111">If **true**, the certificate is valid.</span></span> <span data-ttu-id="a61ae-112">Срок действия сертификата проверяется с использованием текущего значения свойства [**чеккфлаг**](certificatestatus-checkflag.md) и различных параметров политики.</span><span class="sxs-lookup"><span data-stu-id="a61ae-112">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the various policy settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="a61ae-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a61ae-113">Requirements</span></span>



| <span data-ttu-id="a61ae-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a61ae-114">Requirement</span></span> | <span data-ttu-id="a61ae-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a61ae-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a61ae-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a61ae-116">End of client support</span></span><br/> | <span data-ttu-id="a61ae-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a61ae-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a61ae-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a61ae-118">End of server support</span></span><br/> | <span data-ttu-id="a61ae-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a61ae-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a61ae-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a61ae-120">Redistributable</span></span><br/>       | <span data-ttu-id="a61ae-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a61ae-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a61ae-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a61ae-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a61ae-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a61ae-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
