---
description: Метод Get \_ локалпартиЦипанттипединфо получает сведения о участнике, такие как имя электронной почты или географическое расположение.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Метод ИтлокалпартиЦипант:: get_LocalParticipantTypedInfo (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689072"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a><span data-ttu-id="0f9ac-103">Метод ИтлокалпартиЦипант:: Get \_ локалпартиЦипанттипединфо</span><span class="sxs-lookup"><span data-stu-id="0f9ac-103">ITLocalParticipant::get\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="0f9ac-104">Метод **Get \_ локалпартиЦипанттипединфо** получает сведения о участнике, такие как имя электронной почты или географическое расположение.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-104">The **get\_LocalParticipantTypedInfo** method gets participant information, such as e-mail name or geographical location.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f9ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f9ac-105">Syntax</span></span>


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="0f9ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f9ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f9ac-107">*Инфотипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f9ac-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f9ac-108">[**Участник \_ ТИПИЗИРОВАНный \_**](participant-typed-info.md) идентификатор сведений о требуемом типе сведений.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="0f9ac-109">*ппинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0f9ac-109">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f9ac-110">Указатель на **BSTR** , который будет содержать необходимые сведения после успешного возврата метода.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-110">Pointer to a **BSTR** that will contain the required information following a successful return of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f9ac-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f9ac-111">Return value</span></span>

<span data-ttu-id="0f9ac-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0f9ac-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f9ac-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f9ac-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f9ac-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f9ac-114">Remarks</span></span>

<span data-ttu-id="0f9ac-115">Приложение должно использовать [сисфристринг](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, выделенной для параметра *ппинфо* .</span><span class="sxs-lookup"><span data-stu-id="0f9ac-115">The application must use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f9ac-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0f9ac-116">Requirements</span></span>



| <span data-ttu-id="0f9ac-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0f9ac-117">Requirement</span></span> | <span data-ttu-id="0f9ac-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0f9ac-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f9ac-119">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="0f9ac-119">TAPI version</span></span><br/> | <span data-ttu-id="0f9ac-120">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0f9ac-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0f9ac-121">Header</span><span class="sxs-lookup"><span data-stu-id="0f9ac-121">Header</span></span><br/>       | <dl> <span data-ttu-id="0f9ac-122"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f9ac-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="0f9ac-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f9ac-123">Library</span></span><br/>      | <dl> <span data-ttu-id="0f9ac-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f9ac-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0f9ac-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0f9ac-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="0f9ac-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f9ac-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0f9ac-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f9ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f9ac-128">**итлокалпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="0f9ac-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="0f9ac-129">**\_сведения о введенных участниках \_**</span><span class="sxs-lookup"><span data-stu-id="0f9ac-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

