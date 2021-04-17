---
description: Метод Get \_ нумпортс возвращает количество портов, необходимых для сеанса. В сеансе используется указанное число портов, начиная со значения, возвращенного функцией Get \_ стартпорт.
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'Метод Итмедиа:: get_NumPorts (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc223ddd5d210d2c1d440c52ca4201ccd6334b08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680034"
---
# <a name="itmediaget_numports-method"></a><span data-ttu-id="a2219-104">Метод Итмедиа:: Get \_ нумпортс</span><span class="sxs-lookup"><span data-stu-id="a2219-104">ITMedia::get\_NumPorts method</span></span>

<span data-ttu-id="a2219-105">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="a2219-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a2219-106">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a2219-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a2219-107">Метод **Get \_ нумпортс** возвращает количество портов, необходимых для сеанса.</span><span class="sxs-lookup"><span data-stu-id="a2219-107">The **get\_NumPorts** method gets the number of ports needed for the session.</span></span> <span data-ttu-id="a2219-108">В сеансе используется указанное число портов, начиная со значения, возвращенного функцией [**Get \_ стартпорт**](itmedia-get-startport.md).</span><span class="sxs-lookup"><span data-stu-id="a2219-108">The session uses the specified number of ports starting from the value returned by [**get\_StartPort**](itmedia-get-startport.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a2219-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2219-109">Syntax</span></span>


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="a2219-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2219-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2219-111">*пнумпортс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a2219-111">*pNumPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2219-112">Указатель на число портов.</span><span class="sxs-lookup"><span data-stu-id="a2219-112">Pointer to the number of ports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2219-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2219-113">Return value</span></span>

<span data-ttu-id="a2219-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a2219-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a2219-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a2219-115">Return code</span></span>                                                                                   | <span data-ttu-id="a2219-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a2219-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a2219-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a2219-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a2219-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="a2219-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a2219-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a2219-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a2219-120">Параметр *пнумпортс* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="a2219-120">The *pNumPorts* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="a2219-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a2219-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a2219-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a2219-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a2219-123"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="a2219-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a2219-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="a2219-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a2219-125"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="a2219-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a2219-126">Этот метод еще не реализован.</span><span class="sxs-lookup"><span data-stu-id="a2219-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="a2219-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a2219-127">Requirements</span></span>



| <span data-ttu-id="a2219-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a2219-128">Requirement</span></span> | <span data-ttu-id="a2219-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a2219-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2219-130">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="a2219-130">TAPI version</span></span><br/> | <span data-ttu-id="a2219-131">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a2219-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a2219-132">Header</span><span class="sxs-lookup"><span data-stu-id="a2219-132">Header</span></span><br/>       | <dl> <span data-ttu-id="a2219-133"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2219-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2219-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2219-134">Library</span></span><br/>      | <dl> <span data-ttu-id="a2219-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2219-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a2219-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a2219-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="a2219-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2219-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2219-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2219-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2219-139">**итмедиа**</span><span class="sxs-lookup"><span data-stu-id="a2219-139">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




