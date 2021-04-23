---
description: Освобождает контекст ПКЦЕРТ, \_ полученный через свойство цертконтекст.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'Метод Ицертконтекст:: Фриконтекст'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668730"
---
# <a name="icertcontextfreecontext-method"></a><span data-ttu-id="49f24-103">Метод Ицертконтекст:: Фриконтекст</span><span class="sxs-lookup"><span data-stu-id="49f24-103">ICertContext::FreeContext method</span></span>

<span data-ttu-id="49f24-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="49f24-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="49f24-105">Метод **фриконтекст** освобождает контекст пкцерт, \_ полученный через свойство [**цертконтекст**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="49f24-105">The **FreeContext** method releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="49f24-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49f24-106">Syntax</span></span>


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a><span data-ttu-id="49f24-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="49f24-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49f24-108">*пцертконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49f24-108">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49f24-109">Контекст ПКЦЕРТ \_ для освобождения.</span><span class="sxs-lookup"><span data-stu-id="49f24-109">The PCCERT\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49f24-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49f24-110">Return value</span></span>

<span data-ttu-id="49f24-111">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="49f24-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="49f24-112">Значение S \_ ОК указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="49f24-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="49f24-113">Любое другое значение указывает на сбой операции.</span><span class="sxs-lookup"><span data-stu-id="49f24-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="49f24-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49f24-114">Remarks</span></span>

<span data-ttu-id="49f24-115">Этот метод не освобождает контекст ПКЦЕРТ, \_ содержащийся в объекте [**сертификата**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="49f24-115">This method does not release the PCCERT\_CONTEXT contained within a [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="49f24-116">Он должен использоваться только для освобождения контекста ПКЦЕРТ, \_ полученного через свойство [**цертконтекст**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="49f24-116">It should be used only to release a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="49f24-117">Требования</span><span class="sxs-lookup"><span data-stu-id="49f24-117">Requirements</span></span>



| <span data-ttu-id="49f24-118">Требование</span><span class="sxs-lookup"><span data-stu-id="49f24-118">Requirement</span></span> | <span data-ttu-id="49f24-119">Значение</span><span class="sxs-lookup"><span data-stu-id="49f24-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49f24-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="49f24-120">Redistributable</span></span><br/> | <span data-ttu-id="49f24-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="49f24-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="49f24-122">DLL</span><span class="sxs-lookup"><span data-stu-id="49f24-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="49f24-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49f24-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49f24-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49f24-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49f24-125">**ицертконтекст**</span><span class="sxs-lookup"><span data-stu-id="49f24-125">**ICertContext**</span></span>](icertcontext.md)
</dt> </dl>

 

 




