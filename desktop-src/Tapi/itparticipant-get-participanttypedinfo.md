---
description: Метод Get \_ партиЦипанттипединфо получает представление BSTR требуемого типа информации, например Пти \_ EMAILADDRESS.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'Метод ИтпартиЦипант:: get_ParticipantTypedInfo (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675061"
---
# <a name="itparticipantget_participanttypedinfo-method"></a><span data-ttu-id="9920f-103">Метод ИтпартиЦипант:: Get \_ партиЦипанттипединфо</span><span class="sxs-lookup"><span data-stu-id="9920f-103">ITParticipant::get\_ParticipantTypedInfo method</span></span>

<span data-ttu-id="9920f-104">\[**получить \_ ПартиЦипанттипединфо** недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9920f-104">\[**get\_ParticipantTypedInfo** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9920f-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="9920f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9920f-106">Метод **Get \_ партиЦипанттипединфо** получает представление **BSTR** требуемого типа информации, например Пти \_ EMAILADDRESS.</span><span class="sxs-lookup"><span data-stu-id="9920f-106">The **get\_ParticipantTypedInfo** method gets a **BSTR** representation of the type of information needed, such as PTI\_EMAILADDRESS.</span></span>

## <a name="syntax"></a><span data-ttu-id="9920f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9920f-107">Syntax</span></span>


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="9920f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9920f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9920f-109">*Инфотипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9920f-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9920f-110">[**Участник \_ ТИПИЗИРОВАНный \_**](participant-typed-info.md) дескриптор сведений о типе необходимой информации.</span><span class="sxs-lookup"><span data-stu-id="9920f-110">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) descriptor of the type of information needed.</span></span>

</dd> <dt>

<span data-ttu-id="9920f-111">*ппинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9920f-111">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9920f-112">Указатель на представление **BSTR** необходимой информации.</span><span class="sxs-lookup"><span data-stu-id="9920f-112">Pointer to **BSTR** representation of the information needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9920f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9920f-113">Return value</span></span>

<span data-ttu-id="9920f-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="9920f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="9920f-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9920f-115">Return code</span></span>                                                                                    | <span data-ttu-id="9920f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9920f-116">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="9920f-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="9920f-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="9920f-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9920f-119"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-119"><dt>**E\_FAIL**</dt></span></span> </dl>         | <span data-ttu-id="9920f-120">Не удалось хранить данные в *ппинфо* .</span><span class="sxs-lookup"><span data-stu-id="9920f-120">Storage of information into *ppInfo* failed.</span></span><br/>         |
| <dl> <span data-ttu-id="9920f-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="9920f-122">Недопустимый параметр *инфотипе* .</span><span class="sxs-lookup"><span data-stu-id="9920f-122">The *InfoType* parameter is not valid.</span></span><br/>               |
| <dl> <span data-ttu-id="9920f-123"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-123"><dt>**E\_POINTER**</dt></span></span> </dl>      | <span data-ttu-id="9920f-124">Параметр *ппинфо* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="9920f-124">The *ppInfo* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="9920f-125"><dt>**ЭЛЕМЕНТ интерфейса TAPI \_ E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-125"><dt>**TAPI\_E\_NOITEM**</dt></span></span> </dl> | <span data-ttu-id="9920f-126">Интерфейс TAPI не содержит сведений о указанном типе.</span><span class="sxs-lookup"><span data-stu-id="9920f-126">TAPI has no information on the specified type.</span></span><br/>       |
| <dl> <span data-ttu-id="9920f-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>  | <span data-ttu-id="9920f-128">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="9920f-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9920f-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9920f-129">Remarks</span></span>

<span data-ttu-id="9920f-130">Приложение должно использовать [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппинфо* .</span><span class="sxs-lookup"><span data-stu-id="9920f-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9920f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="9920f-131">Requirements</span></span>



| <span data-ttu-id="9920f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="9920f-132">Requirement</span></span> | <span data-ttu-id="9920f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9920f-133">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9920f-134">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="9920f-134">TAPI version</span></span><br/> | <span data-ttu-id="9920f-135">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9920f-135">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="9920f-136">Header</span><span class="sxs-lookup"><span data-stu-id="9920f-136">Header</span></span><br/>       | <dl> <span data-ttu-id="9920f-137"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-137"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9920f-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9920f-138">Library</span></span><br/>      | <dl> <span data-ttu-id="9920f-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-139"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="9920f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9920f-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="9920f-141"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9920f-141"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9920f-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9920f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9920f-143">**итпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="9920f-143">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="9920f-144">**\_сведения о введенных участниках \_**</span><span class="sxs-lookup"><span data-stu-id="9920f-144">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> <dt>

[<span data-ttu-id="9920f-145">**типы носителей**</span><span class="sxs-lookup"><span data-stu-id="9920f-145">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

