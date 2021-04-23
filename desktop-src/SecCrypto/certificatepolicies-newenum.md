---
description: '\_Свойство NewEnum объекта цертификатеполиЦиес Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции.'
ms.assetid: 631a11c8-4442-493e-9406-bc63f79db548
title: CertificatePolicies._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2d5e90d4b906661119936ca1e893e3b6e17c9bf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689011"
---
# <a name="certificatepolicies_newenum-property"></a><span data-ttu-id="e0526-103">ЦертификатеполиЦиес. \_ Свойство NewEnum</span><span class="sxs-lookup"><span data-stu-id="e0526-103">CertificatePolicies.\_NewEnum property</span></span>

<span data-ttu-id="e0526-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0526-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e0526-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для получения политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="e0526-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="e0526-106">Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="e0526-106">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e0526-107">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e0526-107">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0526-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0526-108">Syntax</span></span>


```VB
CertificatePolicies._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="e0526-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e0526-109">Property value</span></span>

<span data-ttu-id="e0526-110">Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="e0526-110">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0526-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0526-111">Remarks</span></span>

<span data-ttu-id="e0526-112">Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e0526-112">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0526-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e0526-113">Requirements</span></span>



| <span data-ttu-id="e0526-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e0526-114">Requirement</span></span> | <span data-ttu-id="e0526-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e0526-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0526-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e0526-116">End of client support</span></span><br/> | <span data-ttu-id="e0526-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0526-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e0526-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e0526-118">End of server support</span></span><br/> | <span data-ttu-id="e0526-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0526-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e0526-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e0526-120">Redistributable</span></span><br/>       | <span data-ttu-id="e0526-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0526-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e0526-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e0526-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e0526-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0526-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
