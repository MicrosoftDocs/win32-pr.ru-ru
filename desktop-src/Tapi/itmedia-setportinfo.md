---
description: Метод Сетпортинфо задает 16-битное значение порта для первого порта и число портов, необходимых для сеанса.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: 'Метод Итмедиа:: Сетпортинфо (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689402"
---
# <a name="itmediasetportinfo-method"></a><span data-ttu-id="a4db1-103">Метод Итмедиа:: Сетпортинфо</span><span class="sxs-lookup"><span data-stu-id="a4db1-103">ITMedia::SetPortInfo method</span></span>

<span data-ttu-id="a4db1-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="a4db1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a4db1-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a4db1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a4db1-106">Метод **сетпортинфо** задает 16-битное значение порта для первого порта и число портов, необходимых для сеанса.</span><span class="sxs-lookup"><span data-stu-id="a4db1-106">The **SetPortInfo** method sets the 16-bit port value for the first port and the number of ports needed for a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4db1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4db1-107">Syntax</span></span>


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="a4db1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4db1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4db1-109">*Стартпорт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4db1-109">*StartPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4db1-110">Начальный порт.</span><span class="sxs-lookup"><span data-stu-id="a4db1-110">Starting port.</span></span> <span data-ttu-id="a4db1-111">Это может быть значение в диапазоне 0-65535.</span><span class="sxs-lookup"><span data-stu-id="a4db1-111">This can be a value in the range 0-65535.</span></span>

</dd> <dt>

<span data-ttu-id="a4db1-112">*Нумпортс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4db1-112">*NumPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4db1-113">Число портов.</span><span class="sxs-lookup"><span data-stu-id="a4db1-113">Number of ports.</span></span> <span data-ttu-id="a4db1-114">Это может быть значение в диапазоне 0-65535.</span><span class="sxs-lookup"><span data-stu-id="a4db1-114">This can be a value in the range 0-65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4db1-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4db1-115">Return value</span></span>

<span data-ttu-id="a4db1-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a4db1-116">This method can return one of these values.</span></span>



| <span data-ttu-id="a4db1-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a4db1-117">Return code</span></span>                                                                                   | <span data-ttu-id="a4db1-118">Описание</span><span class="sxs-lookup"><span data-stu-id="a4db1-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a4db1-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a4db1-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a4db1-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a4db1-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a4db1-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a4db1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a4db1-122">Недопустимый параметр *стартпорт или нумпортс* .</span><span class="sxs-lookup"><span data-stu-id="a4db1-122">The *StartPort or NumPorts* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="a4db1-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a4db1-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a4db1-124">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a4db1-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a4db1-125"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a4db1-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a4db1-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a4db1-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a4db1-127"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="a4db1-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a4db1-128">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="a4db1-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a4db1-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4db1-129">Remarks</span></span>

<span data-ttu-id="a4db1-130">Эта функция может передавать данные по сети в незашифрованном виде; Таким образом, кто-то, кто прослушивает сеть, может прочитать данные.</span><span class="sxs-lookup"><span data-stu-id="a4db1-130">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="a4db1-131">Прежде чем использовать этот метод, следует учесть угрозу безопасности при отправке данных в виде открытого текста.</span><span class="sxs-lookup"><span data-stu-id="a4db1-131">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4db1-132">Требования</span><span class="sxs-lookup"><span data-stu-id="a4db1-132">Requirements</span></span>



| <span data-ttu-id="a4db1-133">Требование</span><span class="sxs-lookup"><span data-stu-id="a4db1-133">Requirement</span></span> | <span data-ttu-id="a4db1-134">Значение</span><span class="sxs-lookup"><span data-stu-id="a4db1-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a4db1-135">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="a4db1-135">TAPI version</span></span><br/> | <span data-ttu-id="a4db1-136">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a4db1-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a4db1-137">Header</span><span class="sxs-lookup"><span data-stu-id="a4db1-137">Header</span></span><br/>       | <dl> <span data-ttu-id="a4db1-138"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4db1-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4db1-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a4db1-139">Library</span></span><br/>      | <dl> <span data-ttu-id="a4db1-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4db1-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a4db1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a4db1-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="a4db1-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4db1-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4db1-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4db1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4db1-144">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="a4db1-144">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




