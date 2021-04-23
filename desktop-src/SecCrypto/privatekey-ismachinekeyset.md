---
description: Возвращает логическое значение, указывающее, принадлежит ли закрытый ключ к набору ключей компьютера.
ms.assetid: ea13ba68-30ae-4aa4-b490-29fd4542c621
title: PrivateKey. Исмачинекэйсет, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsMachineKeyset
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a42e3f932b8294d9671b7901437151d9fbbe5a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689514"
---
# <a name="privatekeyismachinekeyset-method"></a><span data-ttu-id="87f5c-103">PrivateKey. Исмачинекэйсет, метод</span><span class="sxs-lookup"><span data-stu-id="87f5c-103">PrivateKey.IsMachineKeyset method</span></span>

<span data-ttu-id="87f5c-104">\[Метод **исмачинекэйсет** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="87f5c-104">\[The **IsMachineKeyset** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="87f5c-105">Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="87f5c-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="87f5c-106">Метод **исмачинекэйсет** возвращает логическое значение, указывающее, принадлежит ли закрытый ключ к набору ключей компьютера.</span><span class="sxs-lookup"><span data-stu-id="87f5c-106">The **IsMachineKeyset** method returns a Boolean value that indicates whether the private key belongs to a machine key set.</span></span>

## <a name="syntax"></a><span data-ttu-id="87f5c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87f5c-107">Syntax</span></span>


```VB
PrivateKey.IsMachineKeyset()
```



## <a name="parameters"></a><span data-ttu-id="87f5c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="87f5c-108">Parameters</span></span>

<span data-ttu-id="87f5c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="87f5c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87f5c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87f5c-110">Return value</span></span>

<span data-ttu-id="87f5c-111">Если значение — true, закрытый ключ принадлежит набору ключей компьютера.</span><span class="sxs-lookup"><span data-stu-id="87f5c-111">If true, the private key belongs to a machine key set.</span></span>

## <a name="remarks"></a><span data-ttu-id="87f5c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87f5c-112">Remarks</span></span>

<span data-ttu-id="87f5c-113">Возвращаемое значение этого метода зависит от используемого [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="87f5c-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="87f5c-114">Этот метод возвращает надежное значение, если используется Microsoft CSP.</span><span class="sxs-lookup"><span data-stu-id="87f5c-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="87f5c-115">Если CSP не является CSP Майкрософт, возвращаемое значение не может быть точным.</span><span class="sxs-lookup"><span data-stu-id="87f5c-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f5c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="87f5c-116">Requirements</span></span>



| <span data-ttu-id="87f5c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="87f5c-117">Requirement</span></span> | <span data-ttu-id="87f5c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="87f5c-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87f5c-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="87f5c-119">Redistributable</span></span><br/> | <span data-ttu-id="87f5c-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="87f5c-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="87f5c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="87f5c-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="87f5c-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87f5c-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87f5c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87f5c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87f5c-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="87f5c-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
