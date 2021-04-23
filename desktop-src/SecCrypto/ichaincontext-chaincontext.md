---
description: Задает или получает \_ контекст цепочки пкцерт \_ сертификата.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'Свойство Ичаинконтекст:: Чаинконтекст'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36b2f6f5811c844e4e43544f5b56b8de66cb3bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685124"
---
# <a name="ichaincontextchaincontext-property"></a><span data-ttu-id="10fac-103">Свойство Ичаинконтекст:: Чаинконтекст</span><span class="sxs-lookup"><span data-stu-id="10fac-103">IChainContext::ChainContext property</span></span>

<span data-ttu-id="10fac-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="10fac-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="10fac-105">Свойство **чаинконтекст** задает или получает \_ контекст цепочки пкцерт \_ сертификата.</span><span class="sxs-lookup"><span data-stu-id="10fac-105">The **ChainContext** property sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span>

<span data-ttu-id="10fac-106">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="10fac-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="10fac-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10fac-107">Syntax</span></span>


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a><span data-ttu-id="10fac-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="10fac-108">Property value</span></span>

<span data-ttu-id="10fac-109">\_Контекст цепочки пкцерт \_ сертификата.</span><span class="sxs-lookup"><span data-stu-id="10fac-109">The PCCERT\_CHAIN\_CONTEXT of the certificate.</span></span>

## <a name="error-codes"></a><span data-ttu-id="10fac-110">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="10fac-110">Error codes</span></span>

<span data-ttu-id="10fac-111">Если методы доступа к свойству **помещают \_ чаинконтекст** и **Get \_ Чаинконтекст** , они возвращают S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="10fac-111">If the property access methods **put\_ChainContext** and **get\_ChainContext** succeed, they return S\_OK.</span></span>

<span data-ttu-id="10fac-112">Любое другое значение **HRESULT** указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="10fac-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="10fac-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10fac-113">Remarks</span></span>

<span data-ttu-id="10fac-114">Чтобы освободить контекст, необходимо вызвать метод [**фриконтекст**](ichaincontext-freecontext.md) или функцию [**цертфрицертификатечаин**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) .</span><span class="sxs-lookup"><span data-stu-id="10fac-114">You must call either the [**FreeContext**](ichaincontext-freecontext.md) method or the [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) function to free the context.</span></span>

<span data-ttu-id="10fac-115">Если задано свойство **чаинконтекст** , то состояние всего объекта [**цепочки**](chain.md) сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="10fac-115">If you set the **ChainContext** property, the state of the entire [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="10fac-116">Требования</span><span class="sxs-lookup"><span data-stu-id="10fac-116">Requirements</span></span>



| <span data-ttu-id="10fac-117">Требование</span><span class="sxs-lookup"><span data-stu-id="10fac-117">Requirement</span></span> | <span data-ttu-id="10fac-118">Значение</span><span class="sxs-lookup"><span data-stu-id="10fac-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10fac-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="10fac-119">Redistributable</span></span><br/> | <span data-ttu-id="10fac-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="10fac-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="10fac-121">DLL</span><span class="sxs-lookup"><span data-stu-id="10fac-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="10fac-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10fac-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fac-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10fac-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fac-124">**ичаинконтекст**</span><span class="sxs-lookup"><span data-stu-id="10fac-124">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




