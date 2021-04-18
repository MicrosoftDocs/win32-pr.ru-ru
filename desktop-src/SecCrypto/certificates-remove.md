---
description: Удаляет из коллекции один объект сертификата.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'Метод ICertificates2:: Remove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689242"
---
# <a name="icertificates2remove-method"></a><span data-ttu-id="bef0f-103">Метод ICertificates2:: Remove</span><span class="sxs-lookup"><span data-stu-id="bef0f-103">ICertificates2::Remove method</span></span>

<span data-ttu-id="bef0f-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bef0f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="bef0f-105">Вместо этого используйте [**класс X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bef0f-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bef0f-106">Метод **Remove** удаляет из коллекции один объект [**сертификата**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="bef0f-106">The **Remove** method removes a single [**Certificate**](certificate.md) object from the collection.</span></span> <span data-ttu-id="bef0f-107">Этот метод появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="bef0f-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="bef0f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bef0f-108">Syntax</span></span>


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="bef0f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bef0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bef0f-110">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bef0f-110">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bef0f-111">Значение индекса для удаляемого объекта [**сертификата**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="bef0f-111">Index value for the [**Certificate**](certificate.md) object to be removed.</span></span> <span data-ttu-id="bef0f-112">Этот параметр может иметь один из следующих возможных типов.</span><span class="sxs-lookup"><span data-stu-id="bef0f-112">This parameter can be one of the following possible types.</span></span>



| <span data-ttu-id="bef0f-113">Тип</span><span class="sxs-lookup"><span data-stu-id="bef0f-113">Type</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="bef0f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bef0f-114">Meaning</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <span data-ttu-id="bef0f-115">\* \* \* \* <dt>Длинный \*</dt> \* \* \* \*<dt></dt></span><span class="sxs-lookup"><span data-stu-id="bef0f-115"><dt>\*\*\*\*Long\*\*\*\*</dt> <dt></dt></span></span> </dl>                                                | <span data-ttu-id="bef0f-116">Объект [**сертификата**](certificate.md) по указанному индексу в коллекции удален.</span><span class="sxs-lookup"><span data-stu-id="bef0f-116">The [**Certificate**](certificate.md) object at the specified index into the collection is removed.</span></span><br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="bef0f-117"><dt>\* \* \* \* Строка \*</dt> \* \* \* <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bef0f-117"><dt>\*\*\*\*String\*\*\*\*</dt> <dt></dt></span></span> </dl>                                        | <span data-ttu-id="bef0f-118">Первый объект [**сертификата**](certificate.md) в коллекции, соответствующий отпечатку [*SHA-1*](../secgloss/s-gly.md) , который содержится в указанной строке, удаляется.</span><span class="sxs-lookup"><span data-stu-id="bef0f-118">The first [**Certificate**](certificate.md) object in the collection that matches the [*SHA-1*](../secgloss/s-gly.md) thumbprint contained in the specified string is removed.</span></span><br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <span data-ttu-id="bef0f-119"><dt>**[**Сертификат**](certificate.md)**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="bef0f-119"><dt>**[**Certificate**](certificate.md)**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="bef0f-120">Удаляется первый объект [**сертификата**](certificate.md) в коллекции, соответствующий указанному объекту **сертификата** .</span><span class="sxs-lookup"><span data-stu-id="bef0f-120">The first [**Certificate**](certificate.md) object in the collection that matches the specified **Certificate** object is removed.</span></span><br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bef0f-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bef0f-121">Return value</span></span>

<span data-ttu-id="bef0f-122">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bef0f-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bef0f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="bef0f-123">Requirements</span></span>



| <span data-ttu-id="bef0f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="bef0f-124">Requirement</span></span> | <span data-ttu-id="bef0f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="bef0f-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bef0f-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="bef0f-126">End of client support</span></span><br/> | <span data-ttu-id="bef0f-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bef0f-127">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="bef0f-128">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="bef0f-128">End of server support</span></span><br/> | <span data-ttu-id="bef0f-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bef0f-129">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bef0f-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="bef0f-130">Redistributable</span></span><br/>       | <span data-ttu-id="bef0f-131">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="bef0f-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bef0f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bef0f-132">DLL</span></span><br/>                   | <dl> <span data-ttu-id="bef0f-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bef0f-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
