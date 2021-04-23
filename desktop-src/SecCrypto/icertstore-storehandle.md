---
description: Задает или получает маркер ХЦЕРТСТОРЕ хранилища сертификатов.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'Свойство Ицертсторе:: Сторехандле'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 86f57159a2fdd444f22593ec66fa99510a5260b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688901"
---
# <a name="icertstorestorehandle-property"></a><span data-ttu-id="b01f6-103">Свойство Ицертсторе:: Сторехандле</span><span class="sxs-lookup"><span data-stu-id="b01f6-103">ICertStore::StoreHandle property</span></span>

<span data-ttu-id="b01f6-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="b01f6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="b01f6-105">Свойство **сторехандле** задает или получает маркер хцертсторе хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="b01f6-105">The **StoreHandle** property sets or retrieves the HCERTSTORE handle of a certificate store.</span></span>

<span data-ttu-id="b01f6-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b01f6-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b01f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b01f6-107">Syntax</span></span>


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a><span data-ttu-id="b01f6-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b01f6-108">Property value</span></span>

<span data-ttu-id="b01f6-109">ХЦЕРТСТОРЕный обработчик хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="b01f6-109">The HCERTSTORE handle of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b01f6-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b01f6-110">Error codes</span></span>

<span data-ttu-id="b01f6-111">Если методы доступа к свойству **помещают \_ сторехандле** и **Get \_ Сторехандле** , они возвращают S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="b01f6-111">If the property access methods **put\_StoreHandle** and **get\_StoreHandle** succeed, they return S\_OK.</span></span>

<span data-ttu-id="b01f6-112">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="b01f6-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b01f6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b01f6-113">Remarks</span></span>

<span data-ttu-id="b01f6-114">Чтобы освободить контекст, необходимо вызвать либо метод [**CloseHandle**](icertstore-closehandle.md) , либо функцию [**цертклосесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) .</span><span class="sxs-lookup"><span data-stu-id="b01f6-114">You must call either the [**CloseHandle**](icertstore-closehandle.md) method or the [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) function to free the context.</span></span>

<span data-ttu-id="b01f6-115">Если задано свойство **сторехандле** , состояние всего объекта [**Store**](store.md) сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="b01f6-115">If you set the **StoreHandle** property, the state of the entire [**Store**](store.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="b01f6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b01f6-116">Requirements</span></span>



| <span data-ttu-id="b01f6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b01f6-117">Requirement</span></span> | <span data-ttu-id="b01f6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b01f6-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b01f6-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b01f6-119">Redistributable</span></span><br/> | <span data-ttu-id="b01f6-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="b01f6-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b01f6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b01f6-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="b01f6-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b01f6-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b01f6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b01f6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b01f6-124">**ицертсторе**</span><span class="sxs-lookup"><span data-stu-id="b01f6-124">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




