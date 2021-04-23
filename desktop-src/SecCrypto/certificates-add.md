---
description: Добавляет объект сертификата в коллекцию.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'Метод ICertificates2:: Add'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d56120c6f584e828c3aadca037d75263d5350f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668951"
---
# <a name="icertificates2add-method"></a><span data-ttu-id="c7433-103">Метод ICertificates2:: Add</span><span class="sxs-lookup"><span data-stu-id="c7433-103">ICertificates2::Add method</span></span>

<span data-ttu-id="c7433-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c7433-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c7433-105">Вместо этого используйте [**класс X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c7433-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c7433-106">Метод **Add** добавляет объект [**сертификата**](certificate.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="c7433-106">The **Add** method adds a [**Certificate**](certificate.md) object to the collection.</span></span> <span data-ttu-id="c7433-107">Этот метод появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="c7433-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7433-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7433-108">Syntax</span></span>


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="c7433-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7433-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7433-110">*Сертификат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7433-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7433-111">Объект [**сертификата**](certificate.md) , добавляемый в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="c7433-111">The [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7433-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7433-112">Return value</span></span>

<span data-ttu-id="c7433-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c7433-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7433-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c7433-114">Requirements</span></span>



| <span data-ttu-id="c7433-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c7433-115">Requirement</span></span> | <span data-ttu-id="c7433-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c7433-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7433-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c7433-117">End of client support</span></span><br/> | <span data-ttu-id="c7433-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7433-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c7433-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c7433-119">End of server support</span></span><br/> | <span data-ttu-id="c7433-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7433-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c7433-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c7433-121">Redistributable</span></span><br/>       | <span data-ttu-id="c7433-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7433-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c7433-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c7433-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c7433-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7433-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
