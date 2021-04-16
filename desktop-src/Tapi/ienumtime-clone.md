---
description: Метод Clone создает еще один перечислитель, который содержит то же состояние перечисления, что и текущий.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'Метод Иенумтиме:: Clone (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679816"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="12a4a-103">Метод Иенумтиме:: Clone</span><span class="sxs-lookup"><span data-stu-id="12a4a-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="12a4a-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="12a4a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="12a4a-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="12a4a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="12a4a-106">Метод **clone** создает еще один перечислитель, который содержит то же состояние перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="12a4a-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="12a4a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12a4a-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="12a4a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="12a4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12a4a-109">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="12a4a-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12a4a-110">Указатель на новый объект [**иенумтиме**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="12a4a-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12a4a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12a4a-111">Return value</span></span>

<span data-ttu-id="12a4a-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="12a4a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="12a4a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="12a4a-113">Value</span></span>                                                                                         | <span data-ttu-id="12a4a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="12a4a-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="12a4a-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="12a4a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="12a4a-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="12a4a-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="12a4a-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="12a4a-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="12a4a-118">Параметр *ппенум* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="12a4a-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="12a4a-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="12a4a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="12a4a-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="12a4a-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="12a4a-121"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="12a4a-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="12a4a-122">Сбой по неизвестным причинам.</span><span class="sxs-lookup"><span data-stu-id="12a4a-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="12a4a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12a4a-123">Remarks</span></span>

<span data-ttu-id="12a4a-124">TAPI вызывает метод **AddRef** в интерфейсе [**иенумтиме**](ienumtime.md) , возвращенном **иенумтиме:: Clone**.</span><span class="sxs-lookup"><span data-stu-id="12a4a-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="12a4a-125">Приложение должно вызвать **выпуск** в интерфейсе **иенумтиме** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="12a4a-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="12a4a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="12a4a-126">Requirements</span></span>



| <span data-ttu-id="12a4a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="12a4a-127">Requirement</span></span> | <span data-ttu-id="12a4a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="12a4a-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12a4a-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="12a4a-129">TAPI version</span></span><br/> | <span data-ttu-id="12a4a-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="12a4a-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="12a4a-131">Header</span><span class="sxs-lookup"><span data-stu-id="12a4a-131">Header</span></span><br/>       | <dl> <span data-ttu-id="12a4a-132"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="12a4a-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="12a4a-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="12a4a-133">Library</span></span><br/>      | <dl> <span data-ttu-id="12a4a-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12a4a-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="12a4a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="12a4a-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="12a4a-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12a4a-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a4a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12a4a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a4a-138">**иенумтиме**</span><span class="sxs-lookup"><span data-stu-id="12a4a-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




