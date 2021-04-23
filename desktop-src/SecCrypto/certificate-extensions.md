---
description: Возвращает коллекцию расширений, связанных с сертификатом.
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: 'Метод ICertificate2:: Extensions'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cc96dee9c33bb3f76e1fb17acb2000f9740d1b5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668795"
---
# <a name="icertificate2extensions-method"></a><span data-ttu-id="f9d35-103">Метод ICertificate2:: Extensions</span><span class="sxs-lookup"><span data-stu-id="f9d35-103">ICertificate2::Extensions method</span></span>

<span data-ttu-id="f9d35-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f9d35-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f9d35-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f9d35-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f9d35-106">Метод **Extensions** Возвращает коллекцию расширений, связанных с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="f9d35-106">The **Extensions** method returns a collection of the extensions associated with the certificate.</span></span> <span data-ttu-id="f9d35-107">Этот метод появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f9d35-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d35-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9d35-108">Syntax</span></span>


```VB
Certificate.Extensions()
```



## <a name="parameters"></a><span data-ttu-id="f9d35-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9d35-109">Parameters</span></span>

<span data-ttu-id="f9d35-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f9d35-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9d35-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9d35-111">Return value</span></span>

<span data-ttu-id="f9d35-112">Объект [**Extensions**](extensions.md) , представляющий все расширения, связанные с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="f9d35-112">An [**Extensions**](extensions.md) object that represents all of the extensions associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d35-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f9d35-113">Requirements</span></span>



| <span data-ttu-id="f9d35-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f9d35-114">Requirement</span></span> | <span data-ttu-id="f9d35-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f9d35-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d35-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f9d35-116">End of client support</span></span><br/> | <span data-ttu-id="f9d35-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9d35-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f9d35-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f9d35-118">End of server support</span></span><br/> | <span data-ttu-id="f9d35-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9d35-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f9d35-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f9d35-120">Redistributable</span></span><br/>       | <span data-ttu-id="f9d35-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="f9d35-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f9d35-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f9d35-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f9d35-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9d35-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
