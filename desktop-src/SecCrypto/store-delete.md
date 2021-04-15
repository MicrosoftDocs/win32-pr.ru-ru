---
description: Удаляет хранилище сертификатов, представленное текущим объектом хранилища.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Метод Store. Delete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649123"
---
# <a name="storedelete-method"></a><span data-ttu-id="af643-103">Метод Store. Delete</span><span class="sxs-lookup"><span data-stu-id="af643-103">Store.Delete method</span></span>

<span data-ttu-id="af643-104">\[Метод **Delete** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="af643-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af643-105">Вместо этого используйте [**класс X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="af643-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="af643-106">Метод **Delete** удаляет [*хранилище сертификатов*](../secgloss/c-gly.md) , представленное текущим объектом [**хранилища**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="af643-106">The **Delete** method deletes the [*certificate store*](../secgloss/c-gly.md) that is represented by the current [**Store**](certificate.md) object.</span></span> <span data-ttu-id="af643-107">Этот метод удаляет только несистемные хранилища.</span><span class="sxs-lookup"><span data-stu-id="af643-107">This method deletes only nonsystem stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="af643-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af643-108">Syntax</span></span>


```VB
Store.Delete()
```



## <a name="parameters"></a><span data-ttu-id="af643-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="af643-109">Parameters</span></span>

<span data-ttu-id="af643-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="af643-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af643-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af643-111">Return value</span></span>

<span data-ttu-id="af643-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="af643-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af643-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af643-113">Remarks</span></span>

<span data-ttu-id="af643-114">Следующие хранилища являются системными хранилищами и не могут быть удалены:</span><span class="sxs-lookup"><span data-stu-id="af643-114">The following stores are system stores and cannot be deleted:</span></span>

-   <span data-ttu-id="af643-115">My</span><span class="sxs-lookup"><span data-stu-id="af643-115">My</span></span>
-   <span data-ttu-id="af643-116">Root</span><span class="sxs-lookup"><span data-stu-id="af643-116">Root</span></span>
-   <span data-ttu-id="af643-117">Доверие</span><span class="sxs-lookup"><span data-stu-id="af643-117">Trust</span></span>
-   <span data-ttu-id="af643-118">Целостности и доступности</span><span class="sxs-lookup"><span data-stu-id="af643-118">CA</span></span>
-   <span data-ttu-id="af643-119">усердс</span><span class="sxs-lookup"><span data-stu-id="af643-119">UserDS</span></span>
-   <span data-ttu-id="af643-120">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="af643-120">TrustedPublisher</span></span>
-   <span data-ttu-id="af643-121">Запрещено</span><span class="sxs-lookup"><span data-stu-id="af643-121">Disallowed</span></span>
-   <span data-ttu-id="af643-122">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="af643-122">AuthRoot</span></span>
-   <span data-ttu-id="af643-123">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="af643-123">TrustedPeople</span></span>

<span data-ttu-id="af643-124">Метод **Delete** возвращает ошибку, если вызывается из веб-скрипта.</span><span class="sxs-lookup"><span data-stu-id="af643-124">The **Delete** method returns an error if called from a web script.</span></span>

## <a name="requirements"></a><span data-ttu-id="af643-125">Требования</span><span class="sxs-lookup"><span data-stu-id="af643-125">Requirements</span></span>



| <span data-ttu-id="af643-126">Требование</span><span class="sxs-lookup"><span data-stu-id="af643-126">Requirement</span></span> | <span data-ttu-id="af643-127">Значение</span><span class="sxs-lookup"><span data-stu-id="af643-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af643-128">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="af643-128">Redistributable</span></span><br/> | <span data-ttu-id="af643-129">CAPICOM 2,1 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="af643-129">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="af643-130">DLL</span><span class="sxs-lookup"><span data-stu-id="af643-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="af643-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af643-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af643-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af643-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af643-133">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="af643-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="af643-134">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="af643-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
