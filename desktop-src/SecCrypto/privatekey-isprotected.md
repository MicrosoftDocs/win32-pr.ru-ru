---
description: Возвращает логическое значение, указывающее, защищен ли закрытый ключ.
ms.assetid: 6a329581-0ff8-45fa-9997-5fcf043287cb
title: PrivateKey. с защитным методом
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsProtected
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 33ba72935b2c3f9f9cf537469e043160f9ce2d7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668974"
---
# <a name="privatekeyisprotected-method"></a><span data-ttu-id="2e7f6-103">PrivateKey. с защитным методом</span><span class="sxs-lookup"><span data-stu-id="2e7f6-103">PrivateKey.IsProtected method</span></span>

<span data-ttu-id="2e7f6-104">\[Метод «с **защитой** » доступен для использования в операционных системах, указанных в разделе «требования».</span><span class="sxs-lookup"><span data-stu-id="2e7f6-104">\[The **IsProtected** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2e7f6-105">Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2e7f6-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2e7f6-106">Метод «с **защитой** » возвращает логическое значение, указывающее, защищен ли закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-106">The **IsProtected** method returns a Boolean value that indicates whether the private key is protected.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e7f6-107">Syntax</span></span>


```VB
PrivateKey.IsProtected()
```



## <a name="parameters"></a><span data-ttu-id="2e7f6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e7f6-108">Parameters</span></span>

<span data-ttu-id="2e7f6-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e7f6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e7f6-110">Return value</span></span>

<span data-ttu-id="2e7f6-111">Если значение — true, закрытый ключ защищен.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-111">If true, the private key is protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e7f6-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e7f6-112">Remarks</span></span>

<span data-ttu-id="2e7f6-113">Возвращаемое значение этого метода зависит от используемого [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="2e7f6-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="2e7f6-114">Этот метод возвращает надежное значение, если используется Microsoft CSP.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="2e7f6-115">Если CSP не является CSP Майкрософт, возвращаемое значение не может быть точным.</span><span class="sxs-lookup"><span data-stu-id="2e7f6-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e7f6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2e7f6-116">Requirements</span></span>



| <span data-ttu-id="2e7f6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2e7f6-117">Requirement</span></span> | <span data-ttu-id="2e7f6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2e7f6-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7f6-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2e7f6-119">Redistributable</span></span><br/> | <span data-ttu-id="2e7f6-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e7f6-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2e7f6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2e7f6-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="2e7f6-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e7f6-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e7f6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e7f6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7f6-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="2e7f6-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
