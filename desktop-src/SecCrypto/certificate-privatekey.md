---
description: Задает или получает закрытый ключ, связанный с сертификатом.
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Свойство Certificate. PrivateKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669517"
---
# <a name="certificateprivatekey-property"></a><span data-ttu-id="58b72-103">Свойство Certificate. PrivateKey</span><span class="sxs-lookup"><span data-stu-id="58b72-103">Certificate.PrivateKey property</span></span>

<span data-ttu-id="58b72-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="58b72-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="58b72-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="58b72-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="58b72-106">Свойство **PrivateKey** задает или получает закрытый ключ, связанный с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="58b72-106">The **PrivateKey** property sets or retrieves the private key associated with the certificate.</span></span> <span data-ttu-id="58b72-107">Это свойство было представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="58b72-107">This property was introduced in CAPICOM 2.0.</span></span>

<span data-ttu-id="58b72-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="58b72-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="58b72-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58b72-109">Syntax</span></span>


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a><span data-ttu-id="58b72-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="58b72-110">Property value</span></span>

<span data-ttu-id="58b72-111">Объект [**PrivateKey**](privatekey.md) , представляющий закрытый ключ, связанный с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="58b72-111">A [**PrivateKey**](privatekey.md) object that represents the private key that is associated with the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="58b72-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58b72-112">Remarks</span></span>

<span data-ttu-id="58b72-113">Если задать для свойства **PrivateKey** значение Nothing, связь между закрытым ключом и сертификатом будет удалена, но закрытый ключ не будет удален.</span><span class="sxs-lookup"><span data-stu-id="58b72-113">Setting the **PrivateKey** property to Nothing removes the association between the private key and the certificate, but it does not delete the private key.</span></span> <span data-ttu-id="58b72-114">Чтобы удалить закрытый ключ, вызовите метод [**PrivateKey. Delete**](privatekey-delete.md) , а затем установите для этого свойства значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="58b72-114">To delete the private key, call the [**PrivateKey.Delete**](privatekey-delete.md) method, and then set this property to Nothing.</span></span>

<span data-ttu-id="58b72-115">Это свойство вызывает CAPICOM \_ E \_ не \_ разрешено, если оно задано из веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="58b72-115">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is set from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="58b72-116">Требования</span><span class="sxs-lookup"><span data-stu-id="58b72-116">Requirements</span></span>



| <span data-ttu-id="58b72-117">Требование</span><span class="sxs-lookup"><span data-stu-id="58b72-117">Requirement</span></span> | <span data-ttu-id="58b72-118">Значение</span><span class="sxs-lookup"><span data-stu-id="58b72-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58b72-119">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="58b72-119">End of client support</span></span><br/> | <span data-ttu-id="58b72-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58b72-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="58b72-121">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="58b72-121">End of server support</span></span><br/> | <span data-ttu-id="58b72-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58b72-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="58b72-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="58b72-123">Redistributable</span></span><br/>       | <span data-ttu-id="58b72-124">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="58b72-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="58b72-125">DLL</span><span class="sxs-lookup"><span data-stu-id="58b72-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="58b72-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58b72-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58b72-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58b72-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b72-128">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="58b72-128">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
