---
description: Извлекает строку, содержащую имя субъекта сертификата.
ms.assetid: 95dc7e8b-6670-4dfc-9fe1-d37635fb92d6
title: Свойство Certificate. SubjectName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SubjectName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b17d99ab3ab485153a0af535aa74b9a9123ddaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685151"
---
# <a name="certificatesubjectname-property"></a><span data-ttu-id="d73c4-103">Свойство Certificate. SubjectName</span><span class="sxs-lookup"><span data-stu-id="d73c4-103">Certificate.SubjectName property</span></span>

<span data-ttu-id="d73c4-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d73c4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d73c4-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d73c4-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d73c4-106">Свойство **SubjectName** извлекает строку, содержащую имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="d73c4-106">The **SubjectName** property retrieves a string that contains the name of the certificate subject.</span></span>

<span data-ttu-id="d73c4-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d73c4-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d73c4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d73c4-108">Syntax</span></span>


```VB
Certificate.SubjectName As String
```



## <a name="property-value"></a><span data-ttu-id="d73c4-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d73c4-109">Property value</span></span>

<span data-ttu-id="d73c4-110">Строка, содержащая имя субъекта сертификата.</span><span class="sxs-lookup"><span data-stu-id="d73c4-110">A string that contains the name of the certificate subject.</span></span>

## <a name="requirements"></a><span data-ttu-id="d73c4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d73c4-111">Requirements</span></span>



| <span data-ttu-id="d73c4-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d73c4-112">Requirement</span></span> | <span data-ttu-id="d73c4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d73c4-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d73c4-114">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d73c4-114">End of client support</span></span><br/> | <span data-ttu-id="d73c4-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d73c4-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d73c4-116">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d73c4-116">End of server support</span></span><br/> | <span data-ttu-id="d73c4-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d73c4-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d73c4-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d73c4-118">Redistributable</span></span><br/>       | <span data-ttu-id="d73c4-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="d73c4-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d73c4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d73c4-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d73c4-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d73c4-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d73c4-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d73c4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73c4-123">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="d73c4-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
