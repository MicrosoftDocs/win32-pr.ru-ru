---
description: Свойство Version извлекает номер версии сертификата.
ms.assetid: 7f135a1a-ca77-4ff1-9437-532e468c6b41
title: Свойство Certificate. Version
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Version
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 48d67ac2154f63573cb8b75686b3846e14b0ed65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668495"
---
# <a name="certificateversion-property"></a><span data-ttu-id="9aa9d-103">Свойство Certificate. Version</span><span class="sxs-lookup"><span data-stu-id="9aa9d-103">Certificate.Version property</span></span>

<span data-ttu-id="9aa9d-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9aa9d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9aa9d-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9aa9d-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9aa9d-106">Свойство **Version** извлекает номер версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="9aa9d-106">The **Version** property retrieves the version number of the certificate.</span></span>

<span data-ttu-id="9aa9d-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9aa9d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa9d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9aa9d-108">Syntax</span></span>


```VB
Certificate.Version As Long
```



## <a name="property-value"></a><span data-ttu-id="9aa9d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9aa9d-109">Property value</span></span>

<span data-ttu-id="9aa9d-110">Номер версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="9aa9d-110">The version number of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa9d-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9aa9d-111">Requirements</span></span>



| <span data-ttu-id="9aa9d-112">Требование</span><span class="sxs-lookup"><span data-stu-id="9aa9d-112">Requirement</span></span> | <span data-ttu-id="9aa9d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa9d-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa9d-114">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9aa9d-114">End of client support</span></span><br/> | <span data-ttu-id="9aa9d-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9aa9d-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9aa9d-116">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9aa9d-116">End of server support</span></span><br/> | <span data-ttu-id="9aa9d-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9aa9d-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9aa9d-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9aa9d-118">Redistributable</span></span><br/>       | <span data-ttu-id="9aa9d-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9aa9d-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9aa9d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9aa9d-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9aa9d-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aa9d-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9aa9d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9aa9d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa9d-123">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="9aa9d-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
