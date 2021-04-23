---
description: Задает или получает расположение CAPICOM \_ \_ -хранилища для хранилища сертификатов.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'Свойство Ицертсторе:: StoreLocation'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668589"
---
# <a name="icertstorestorelocation-property"></a><span data-ttu-id="ccfe0-103">Свойство Ицертсторе:: StoreLocation</span><span class="sxs-lookup"><span data-stu-id="ccfe0-103">ICertStore::StoreLocation property</span></span>

<span data-ttu-id="ccfe0-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="ccfe0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="ccfe0-105">Свойство **StoreLocation** задает или получает [**Расположение CAPICOM- \_ хранилища \_**](capicom-store-location.md) для хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ccfe0-105">The **StoreLocation** property sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span>

<span data-ttu-id="ccfe0-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ccfe0-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccfe0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccfe0-107">Syntax</span></span>


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="ccfe0-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ccfe0-108">Property value</span></span>

<span data-ttu-id="ccfe0-109">Расположение хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ccfe0-109">The location of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ccfe0-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="ccfe0-110">Error codes</span></span>

<span data-ttu-id="ccfe0-111">Если методы доступа к свойству **помещают \_ StoreLocation** и **Get \_ StoreLocation** , они возвращают S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ccfe0-111">If the property access methods **put\_StoreLocation** and **get\_StoreLocation** succeed, they return S\_OK.</span></span>

<span data-ttu-id="ccfe0-112">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="ccfe0-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccfe0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ccfe0-113">Requirements</span></span>



| <span data-ttu-id="ccfe0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ccfe0-114">Requirement</span></span> | <span data-ttu-id="ccfe0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ccfe0-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccfe0-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ccfe0-116">Redistributable</span></span><br/> | <span data-ttu-id="ccfe0-117">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccfe0-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ccfe0-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ccfe0-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="ccfe0-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccfe0-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccfe0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccfe0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccfe0-121">**ицертсторе**</span><span class="sxs-lookup"><span data-stu-id="ccfe0-121">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




