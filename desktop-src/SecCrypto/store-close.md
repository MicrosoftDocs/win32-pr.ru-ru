---
description: Закрывает открытое хранилище сертификатов.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Метод Store. Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669139"
---
# <a name="storeclose-method"></a><span data-ttu-id="d7b05-103">Метод Store. Close</span><span class="sxs-lookup"><span data-stu-id="d7b05-103">Store.Close method</span></span>

<span data-ttu-id="d7b05-104">\[Метод **Close** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d7b05-104">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d7b05-105">Вместо этого используйте [**класс X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d7b05-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d7b05-106">Метод **Close** закрывает открытое [*хранилище сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d7b05-106">The **Close** method closes an open [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b05-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7b05-107">Syntax</span></span>


```VB
Store.Close()
```



## <a name="parameters"></a><span data-ttu-id="d7b05-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7b05-108">Parameters</span></span>

<span data-ttu-id="d7b05-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d7b05-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7b05-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7b05-110">Return value</span></span>

<span data-ttu-id="d7b05-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d7b05-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7b05-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7b05-112">Remarks</span></span>

<span data-ttu-id="d7b05-113">После вызова метода **Close** объект [**Store**](store.md) уничтожается.</span><span class="sxs-lookup"><span data-stu-id="d7b05-113">After the **Close** method is called, the [**Store**](store.md) object is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7b05-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d7b05-114">Requirements</span></span>



| <span data-ttu-id="d7b05-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d7b05-115">Requirement</span></span> | <span data-ttu-id="d7b05-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d7b05-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b05-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d7b05-117">Redistributable</span></span><br/> | <span data-ttu-id="d7b05-118">CAPICOM 2,1 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7b05-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d7b05-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d7b05-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="d7b05-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7b05-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7b05-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7b05-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b05-122">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="d7b05-122">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="d7b05-123">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="d7b05-123">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="d7b05-124">**Открыт**</span><span class="sxs-lookup"><span data-stu-id="d7b05-124">**Open**</span></span>](store-open.md)
</dt> </dl>

 

 
