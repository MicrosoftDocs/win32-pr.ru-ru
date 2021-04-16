---
description: Метод Доинитиализе должен быть реализован монитором. МКСВК вызывает этот метод для получения фильтра записи непосредственно перед вызовом метода НППС Ирткконнект.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Метод Имонитордоинитиализе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540178"
---
# <a name="imonitordoinitialize-method"></a><span data-ttu-id="b2460-104">Имонитор: метод:D Оинитиализе</span><span class="sxs-lookup"><span data-stu-id="b2460-104">IMonitor::DoInitialize method</span></span>

<span data-ttu-id="b2460-105">Метод **доинитиализе** должен быть реализован монитором.</span><span class="sxs-lookup"><span data-stu-id="b2460-105">The **DoInitialize** method must be implemented by the monitor.</span></span> <span data-ttu-id="b2460-106">МКСВК вызывает этот метод для получения фильтра записи непосредственно перед вызовом метода [ИРТК:: Connect](irtc-connect.md) НПП.</span><span class="sxs-lookup"><span data-stu-id="b2460-106">The MCSVC calls this method to obtain a capture filter immediately before calling the NPP's [IRTC::Connect](irtc-connect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2460-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2460-107">Syntax</span></span>


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a><span data-ttu-id="b2460-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2460-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2460-109">*пункмониторктрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b2460-109">*pUnkMonitorCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2460-110">Указатель [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , переданный мксвк.</span><span class="sxs-lookup"><span data-stu-id="b2460-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer passed in by the MCSVC.</span></span> <span data-ttu-id="b2460-111">Чтобы получить поддерживаемый интерфейс управления монитором, монитор должен вызвать метод [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе.</span><span class="sxs-lookup"><span data-stu-id="b2460-111">To obtain a supported monitor control interface, the monitor must call [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer.</span></span>

</dd> <dt>

<span data-ttu-id="b2460-112">*хнппблоб* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b2460-112">*hNPPBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2460-113">На входе — маркер для большого двоичного объекта НПП.</span><span class="sxs-lookup"><span data-stu-id="b2460-113">On input, a handle to an NPP BLOB.</span></span>

<span data-ttu-id="b2460-114">На выходе — большой двоичный объект НПП, содержащий фильтр записи.</span><span class="sxs-lookup"><span data-stu-id="b2460-114">On output, an NPP BLOB that contains a capture filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2460-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2460-115">Return value</span></span>

<span data-ttu-id="b2460-116">Если метод выполнен успешно, возвращается значение S \_ OK (то же самое, что и ошибка).</span><span class="sxs-lookup"><span data-stu-id="b2460-116">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="b2460-117">Если метод завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="b2460-117">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="b2460-118">При возникновении ошибки МКСВК не создаст монитор или вызовите метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) на указатель интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b2460-118">On error, the MCSVC will not create the monitor or call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2460-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2460-119">Remarks</span></span>

<span data-ttu-id="b2460-120">МКСВК вызывает метод **доинитиализе** для выполнения любой необходимой инициализации монитора.</span><span class="sxs-lookup"><span data-stu-id="b2460-120">The MCSVC calls the **DoInitialize** method to perform any required monitor initialization.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2460-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b2460-121">Requirements</span></span>



| <span data-ttu-id="b2460-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b2460-122">Requirement</span></span> | <span data-ttu-id="b2460-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b2460-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b2460-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2460-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b2460-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2460-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b2460-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2460-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b2460-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b2460-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b2460-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b2460-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2460-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2460-129"><dt>Netmon.h</dt></span></span> </dl> |



 

