---
description: Извлекает строку, содержащую имя издателя сертификата.
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Свойство Certificate. IssuerName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b34b3bf198759d08fd3d0e3e4261407389a69a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668496"
---
# <a name="certificateissuername-property"></a><span data-ttu-id="51cbe-103">Свойство Certificate. IssuerName</span><span class="sxs-lookup"><span data-stu-id="51cbe-103">Certificate.IssuerName property</span></span>

<span data-ttu-id="51cbe-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="51cbe-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="51cbe-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="51cbe-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="51cbe-106">Свойство **IssuerName** извлекает строку, содержащую имя издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="51cbe-106">The **IssuerName** property retrieves a string that contains the name of the certificate issuer.</span></span>

<span data-ttu-id="51cbe-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="51cbe-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="51cbe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51cbe-108">Syntax</span></span>


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a><span data-ttu-id="51cbe-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="51cbe-109">Property value</span></span>

<span data-ttu-id="51cbe-110">Строка, содержащая имя издателя сертификата.</span><span class="sxs-lookup"><span data-stu-id="51cbe-110">String that contains the name of the certificate issuer.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cbe-111">Требования</span><span class="sxs-lookup"><span data-stu-id="51cbe-111">Requirements</span></span>



| <span data-ttu-id="51cbe-112">Требование</span><span class="sxs-lookup"><span data-stu-id="51cbe-112">Requirement</span></span> | <span data-ttu-id="51cbe-113">Значение</span><span class="sxs-lookup"><span data-stu-id="51cbe-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51cbe-114">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="51cbe-114">End of client support</span></span><br/> | <span data-ttu-id="51cbe-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51cbe-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="51cbe-116">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="51cbe-116">End of server support</span></span><br/> | <span data-ttu-id="51cbe-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51cbe-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="51cbe-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="51cbe-118">Redistributable</span></span><br/>       | <span data-ttu-id="51cbe-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="51cbe-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="51cbe-120">DLL</span><span class="sxs-lookup"><span data-stu-id="51cbe-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="51cbe-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51cbe-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
