---
description: Возвращает имя поставщика служб шифрования (CSP).
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: PrivateKey. ProviderName, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669333"
---
# <a name="privatekeyprovidername-property"></a><span data-ttu-id="9000f-103">PrivateKey. ProviderName, свойство</span><span class="sxs-lookup"><span data-stu-id="9000f-103">PrivateKey.ProviderName property</span></span>

<span data-ttu-id="9000f-104">\[Свойство **providerName** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9000f-104">\[The **ProviderName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9000f-105">Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="9000f-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9000f-106">Свойство **providerName** извлекает имя [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="9000f-106">The **ProviderName** property retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="9000f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9000f-107">Syntax</span></span>


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a><span data-ttu-id="9000f-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9000f-108">Property value</span></span>

<span data-ttu-id="9000f-109">Строка, содержащая имя CSP.</span><span class="sxs-lookup"><span data-stu-id="9000f-109">A string that contains the name of the CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="9000f-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9000f-110">Requirements</span></span>



| <span data-ttu-id="9000f-111">Требование</span><span class="sxs-lookup"><span data-stu-id="9000f-111">Requirement</span></span> | <span data-ttu-id="9000f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9000f-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9000f-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9000f-113">Redistributable</span></span><br/> | <span data-ttu-id="9000f-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9000f-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9000f-115">DLL</span><span class="sxs-lookup"><span data-stu-id="9000f-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="9000f-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9000f-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9000f-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9000f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9000f-118">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="9000f-118">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
