---
description: Извлекает строку, содержащую серийный номер сертификата.
ms.assetid: d08be744-4ae8-49f9-8b00-48e76c296f2b
title: Свойство Certificate. SerialNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SerialNumber
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6dbd9485891cc89e686cef118e12dd43ec400f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685389"
---
# <a name="certificateserialnumber-property"></a><span data-ttu-id="df3fd-103">Свойство Certificate. SerialNumber</span><span class="sxs-lookup"><span data-stu-id="df3fd-103">Certificate.SerialNumber property</span></span>

<span data-ttu-id="df3fd-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="df3fd-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="df3fd-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="df3fd-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="df3fd-106">Свойство **SerialNumber** извлекает строку, содержащую серийный номер сертификата.</span><span class="sxs-lookup"><span data-stu-id="df3fd-106">The **SerialNumber** property retrieves a string that contains the certificate serial number.</span></span>

<span data-ttu-id="df3fd-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="df3fd-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df3fd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df3fd-108">Syntax</span></span>


```VB
Certificate.SerialNumber As String
```



## <a name="property-value"></a><span data-ttu-id="df3fd-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="df3fd-109">Property value</span></span>

<span data-ttu-id="df3fd-110">Строка, содержащая серийный номер сертификата.</span><span class="sxs-lookup"><span data-stu-id="df3fd-110">A string that contains the certificate serial number.</span></span>

## <a name="requirements"></a><span data-ttu-id="df3fd-111">Требования</span><span class="sxs-lookup"><span data-stu-id="df3fd-111">Requirements</span></span>



| <span data-ttu-id="df3fd-112">Требование</span><span class="sxs-lookup"><span data-stu-id="df3fd-112">Requirement</span></span> | <span data-ttu-id="df3fd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="df3fd-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df3fd-114">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="df3fd-114">End of client support</span></span><br/> | <span data-ttu-id="df3fd-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df3fd-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="df3fd-116">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="df3fd-116">End of server support</span></span><br/> | <span data-ttu-id="df3fd-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df3fd-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="df3fd-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="df3fd-118">Redistributable</span></span><br/>       | <span data-ttu-id="df3fd-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="df3fd-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="df3fd-120">DLL</span><span class="sxs-lookup"><span data-stu-id="df3fd-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="df3fd-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df3fd-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
