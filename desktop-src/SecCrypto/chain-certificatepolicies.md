---
description: Возвращает коллекцию OID, которая представляет идентификатор объекта политики сертификата, допустимый для цепочки.
ms.assetid: 18200003-f4f1-4cf3-af9a-bc223151ff68
title: 'Метод IChain2:: ЦертификатеполиЦиес'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.CertificatePolicies
- IChain2.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e37abce9ea1aec5eb8adaf1d8eceeb3fac284fa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685040"
---
# <a name="ichain2certificatepolicies-method"></a><span data-ttu-id="a9fea-103">Метод IChain2:: ЦертификатеполиЦиес</span><span class="sxs-lookup"><span data-stu-id="a9fea-103">IChain2::CertificatePolicies method</span></span>

<span data-ttu-id="a9fea-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a9fea-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a9fea-105">Вместо этого используйте [**класс X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a9fea-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a9fea-106">Метод **цертификатеполиЦиес** Возвращает коллекцию [**OID**](oids.md) , которая представляет идентификатор объекта (OID) политики сертификата, допустимый для цепочки.</span><span class="sxs-lookup"><span data-stu-id="a9fea-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9fea-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9fea-107">Syntax</span></span>


```VB
Chain.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="a9fea-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9fea-108">Parameters</span></span>

<span data-ttu-id="a9fea-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a9fea-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9fea-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a9fea-110">Requirements</span></span>



| <span data-ttu-id="a9fea-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a9fea-111">Requirement</span></span> | <span data-ttu-id="a9fea-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a9fea-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9fea-113">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a9fea-113">End of client support</span></span><br/> | <span data-ttu-id="a9fea-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9fea-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a9fea-115">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a9fea-115">End of server support</span></span><br/> | <span data-ttu-id="a9fea-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9fea-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a9fea-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a9fea-117">Redistributable</span></span><br/>       | <span data-ttu-id="a9fea-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9fea-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a9fea-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a9fea-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a9fea-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9fea-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
