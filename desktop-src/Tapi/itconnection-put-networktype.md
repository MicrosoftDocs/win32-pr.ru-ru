---
description: Метод размещения \_ нетворктипе задает тип сети.
ms.assetid: 747e3133-d103-44dc-b119-5a4cb4ed7f18
title: 'Итконнектион: метод ut_NetworkType:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e08819bcc5cb00824c8c1510d85fdcb1de186b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685317"
---
# <a name="itconnectionput_networktype-method"></a><span data-ttu-id="b0483-103">Итконнектион::p UT \_ нетворктипе метод</span><span class="sxs-lookup"><span data-stu-id="b0483-103">ITConnection::put\_NetworkType method</span></span>

<span data-ttu-id="b0483-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b0483-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b0483-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="b0483-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b0483-106">Метод **размещения \_ нетворктипе** задает тип сети.</span><span class="sxs-lookup"><span data-stu-id="b0483-106">The **put\_NetworkType** method sets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0483-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0483-107">Syntax</span></span>


```C++
HRESULT put_NetworkType(
  [in] BSTR pNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="b0483-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0483-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0483-109">*пнетворктипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0483-109">*pNetworkType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0483-110">Указатель на **строку BSTR** , содержащую тип сети.</span><span class="sxs-lookup"><span data-stu-id="b0483-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0483-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0483-111">Return value</span></span>

<span data-ttu-id="b0483-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="b0483-112">This method can return one of these values.</span></span>



| <span data-ttu-id="b0483-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b0483-113">Return code</span></span>                                                                                   | <span data-ttu-id="b0483-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b0483-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b0483-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b0483-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b0483-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="b0483-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b0483-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b0483-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b0483-118">Недопустимый параметр *пнетворктипе* .</span><span class="sxs-lookup"><span data-stu-id="b0483-118">The *pNetworkType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="b0483-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b0483-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b0483-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="b0483-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b0483-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="b0483-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b0483-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b0483-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b0483-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="b0483-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b0483-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="b0483-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b0483-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0483-125">Remarks</span></span>

<span data-ttu-id="b0483-126">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Пнетворктипе* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="b0483-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pNetworkType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0483-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b0483-127">Requirements</span></span>



| <span data-ttu-id="b0483-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b0483-128">Requirement</span></span> | <span data-ttu-id="b0483-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b0483-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0483-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="b0483-130">TAPI version</span></span><br/> | <span data-ttu-id="b0483-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b0483-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b0483-132">Header</span><span class="sxs-lookup"><span data-stu-id="b0483-132">Header</span></span><br/>       | <dl> <span data-ttu-id="b0483-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0483-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0483-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b0483-134">Library</span></span><br/>      | <dl> <span data-ttu-id="b0483-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0483-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b0483-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b0483-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="b0483-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0483-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0483-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0483-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0483-139">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="b0483-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="b0483-140">**Итконнектион:: Get \_ нетворктипе**</span><span class="sxs-lookup"><span data-stu-id="b0483-140">**ITConnection::get\_NetworkType**</span></span>](itconnection-get-networktype.md)
</dt> </dl>

 

