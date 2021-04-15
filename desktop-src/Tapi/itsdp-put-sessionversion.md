---
description: Метод размещения \_ сессионверсион задает версию сеанса.
ms.assetid: 8984d608-0fad-4979-9c58-ac2fb7926796
title: 'Итсдп: метод ut_SessionVersion:p (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a096117f894a2ff33f127c683b84ba50e88308e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689374"
---
# <a name="itsdpput_sessionversion-method"></a><span data-ttu-id="a0098-103">Итсдп::p UT \_ сессионверсион метод</span><span class="sxs-lookup"><span data-stu-id="a0098-103">ITSdp::put\_SessionVersion method</span></span>

<span data-ttu-id="a0098-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="a0098-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a0098-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a0098-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a0098-106">Метод **размещения \_ сессионверсион** задает версию сеанса.</span><span class="sxs-lookup"><span data-stu-id="a0098-106">The **put\_SessionVersion** method sets the session version.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0098-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0098-107">Syntax</span></span>


```C++
HRESULT put_SessionVersion(
  [in] DOUBLE SessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="a0098-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0098-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0098-109">*Сессионверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0098-109">*SessionVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0098-110">Значение версии сеанса.</span><span class="sxs-lookup"><span data-stu-id="a0098-110">Session version value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0098-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0098-111">Return value</span></span>

<span data-ttu-id="a0098-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a0098-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a0098-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a0098-113">Return code</span></span>                                                                                   | <span data-ttu-id="a0098-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a0098-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a0098-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a0098-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a0098-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a0098-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a0098-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a0098-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a0098-118">Недопустимый параметр *сессионверсион* .</span><span class="sxs-lookup"><span data-stu-id="a0098-118">The *SessionVersion* parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="a0098-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a0098-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a0098-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a0098-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a0098-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a0098-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a0098-122">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a0098-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a0098-123"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="a0098-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a0098-124">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="a0098-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a0098-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0098-125">Remarks</span></span>

<span data-ttu-id="a0098-126">Возвращаемое значение этого метода может быть **ulong**, но Visual Basic не поддерживает тип **ulong** .</span><span class="sxs-lookup"><span data-stu-id="a0098-126">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="a0098-127">**Double** — это следующий наименьший тип, охватывающий весь диапазон требуемых значений.</span><span class="sxs-lookup"><span data-stu-id="a0098-127">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

<span data-ttu-id="a0098-128">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="a0098-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="a0098-129">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="a0098-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0098-130">Требования</span><span class="sxs-lookup"><span data-stu-id="a0098-130">Requirements</span></span>



| <span data-ttu-id="a0098-131">Требование</span><span class="sxs-lookup"><span data-stu-id="a0098-131">Requirement</span></span> | <span data-ttu-id="a0098-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a0098-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0098-133">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="a0098-133">TAPI version</span></span><br/> | <span data-ttu-id="a0098-134">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a0098-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a0098-135">Header</span><span class="sxs-lookup"><span data-stu-id="a0098-135">Header</span></span><br/>       | <dl> <span data-ttu-id="a0098-136"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0098-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0098-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a0098-137">Library</span></span><br/>      | <dl> <span data-ttu-id="a0098-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0098-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a0098-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a0098-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="a0098-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0098-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0098-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0098-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0098-142">**итсдп**</span><span class="sxs-lookup"><span data-stu-id="a0098-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="a0098-143">**Итсдп:: Get \_ сессионверсион**</span><span class="sxs-lookup"><span data-stu-id="a0098-143">**ITSdp::get\_SessionVersion**</span></span>](itsdp-get-sessionversion.md)
</dt> </dl>

 

 




