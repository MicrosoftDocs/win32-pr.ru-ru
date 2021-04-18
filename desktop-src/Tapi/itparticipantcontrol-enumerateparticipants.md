---
description: Метод ЕнумератепартиЦипантс перечисляет участников, связанных с текущей Конференцией.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'Метод ИтпартиЦипантконтрол:: ЕнумератепартиЦипантс (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685102"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a><span data-ttu-id="8e790-103">Метод ИтпартиЦипантконтрол:: ЕнумератепартиЦипантс</span><span class="sxs-lookup"><span data-stu-id="8e790-103">ITParticipantControl::EnumerateParticipants method</span></span>

<span data-ttu-id="8e790-104">\[**ЕнумератепартиЦипантс** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8e790-104">\[**EnumerateParticipants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8e790-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8e790-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8e790-106">Метод **енумератепартиЦипантс** перечисляет участников, связанных с текущей Конференцией.</span><span class="sxs-lookup"><span data-stu-id="8e790-106">The **EnumerateParticipants** method enumerates participants associated with the current conference.</span></span> <span data-ttu-id="8e790-107">Этот метод предоставляется для приложений C и C++.</span><span class="sxs-lookup"><span data-stu-id="8e790-107">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="8e790-108">Клиентские приложения автоматизации, например написанные на Visual Basic, должны использовать метод [**Get \_ участников**](itparticipantcontrol-get-participants.md) .</span><span class="sxs-lookup"><span data-stu-id="8e790-108">Automation client applications, such as those written in Visual Basic, must use the [**get\_Participants**](itparticipantcontrol-get-participants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e790-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e790-109">Syntax</span></span>


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a><span data-ttu-id="8e790-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e790-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e790-111">*ппенумпартиЦипантс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8e790-111">*ppEnumParticipants* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e790-112">Указатель на интерфейс [**иенумпартиЦипант**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="8e790-112">Pointer to [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e790-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e790-113">Return value</span></span>

<span data-ttu-id="8e790-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="8e790-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8e790-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8e790-115">Value</span></span>                                                                                         | <span data-ttu-id="8e790-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8e790-116">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e790-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8e790-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8e790-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="8e790-118">Method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="8e790-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="8e790-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8e790-120">Параметр *ппенумпартиЦипантс* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="8e790-120">The *ppEnumParticipants* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="8e790-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8e790-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8e790-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="8e790-122">Insufficient memory exists to perform the operation.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="8e790-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e790-123">Remarks</span></span>

<span data-ttu-id="8e790-124">TAPI вызывает метод **AddRef** в интерфейсе [**иенумпартиЦипант**](ienumparticipant.md) , возвращенном **итпартиЦипантконтрол:: енумератепартиЦипантс**.</span><span class="sxs-lookup"><span data-stu-id="8e790-124">TAPI calls the **AddRef** method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **ITParticipantControl::EnumerateParticipants**.</span></span> <span data-ttu-id="8e790-125">Приложение должно вызвать **выпуск** в интерфейсе **иенумпартиЦипант** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="8e790-125">The application must call **Release** on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e790-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8e790-126">Requirements</span></span>



| <span data-ttu-id="8e790-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8e790-127">Requirement</span></span> | <span data-ttu-id="8e790-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8e790-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e790-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8e790-129">TAPI version</span></span><br/> | <span data-ttu-id="8e790-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8e790-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8e790-131">Header</span><span class="sxs-lookup"><span data-stu-id="8e790-131">Header</span></span><br/>       | <dl> <span data-ttu-id="8e790-132"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e790-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="8e790-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8e790-133">Library</span></span><br/>      | <dl> <span data-ttu-id="8e790-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e790-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8e790-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8e790-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="8e790-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e790-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8e790-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e790-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e790-138">**итпартиЦипантконтрол**</span><span class="sxs-lookup"><span data-stu-id="8e790-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="8e790-139">**получение \_ участников**</span><span class="sxs-lookup"><span data-stu-id="8e790-139">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)
</dt> <dt>

[<span data-ttu-id="8e790-140">**иенумпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="8e790-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="8e790-141">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="8e790-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




