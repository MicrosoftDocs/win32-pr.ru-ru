---
description: Возвращает дату окончания срока действия сертификата.
ms.assetid: 25e76b25-9a18-439c-acb8-e0af97b6fcd5
title: Свойство Certificate. Валидтодате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidToDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 08f6c0748c38ec31085c937eda37a413a3644f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688817"
---
# <a name="certificatevalidtodate-property"></a><span data-ttu-id="e23bf-103">Свойство Certificate. Валидтодате</span><span class="sxs-lookup"><span data-stu-id="e23bf-103">Certificate.ValidToDate property</span></span>

<span data-ttu-id="e23bf-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e23bf-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e23bf-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e23bf-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e23bf-106">Свойство **валидтодате** извлекает дату окончания срока действия сертификата.</span><span class="sxs-lookup"><span data-stu-id="e23bf-106">The **ValidToDate** property retrieves the ending date for the validity of the certificate.</span></span>

<span data-ttu-id="e23bf-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e23bf-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e23bf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e23bf-108">Syntax</span></span>


```VB
Certificate.ValidToDate As Date
```



## <a name="property-value"></a><span data-ttu-id="e23bf-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e23bf-109">Property value</span></span>

<span data-ttu-id="e23bf-110">Дата, указывающая дату окончания срока действия сертификата.</span><span class="sxs-lookup"><span data-stu-id="e23bf-110">A date that indicates the ending date for the validity of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="e23bf-111">Требования</span><span class="sxs-lookup"><span data-stu-id="e23bf-111">Requirements</span></span>



| <span data-ttu-id="e23bf-112">Требование</span><span class="sxs-lookup"><span data-stu-id="e23bf-112">Requirement</span></span> | <span data-ttu-id="e23bf-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e23bf-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e23bf-114">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e23bf-114">End of client support</span></span><br/> | <span data-ttu-id="e23bf-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e23bf-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e23bf-116">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e23bf-116">End of server support</span></span><br/> | <span data-ttu-id="e23bf-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e23bf-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e23bf-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e23bf-118">Redistributable</span></span><br/>       | <span data-ttu-id="e23bf-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e23bf-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e23bf-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e23bf-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e23bf-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e23bf-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e23bf-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e23bf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e23bf-123">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="e23bf-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
