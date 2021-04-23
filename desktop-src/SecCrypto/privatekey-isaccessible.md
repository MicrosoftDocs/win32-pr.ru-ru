---
description: Возвращает логическое значение, указывающее, доступен ли закрытый ключ.
ms.assetid: ee5e89af-745e-4a4d-9943-fecbaee5d3e3
title: PrivateKey. доступный метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsAccessible
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9997fad702ab1eddbf4c60fa2304df8185ef4c63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689083"
---
# <a name="privatekeyisaccessible-method"></a><span data-ttu-id="a5b28-103">PrivateKey. доступный метод</span><span class="sxs-lookup"><span data-stu-id="a5b28-103">PrivateKey.IsAccessible method</span></span>

<span data-ttu-id="a5b28-104">\[Метод **доступный** для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a5b28-104">\[The **IsAccessible** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a5b28-105">Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a5b28-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a5b28-106">Метод с **доступом** возвращает логическое значение, указывающее, доступен ли закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="a5b28-106">The **IsAccessible** method returns a Boolean value that indicates whether the private key is accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b28-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5b28-107">Syntax</span></span>


```VB
PrivateKey.IsAccessible()
```



## <a name="parameters"></a><span data-ttu-id="a5b28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5b28-108">Parameters</span></span>

<span data-ttu-id="a5b28-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a5b28-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5b28-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5b28-110">Return value</span></span>

<span data-ttu-id="a5b28-111">Если значение — true, закрытый ключ доступен.</span><span class="sxs-lookup"><span data-stu-id="a5b28-111">If true, the private key is accessible.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b28-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5b28-112">Remarks</span></span>

<span data-ttu-id="a5b28-113">Возвращаемое значение этого метода зависит от используемого [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="a5b28-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="a5b28-114">Этот метод возвращает надежное значение, если используется Microsoft CSP.</span><span class="sxs-lookup"><span data-stu-id="a5b28-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="a5b28-115">Если CSP не является CSP Майкрософт, возвращаемое значение не может быть точным.</span><span class="sxs-lookup"><span data-stu-id="a5b28-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b28-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a5b28-116">Requirements</span></span>



| <span data-ttu-id="a5b28-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a5b28-117">Requirement</span></span> | <span data-ttu-id="a5b28-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a5b28-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b28-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="a5b28-119">Redistributable</span></span><br/> | <span data-ttu-id="a5b28-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="a5b28-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a5b28-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a5b28-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="a5b28-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5b28-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b28-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5b28-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b28-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="a5b28-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
