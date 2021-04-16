---
description: Закрывает обработчик ХЦЕРТСТОРЕ, полученный через свойство Сторехандле.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'Метод Ицертсторе:: CloseHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669519"
---
# <a name="icertstoreclosehandle-method"></a><span data-ttu-id="beb5d-103">Метод Ицертсторе:: CloseHandle</span><span class="sxs-lookup"><span data-stu-id="beb5d-103">ICertStore::CloseHandle method</span></span>

<span data-ttu-id="beb5d-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="beb5d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="beb5d-105">Метод **CloseHandle** закрывает обработчик хцертсторе, полученный через свойство [**сторехандле**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="beb5d-105">The **CloseHandle** method closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb5d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="beb5d-106">Syntax</span></span>


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a><span data-ttu-id="beb5d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="beb5d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb5d-108">*хцертсторе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="beb5d-108">*hCertStore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb5d-109">Закрываемый обработчик ХЦЕРТСТОРЕ.</span><span class="sxs-lookup"><span data-stu-id="beb5d-109">The HCERTSTORE handle to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb5d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="beb5d-110">Return value</span></span>

<span data-ttu-id="beb5d-111">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="beb5d-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="beb5d-112">Значение **S \_ ОК** указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="beb5d-112">A value of **S\_OK** indicates success.</span></span> <span data-ttu-id="beb5d-113">Любое другое значение указывает на сбой операции.</span><span class="sxs-lookup"><span data-stu-id="beb5d-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="beb5d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="beb5d-114">Remarks</span></span>

<span data-ttu-id="beb5d-115">Этот метод не освобождает обработчик ХЦЕРТСТОРЕ, содержащийся в объекте [**Store**](store.md) .</span><span class="sxs-lookup"><span data-stu-id="beb5d-115">This method does not release the HCERTSTORE handle contained within a [**Store**](store.md) object.</span></span> <span data-ttu-id="beb5d-116">Он должен использоваться только для освобождения обработчика ХЦЕРТСТОРЕ, полученного через свойство [**сторехандле**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="beb5d-116">It should be used only to release a HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="beb5d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="beb5d-117">Requirements</span></span>



| <span data-ttu-id="beb5d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="beb5d-118">Requirement</span></span> | <span data-ttu-id="beb5d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="beb5d-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="beb5d-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="beb5d-120">Redistributable</span></span><br/> | <span data-ttu-id="beb5d-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="beb5d-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="beb5d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="beb5d-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="beb5d-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beb5d-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb5d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="beb5d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb5d-125">**ицертсторе**</span><span class="sxs-lookup"><span data-stu-id="beb5d-125">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




