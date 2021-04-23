---
description: Метод Сетаддрессинфо задает сведения об адресе.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'Метод Итконнектион:: Сетаддрессинфо (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685316"
---
# <a name="itconnectionsetaddressinfo-method"></a><span data-ttu-id="11bc1-103">Метод Итконнектион:: Сетаддрессинфо</span><span class="sxs-lookup"><span data-stu-id="11bc1-103">ITConnection::SetAddressInfo method</span></span>

<span data-ttu-id="11bc1-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="11bc1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="11bc1-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="11bc1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="11bc1-106">Метод **сетаддрессинфо** задает сведения об адресе.</span><span class="sxs-lookup"><span data-stu-id="11bc1-106">The **SetAddressInfo** method sets the address information.</span></span>

## <a name="syntax"></a><span data-ttu-id="11bc1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11bc1-107">Syntax</span></span>


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a><span data-ttu-id="11bc1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11bc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11bc1-109">*пстартаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11bc1-109">*pStartAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11bc1-110">Указатель на **строку BSTR** , содержащую начальный адрес.</span><span class="sxs-lookup"><span data-stu-id="11bc1-110">Pointer to a **BSTR** containing the start address.</span></span>

</dd> <dt>

<span data-ttu-id="11bc1-111">*Нумаддрессес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11bc1-111">*NumAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11bc1-112">Число адресов, используемых для сеанса.</span><span class="sxs-lookup"><span data-stu-id="11bc1-112">Number of addresses to be used for the session.</span></span>

</dd> <dt>

<span data-ttu-id="11bc1-113">*Срок жизни* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="11bc1-113">*Ttl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11bc1-114">[*срок жизни (TTL*](t-tapgloss.md) ) для передачи данных по адресам.</span><span class="sxs-lookup"><span data-stu-id="11bc1-114">[*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11bc1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11bc1-115">Return value</span></span>

<span data-ttu-id="11bc1-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="11bc1-116">This method can return one of these values.</span></span>



| <span data-ttu-id="11bc1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="11bc1-117">Value</span></span>                                                                                         | <span data-ttu-id="11bc1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="11bc1-118">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11bc1-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="11bc1-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="11bc1-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="11bc1-120">Method succeeded.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="11bc1-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="11bc1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="11bc1-122">Недопустимый параметр *пстартаддресс*, *нумаддрессес* или *TTL* .</span><span class="sxs-lookup"><span data-stu-id="11bc1-122">The *pStartAddress*, *NumAddresses*, or *Ttl* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="11bc1-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="11bc1-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="11bc1-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="11bc1-124">Insufficient memory exists to perform the operation.</span></span><br/>                  |
| <dl> <span data-ttu-id="11bc1-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="11bc1-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="11bc1-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="11bc1-126">Unspecified error.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="11bc1-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="11bc1-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="11bc1-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="11bc1-128">This method is not yet implemented.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="11bc1-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11bc1-129">Remarks</span></span>

<span data-ttu-id="11bc1-130">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Пстартаддресс* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="11bc1-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pStartAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="11bc1-131">Требования</span><span class="sxs-lookup"><span data-stu-id="11bc1-131">Requirements</span></span>



| <span data-ttu-id="11bc1-132">Требование</span><span class="sxs-lookup"><span data-stu-id="11bc1-132">Requirement</span></span> | <span data-ttu-id="11bc1-133">Значение</span><span class="sxs-lookup"><span data-stu-id="11bc1-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11bc1-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="11bc1-134">TAPI version</span></span><br/> | <span data-ttu-id="11bc1-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="11bc1-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="11bc1-136">Header</span><span class="sxs-lookup"><span data-stu-id="11bc1-136">Header</span></span><br/>       | <dl> <span data-ttu-id="11bc1-137"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="11bc1-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="11bc1-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11bc1-138">Library</span></span><br/>      | <dl> <span data-ttu-id="11bc1-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11bc1-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="11bc1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="11bc1-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="11bc1-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11bc1-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11bc1-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11bc1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11bc1-143">**итконнектион**</span><span class="sxs-lookup"><span data-stu-id="11bc1-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

