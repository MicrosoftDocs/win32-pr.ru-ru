---
description: Удаляет контейнер закрытого ключа, на который ссылается объект PrivateKey.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: PrivateKey. Delete, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665293"
---
# <a name="privatekeydelete-method"></a><span data-ttu-id="08a0b-103">PrivateKey. Delete, метод</span><span class="sxs-lookup"><span data-stu-id="08a0b-103">PrivateKey.Delete method</span></span>

<span data-ttu-id="08a0b-104">\[Метод **Delete** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="08a0b-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="08a0b-105">Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="08a0b-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="08a0b-106">Метод **Delete** удаляет контейнер закрытого ключа, на который ссылается объект [**PrivateKey**](privatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="08a0b-106">The **Delete** method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a0b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08a0b-107">Syntax</span></span>


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a><span data-ttu-id="08a0b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="08a0b-108">Parameters</span></span>

<span data-ttu-id="08a0b-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="08a0b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08a0b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08a0b-110">Return value</span></span>

<span data-ttu-id="08a0b-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="08a0b-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a0b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08a0b-112">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08a0b-113">Этот метод удаляет контейнер закрытого ключа, на который ссылается объект [**PrivateKey**](privatekey.md) , а также все закрытые ключи в контейнере.</span><span class="sxs-lookup"><span data-stu-id="08a0b-113">This method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object as well as all private keys in the container.</span></span> <span data-ttu-id="08a0b-114">Все данные, зашифрованные с помощью открытых ключей, соответствующих удаленным закрытым ключам, больше не смогут быть расшифрованы.</span><span class="sxs-lookup"><span data-stu-id="08a0b-114">Anything encrypted using the public keys corresponding to the deleted private keys will no longer be able to be decrypted.</span></span>

 

<span data-ttu-id="08a0b-115">Этот метод вызывает CAPICOM \_ E \_ не \_ разрешен при создании скрипта из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="08a0b-115">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a0b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="08a0b-116">Requirements</span></span>



| <span data-ttu-id="08a0b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="08a0b-117">Requirement</span></span> | <span data-ttu-id="08a0b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="08a0b-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08a0b-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="08a0b-119">Redistributable</span></span><br/> | <span data-ttu-id="08a0b-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="08a0b-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08a0b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="08a0b-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="08a0b-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a0b-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
