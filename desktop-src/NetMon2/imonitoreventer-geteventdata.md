---
description: Метод Жетевентдата выделяет место для структур НМЕВЕНТДАТА и НМКОЛУМНИНФО.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'Метод Имониторевентер:: Жетевентдата (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263011"
---
# <a name="imonitoreventergeteventdata-method"></a><span data-ttu-id="30517-103">Метод Имониторевентер:: Жетевентдата</span><span class="sxs-lookup"><span data-stu-id="30517-103">IMonitorEventer::GetEventData method</span></span>

<span data-ttu-id="30517-104">Метод **жетевентдата** выделяет место для структур [нмевентдата](nmeventdata.md) и [нмколумнинфо](nmcolumninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="30517-104">The **GetEventData** method allocates space for the [NMEVENTDATA](nmeventdata.md) and [NMCOLUMNINFO](nmcolumninfo.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="30517-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30517-105">Syntax</span></span>


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="30517-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30517-107">*бнумколумнс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="30517-107">*bNumColumns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30517-108">Количество необходимых структур **нмколумнинфо** .</span><span class="sxs-lookup"><span data-stu-id="30517-108">Number of **NMCOLUMNINFO** structures needed.</span></span>

</dd> <dt>

<span data-ttu-id="30517-109">*ппнмевентдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="30517-109">*ppNMEventData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30517-110">Адрес возвращаемой структуры **нмевентдата** .</span><span class="sxs-lookup"><span data-stu-id="30517-110">Address of the **NMEVENTDATA** structure that is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30517-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30517-111">Return value</span></span>

<span data-ttu-id="30517-112">Если метод выполнен успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="30517-112">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="30517-113">Если метод завершился неудачно, возвращаемое значение НМЕРР не \_ хватает \_ \_ памяти.</span><span class="sxs-lookup"><span data-stu-id="30517-113">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="30517-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30517-114">Remarks</span></span>

<span data-ttu-id="30517-115">Мониторы вызывают этот метод, чтобы выделить память для структур данных событий и сведений о столбцах.</span><span class="sxs-lookup"><span data-stu-id="30517-115">Monitors call this method to allocate memory for the event data and column information structures.</span></span> <span data-ttu-id="30517-116">Сведения о высвобождении памяти, выделенной для структуры **нмевентдата** , см. в разделе [Имониторевентер:: фриевентдата](imonitoreventer-freeeventdata.md).</span><span class="sxs-lookup"><span data-stu-id="30517-116">To free memory allocated for an **NMEVENTDATA** structure, see [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30517-117">Требования</span><span class="sxs-lookup"><span data-stu-id="30517-117">Requirements</span></span>



| <span data-ttu-id="30517-118">Требование</span><span class="sxs-lookup"><span data-stu-id="30517-118">Requirement</span></span> | <span data-ttu-id="30517-119">Значение</span><span class="sxs-lookup"><span data-stu-id="30517-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="30517-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30517-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30517-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30517-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="30517-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30517-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30517-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30517-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="30517-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="30517-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30517-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="30517-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30517-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30517-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30517-127">имониторевентер</span><span class="sxs-lookup"><span data-stu-id="30517-127">IMonitorEventer</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="30517-128">Имониторевентер:: Фриевентдата</span><span class="sxs-lookup"><span data-stu-id="30517-128">IMonitorEventer::FreeEventData</span></span>](imonitoreventer-freeeventdata.md)
</dt> <dt>

[<span data-ttu-id="30517-129">нмевентдата</span><span class="sxs-lookup"><span data-stu-id="30517-129">NMEVENTDATA</span></span>](nmeventdata.md)
</dt> <dt>

[<span data-ttu-id="30517-130">нмколумнинфо</span><span class="sxs-lookup"><span data-stu-id="30517-130">NMCOLUMNINFO</span></span>](nmcolumninfo.md)
</dt> </dl>

 

 




