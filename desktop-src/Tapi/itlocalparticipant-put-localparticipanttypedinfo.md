---
description: Метод размещения \_ локалпартиЦипанттипединфо задает сведения о участнике.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: 'ИтлокалпартиЦипант: метод ut_LocalParticipantTypedInfo:p (Конфприв. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689070"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a><span data-ttu-id="3f7f7-103">ИтлокалпартиЦипант::p UT \_ локалпартиЦипанттипединфо метод</span><span class="sxs-lookup"><span data-stu-id="3f7f7-103">ITLocalParticipant::put\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="3f7f7-104">Метод **размещения \_ локалпартиЦипанттипединфо** задает сведения о участнике.</span><span class="sxs-lookup"><span data-stu-id="3f7f7-104">The **put\_LocalParticipantTypedInfo** method sets participant information.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f7f7-105">Syntax</span></span>


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3f7f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f7f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f7f7-107">*Инфотипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f7f7-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f7f7-108">[**Участник \_ ТИПИЗИРОВАНный \_**](participant-typed-info.md) идентификатор сведений о требуемом типе информации.</span><span class="sxs-lookup"><span data-stu-id="3f7f7-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of the type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="3f7f7-109">*ппинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f7f7-109">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f7f7-110">**BSTR** , содержащий необходимое новое значение для данных.</span><span class="sxs-lookup"><span data-stu-id="3f7f7-110">**BSTR** containing the required new value for the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f7f7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f7f7-111">Return value</span></span>

<span data-ttu-id="3f7f7-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3f7f7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3f7f7-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3f7f7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f7f7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f7f7-114">Remarks</span></span>

<span data-ttu-id="3f7f7-115">Приложение должно использовать [сисаллокстринг](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) для выделения памяти для параметра *Ппинфо* и использовать [сисфристринг](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для освобождения памяти, когда переменная больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="3f7f7-115">The application must use [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *ppInfo* parameter and use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f7f7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3f7f7-116">Requirements</span></span>



| <span data-ttu-id="3f7f7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3f7f7-117">Requirement</span></span> | <span data-ttu-id="3f7f7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3f7f7-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7f7-119">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="3f7f7-119">TAPI version</span></span><br/> | <span data-ttu-id="3f7f7-120">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3f7f7-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3f7f7-121">Header</span><span class="sxs-lookup"><span data-stu-id="3f7f7-121">Header</span></span><br/>       | <dl> <span data-ttu-id="3f7f7-122"><dt>Конфприв. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f7f7-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="3f7f7-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3f7f7-123">Library</span></span><br/>      | <dl> <span data-ttu-id="3f7f7-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f7f7-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3f7f7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3f7f7-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="3f7f7-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f7f7-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3f7f7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f7f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f7f7-128">**итлокалпартиЦипант**</span><span class="sxs-lookup"><span data-stu-id="3f7f7-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="3f7f7-129">**\_сведения о введенных участниках \_**</span><span class="sxs-lookup"><span data-stu-id="3f7f7-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

