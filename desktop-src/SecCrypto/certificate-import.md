---
description: Импортирует ранее закодированный сертификат из строки в объект сертификата.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: 'Метод ICertificate2:: Import'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea639f1cd89b673ecf8da77302e3d812894a202b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665397"
---
# <a name="icertificate2import-method"></a><span data-ttu-id="0b4eb-103">Метод ICertificate2:: Import</span><span class="sxs-lookup"><span data-stu-id="0b4eb-103">ICertificate2::Import method</span></span>

<span data-ttu-id="0b4eb-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b4eb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0b4eb-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0b4eb-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0b4eb-106">Метод **Import** импортирует ранее закодированный сертификат из строки в объект [**сертификата**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="0b4eb-106">The **Import** method imports a previously encoded certificate from a string into the [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="0b4eb-107">При вызове этого метода происходит сброс [*состояния*](../secgloss/s-gly.md) этого объекта.</span><span class="sxs-lookup"><span data-stu-id="0b4eb-107">Calling this method resets the [*state*](../secgloss/s-gly.md) of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b4eb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b4eb-108">Syntax</span></span>


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a><span data-ttu-id="0b4eb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b4eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b4eb-110">*Енкодедцертификате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0b4eb-110">*EncodedCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b4eb-111">Строка, содержащая закодированные данные сертификата для импорта.</span><span class="sxs-lookup"><span data-stu-id="0b4eb-111">A string that contains the encoded certificate data to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b4eb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b4eb-112">Return value</span></span>

<span data-ttu-id="0b4eb-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0b4eb-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b4eb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0b4eb-114">Requirements</span></span>



| <span data-ttu-id="0b4eb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0b4eb-115">Requirement</span></span> | <span data-ttu-id="0b4eb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0b4eb-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4eb-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0b4eb-117">End of client support</span></span><br/> | <span data-ttu-id="0b4eb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b4eb-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0b4eb-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0b4eb-119">End of server support</span></span><br/> | <span data-ttu-id="0b4eb-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b4eb-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0b4eb-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0b4eb-121">Redistributable</span></span><br/>       | <span data-ttu-id="0b4eb-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0b4eb-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0b4eb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0b4eb-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0b4eb-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b4eb-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b4eb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b4eb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b4eb-126">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="0b4eb-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="0b4eb-127">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="0b4eb-127">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
