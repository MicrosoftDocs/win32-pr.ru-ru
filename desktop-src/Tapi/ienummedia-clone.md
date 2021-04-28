---
description: 'Метод Иенуммедиа:: Clone. метод Clone создает еще один перечислитель, который содержит то же состояние перечисления, что и текущий.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'Метод Иенуммедиа:: Clone (Сдпблб. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f81542e1b0e3fc5bfb44e59827608396d7d906c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114552"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="8f7bb-103">Метод Иенуммедиа:: Clone</span><span class="sxs-lookup"><span data-stu-id="8f7bb-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="8f7bb-104">\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8f7bb-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="8f7bb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8f7bb-106">Метод **clone** создает еще один перечислитель, который содержит то же состояние перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f7bb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f7bb-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="8f7bb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f7bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f7bb-109">*ппенум* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8f7bb-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f7bb-110">Указатель на новый объект [**иенуммедиа**](ienummedia.md) .</span><span class="sxs-lookup"><span data-stu-id="8f7bb-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f7bb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f7bb-111">Return value</span></span>

<span data-ttu-id="8f7bb-112">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8f7bb-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8f7bb-113">Value</span></span>                                                                                         | <span data-ttu-id="8f7bb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8f7bb-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8f7bb-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8f7bb-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8f7bb-116">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8f7bb-117"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="8f7bb-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8f7bb-118">Параметр *ппенум* не является допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="8f7bb-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8f7bb-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8f7bb-120">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8f7bb-121"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="8f7bb-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="8f7bb-122">Сбой по неизвестным причинам.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8f7bb-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="8f7bb-123">Remarks</span></span>

<span data-ttu-id="8f7bb-124">TAPI вызывает метод **AddRef** в интерфейсе [**иенуммедиа**](ienummedia.md) , возвращенном **иенуммедиа:: Clone**.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="8f7bb-125">Приложение должно вызвать **выпуск** в интерфейсе **иенуммедиа** , чтобы освободить ресурсы, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f7bb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8f7bb-126">Requirements</span></span>



| <span data-ttu-id="8f7bb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8f7bb-127">Requirement</span></span> | <span data-ttu-id="8f7bb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8f7bb-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f7bb-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8f7bb-129">TAPI version</span></span><br/> | <span data-ttu-id="8f7bb-130">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8f7bb-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8f7bb-131">Header</span><span class="sxs-lookup"><span data-stu-id="8f7bb-131">Header</span></span><br/>       | <dl> <span data-ttu-id="8f7bb-132"><dt>Сдпблб. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f7bb-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f7bb-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8f7bb-133">Library</span></span><br/>      | <dl> <span data-ttu-id="8f7bb-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f7bb-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8f7bb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8f7bb-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="8f7bb-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f7bb-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f7bb-137">См. также</span><span class="sxs-lookup"><span data-stu-id="8f7bb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f7bb-138">**иенуммедиа**</span><span class="sxs-lookup"><span data-stu-id="8f7bb-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




