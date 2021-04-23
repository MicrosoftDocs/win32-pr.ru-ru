---
description: Метод Фриевентдата освобождает место, выделенное для структуры НМЕВЕНТДАТА.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'Метод Имониторевентер:: Фриевентдата (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673179"
---
# <a name="imonitoreventerfreeeventdata-method"></a><span data-ttu-id="8bb91-103">Метод Имониторевентер:: Фриевентдата</span><span class="sxs-lookup"><span data-stu-id="8bb91-103">IMonitorEventer::FreeEventData method</span></span>

<span data-ttu-id="8bb91-104">Метод **фриевентдата** освобождает место, выделенное для структуры [**нмевентдата**](nmeventdata.md) .</span><span class="sxs-lookup"><span data-stu-id="8bb91-104">The **FreeEventData** method frees space allocated for the [**NMEVENTDATA**](nmeventdata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bb91-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bb91-105">Syntax</span></span>


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="8bb91-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bb91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bb91-107">*пнмевентдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8bb91-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bb91-108">Адрес структуры [**нмевентдата**](nmeventdata.md) , памяти, из которой освобождается.</span><span class="sxs-lookup"><span data-stu-id="8bb91-108">Address of the [**NMEVENTDATA**](nmeventdata.md) structure, the memory of which is freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bb91-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bb91-109">Return value</span></span>

<span data-ttu-id="8bb91-110">Этот метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="8bb91-110">This method returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bb91-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8bb91-111">Remarks</span></span>

<span data-ttu-id="8bb91-112">Мониторы вызывают этот метод, чтобы освободить память, выделенную для структуры данных события.</span><span class="sxs-lookup"><span data-stu-id="8bb91-112">Monitors call this method to free the memory they allocate for the event data structure.</span></span> <span data-ttu-id="8bb91-113">Имейте в виду, что хотя у монитора по-прежнему есть указатель на строки в выделенной структуре [**нмевентдата**](nmeventdata.md) , память для этих строк должна быть освобождена до вызова метода **фриевентдата** .</span><span class="sxs-lookup"><span data-stu-id="8bb91-113">Be aware that while the monitor still has a pointer to strings in an allocated [**NMEVENTDATA**](nmeventdata.md) structure, the memory for these strings must be freed before the **FreeEventData** method is called.</span></span>

<span data-ttu-id="8bb91-114">Дополнительные сведения о том, как выделить память для структуры [**нмевентдата**](nmeventdata.md) , см. в разделе [**Имониторевентер:: жетевентдата**](imonitoreventer-geteventdata.md).</span><span class="sxs-lookup"><span data-stu-id="8bb91-114">For more information about how to allocate memory for an [**NMEVENTDATA**](nmeventdata.md) structure, see [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bb91-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8bb91-115">Requirements</span></span>



| <span data-ttu-id="8bb91-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8bb91-116">Requirement</span></span> | <span data-ttu-id="8bb91-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8bb91-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8bb91-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bb91-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8bb91-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8bb91-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8bb91-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bb91-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8bb91-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8bb91-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8bb91-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8bb91-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bb91-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bb91-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bb91-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bb91-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bb91-125">**имониторевентер**</span><span class="sxs-lookup"><span data-stu-id="8bb91-125">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="8bb91-126">**Имониторевентер:: Жетевентдата**</span><span class="sxs-lookup"><span data-stu-id="8bb91-126">**IMonitorEventer::GetEventData**</span></span>](imonitoreventer-geteventdata.md)
</dt> <dt>

[<span data-ttu-id="8bb91-127">**нмевентдата**</span><span class="sxs-lookup"><span data-stu-id="8bb91-127">**NMEVENTDATA**</span></span>](nmeventdata.md)
</dt> </dl>

 

 




