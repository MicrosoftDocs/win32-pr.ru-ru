---
description: Задает или получает контекст ПКЦЕРТ \_ сертификата.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'Свойство Ицертконтекст:: Цертконтекст'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668728"
---
# <a name="icertcontextcertcontext-property"></a><span data-ttu-id="6e0ba-103">Свойство Ицертконтекст:: Цертконтекст</span><span class="sxs-lookup"><span data-stu-id="6e0ba-103">ICertContext::CertContext property</span></span>

<span data-ttu-id="6e0ba-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="6e0ba-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="6e0ba-105">Свойство **цертконтекст** задает или получает \_ контекст пкцерт сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e0ba-105">The **CertContext** property sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="6e0ba-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6e0ba-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0ba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e0ba-107">Syntax</span></span>


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a><span data-ttu-id="6e0ba-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6e0ba-108">Property value</span></span>

<span data-ttu-id="6e0ba-109">Контекст ПКЦЕРТ \_ сертификата.</span><span class="sxs-lookup"><span data-stu-id="6e0ba-109">The PCCERT\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6e0ba-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6e0ba-110">Error codes</span></span>

<span data-ttu-id="6e0ba-111">Если методы доступа к свойству **помещают \_ цертконтекст** и **Get \_ Цертконтекст** , они возвращают S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6e0ba-111">If the property access methods **put\_CertContext** and **get\_CertContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="6e0ba-112">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="6e0ba-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e0ba-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e0ba-113">Remarks</span></span>

<span data-ttu-id="6e0ba-114">Чтобы освободить контекст, необходимо вызвать метод [**фриконтекст**](icertcontext-freecontext.md) или функцию [**цертфрицертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) .</span><span class="sxs-lookup"><span data-stu-id="6e0ba-114">You must call either the [**FreeContext**](icertcontext-freecontext.md) method or the [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) function to free the context.</span></span>

<span data-ttu-id="6e0ba-115">Если задано свойство **цертконтекст** , состояние всего объекта [**сертификата**](certificate.md) сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="6e0ba-115">If you set the **CertContext** property, the state of the entire [**Certificate**](certificate.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0ba-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6e0ba-116">Requirements</span></span>



| <span data-ttu-id="6e0ba-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6e0ba-117">Requirement</span></span> | <span data-ttu-id="6e0ba-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6e0ba-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0ba-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6e0ba-119">Redistributable</span></span><br/> | <span data-ttu-id="6e0ba-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="6e0ba-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6e0ba-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6e0ba-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="6e0ba-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e0ba-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e0ba-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e0ba-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0ba-124">**ицертконтекст**</span><span class="sxs-lookup"><span data-stu-id="6e0ba-124">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




