---
description: Получает логическое значение, указывающее, помечено ли расширение как критическое.
ms.assetid: 71f55d63-a51c-472c-81fc-59212c97bb34
title: Свойство Extension. «Critical»
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 61e53f869a7063e029cb629b8b2fff4cff025b31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665418"
---
# <a name="extensioniscritical-property"></a><span data-ttu-id="37e17-103">Свойство Extension. «Critical»</span><span class="sxs-lookup"><span data-stu-id="37e17-103">Extension.IsCritical property</span></span>

<span data-ttu-id="37e17-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37e17-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="37e17-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="37e17-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="37e17-106">Свойство « **Critical** » получает логическое значение, указывающее, помечено ли расширение как критическое.</span><span class="sxs-lookup"><span data-stu-id="37e17-106">The **IsCritical** property retrieves a Boolean value that indicates whether the extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="37e17-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37e17-107">Syntax</span></span>


```VB
Extension.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="37e17-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="37e17-108">Property value</span></span>

<span data-ttu-id="37e17-109">Если **значение равно true**, расширение помечено как критическое.</span><span class="sxs-lookup"><span data-stu-id="37e17-109">If **true**, the extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="37e17-110">Требования</span><span class="sxs-lookup"><span data-stu-id="37e17-110">Requirements</span></span>



| <span data-ttu-id="37e17-111">Требование</span><span class="sxs-lookup"><span data-stu-id="37e17-111">Requirement</span></span> | <span data-ttu-id="37e17-112">Значение</span><span class="sxs-lookup"><span data-stu-id="37e17-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37e17-113">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="37e17-113">End of client support</span></span><br/> | <span data-ttu-id="37e17-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="37e17-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="37e17-115">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="37e17-115">End of server support</span></span><br/> | <span data-ttu-id="37e17-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37e17-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="37e17-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="37e17-117">Redistributable</span></span><br/>       | <span data-ttu-id="37e17-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="37e17-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="37e17-119">DLL</span><span class="sxs-lookup"><span data-stu-id="37e17-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="37e17-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37e17-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
