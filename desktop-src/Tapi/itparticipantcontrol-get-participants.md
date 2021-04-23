---
description: Метод Get \_ Участники создает коллекцию участников, связанных с текущей Конференцией.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'Метод ИтпартиЦипантконтрол:: get_Participants (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685423"
---
# <a name="itparticipantcontrolget_participants-method"></a><span data-ttu-id="ac1d5-103">Метод ИтпартиЦипантконтрол:: Get \_ участников</span><span class="sxs-lookup"><span data-stu-id="ac1d5-103">ITParticipantControl::get\_Participants method</span></span>

<span data-ttu-id="ac1d5-104">\[**получить \_ Участники** не могут использоваться в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ac1d5-104">\[**get\_Participants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ac1d5-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="ac1d5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ac1d5-106">Метод **Get \_ Участники** создает коллекцию участников, связанных с текущей Конференцией.</span><span class="sxs-lookup"><span data-stu-id="ac1d5-106">The **get\_Participants** method creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="ac1d5-107">Этот метод предоставляется для клиентских приложений автоматизации, например, написанных на Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ac1d5-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="ac1d5-108">Приложения C и C++ должны использовать метод [**енумератепартиЦипантс**](itparticipantcontrol-enumerateparticipants.md) .</span><span class="sxs-lookup"><span data-stu-id="ac1d5-108">C and C++ applications must use the [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac1d5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac1d5-109">Syntax</span></span>


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="ac1d5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac1d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac1d5-111">*пвариант* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac1d5-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac1d5-112">Указатель на **вариант** , содержащий [**итколлектион**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) указателей интерфейса [**итпартиЦипант**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="ac1d5-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac1d5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac1d5-113">Return value</span></span>

<span data-ttu-id="ac1d5-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="ac1d5-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ac1d5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ac1d5-115">Value</span></span>                                                                                         | <span data-ttu-id="ac1d5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ac1d5-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ac1d5-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d5-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ac1d5-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ac1d5-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ac1d5-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d5-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ac1d5-120">Параметр *пвариант* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="ac1d5-120">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |
| <dl> <span data-ttu-id="ac1d5-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d5-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ac1d5-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ac1d5-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac1d5-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac1d5-123">Remarks</span></span>

<span data-ttu-id="ac1d5-124">TAPI вызывает метод **AddRef** в интерфейсе [**итпартиЦипант**](itparticipant.md) , возвращенном **итпартиЦипантконтрол:: Get \_ Участники**.</span><span class="sxs-lookup"><span data-stu-id="ac1d5-124">TAPI calls the **AddRef** method on the [**ITParticipant**](itparticipant.md) interface returned by **ITParticipantControl::get\_Participants**.</span></span> <span data-ttu-id="ac1d5-125">Приложение должно вызвать **выпуск** в интерфейсе **итпартиЦипант** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="ac1d5-125">The application must call **Release** on the **ITParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac1d5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ac1d5-126">Requirements</span></span>



| <span data-ttu-id="ac1d5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ac1d5-127">Requirement</span></span> | <span data-ttu-id="ac1d5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ac1d5-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1d5-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ac1d5-129">TAPI version</span></span><br/> | <span data-ttu-id="ac1d5-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ac1d5-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ac1d5-131">Header</span><span class="sxs-lookup"><span data-stu-id="ac1d5-131">Header</span></span><br/>       | <dl> <span data-ttu-id="ac1d5-132"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d5-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="ac1d5-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac1d5-133">Library</span></span><br/>      | <dl> <span data-ttu-id="ac1d5-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d5-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ac1d5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ac1d5-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="ac1d5-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac1d5-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ac1d5-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac1d5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac1d5-138">**итпартиЦипантконтрол**</span><span class="sxs-lookup"><span data-stu-id="ac1d5-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="ac1d5-139">**енумератепартиЦипантс**</span><span class="sxs-lookup"><span data-stu-id="ac1d5-139">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[<span data-ttu-id="ac1d5-140">**итколлектион**</span><span class="sxs-lookup"><span data-stu-id="ac1d5-140">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="ac1d5-141">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="ac1d5-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




