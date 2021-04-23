---
description: Возвращает объект Басикконстраинтс, представляющий расширение базовых ограничений сертификата.
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: 'Метод ICertificate2:: Басикконстраинтс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.BasicConstraints
- ICertificate2.BasicConstraints
- ICertificate.BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b511781c29d313715e7714f185dbff7e4b38f86c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669498"
---
# <a name="icertificate2basicconstraints-method"></a><span data-ttu-id="0335d-103">Метод ICertificate2:: Басикконстраинтс</span><span class="sxs-lookup"><span data-stu-id="0335d-103">ICertificate2::BasicConstraints method</span></span>

<span data-ttu-id="0335d-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0335d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0335d-105">Вместо этого используйте [**класс X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="0335d-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0335d-106">Метод **басикконстраинтс** возвращает объект [**басикконстраинтс**](basicconstraints.md) , представляющий базовое расширение ограничений сертификата.</span><span class="sxs-lookup"><span data-stu-id="0335d-106">The **BasicConstraints** method returns a [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="0335d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0335d-107">Syntax</span></span>


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a><span data-ttu-id="0335d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0335d-108">Parameters</span></span>

<span data-ttu-id="0335d-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0335d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0335d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0335d-110">Return value</span></span>

<span data-ttu-id="0335d-111">Объект [**басикконстраинтс**](basicconstraints.md) , представляющий расширение базовых ограничений сертификата.</span><span class="sxs-lookup"><span data-stu-id="0335d-111">The [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="0335d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0335d-112">Requirements</span></span>



| <span data-ttu-id="0335d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0335d-113">Requirement</span></span> | <span data-ttu-id="0335d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0335d-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0335d-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0335d-115">End of client support</span></span><br/> | <span data-ttu-id="0335d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0335d-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0335d-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0335d-117">End of server support</span></span><br/> | <span data-ttu-id="0335d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0335d-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0335d-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0335d-119">Redistributable</span></span><br/>       | <span data-ttu-id="0335d-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0335d-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0335d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0335d-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0335d-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0335d-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
