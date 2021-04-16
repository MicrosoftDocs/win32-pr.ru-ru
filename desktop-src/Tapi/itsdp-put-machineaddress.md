---
description: Метод размещения \_ мачинеаддресс задает адрес исходного узла.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: 'Итсдп: метод ut_MachineAddress:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec09d41cb7735383f08ce8c8983331165c54fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679881"
---
# <a name="itsdpput_machineaddress-method"></a><span data-ttu-id="a6a42-103">Итсдп::p UT \_ мачинеаддресс метод</span><span class="sxs-lookup"><span data-stu-id="a6a42-103">ITSdp::put\_MachineAddress method</span></span>

<span data-ttu-id="a6a42-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="a6a42-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a6a42-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a6a42-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a6a42-106">Метод **размещения \_ мачинеаддресс** задает адрес исходного узла.</span><span class="sxs-lookup"><span data-stu-id="a6a42-106">The **put\_MachineAddress** method sets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a42-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6a42-107">Syntax</span></span>


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="a6a42-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6a42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a42-109">*пмачинеаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6a42-109">*pMachineAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6a42-110">Указатель на **строку BSTR** , содержащую адрес компьютера узла Конференции.</span><span class="sxs-lookup"><span data-stu-id="a6a42-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a42-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6a42-111">Return value</span></span>

<span data-ttu-id="a6a42-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a6a42-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a6a42-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a6a42-113">Return code</span></span>                                                                                   | <span data-ttu-id="a6a42-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a6a42-114">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6a42-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a6a42-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a6a42-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a6a42-116">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="a6a42-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a6a42-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a6a42-118">Параметр *пмачинеаддресс* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="a6a42-118">The *pMachineAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="a6a42-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a6a42-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a6a42-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a6a42-120">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="a6a42-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a6a42-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a6a42-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a6a42-122">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="a6a42-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="a6a42-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a6a42-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="a6a42-124">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="a6a42-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6a42-125">Remarks</span></span>

<span data-ttu-id="a6a42-126">Приложение должно использовать [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Пмачинеаддресс* и использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="a6a42-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMachineAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="a6a42-127">Параметр *пмачинеаддресс* может быть либо DNS-именем ("JohnSmith.workinghard.Microsoft.com"), либо IP-адресом ("10.111.222.111").</span><span class="sxs-lookup"><span data-stu-id="a6a42-127">The *pMachineAddress* parameter can be either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

<span data-ttu-id="a6a42-128">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="a6a42-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="a6a42-129">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="a6a42-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a42-130">Требования</span><span class="sxs-lookup"><span data-stu-id="a6a42-130">Requirements</span></span>



| <span data-ttu-id="a6a42-131">Требование</span><span class="sxs-lookup"><span data-stu-id="a6a42-131">Requirement</span></span> | <span data-ttu-id="a6a42-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a6a42-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a42-133">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="a6a42-133">TAPI version</span></span><br/> | <span data-ttu-id="a6a42-134">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a6a42-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a6a42-135">Header</span><span class="sxs-lookup"><span data-stu-id="a6a42-135">Header</span></span><br/>       | <dl> <span data-ttu-id="a6a42-136"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6a42-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6a42-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a6a42-137">Library</span></span><br/>      | <dl> <span data-ttu-id="a6a42-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6a42-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a6a42-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a6a42-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="a6a42-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6a42-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a42-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6a42-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a42-142">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="a6a42-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="a6a42-143">**Итсдп:: Get \_ мачинеаддресс**</span><span class="sxs-lookup"><span data-stu-id="a6a42-143">**ITSdp::get\_MachineAddress**</span></span>](itsdp-get-machineaddress.md)
</dt> </dl>

 

