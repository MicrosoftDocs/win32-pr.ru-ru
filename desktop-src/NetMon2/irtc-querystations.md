---
description: Список всех компьютеров, на которых в настоящее время используется сетевой монитор для записи сетевых данных.
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: 'Метод ИРТК:: Куеристатионс (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a0cebd789284dd41c293424a70686f30eb4601d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991572"
---
# <a name="irtcquerystations-method"></a><span data-ttu-id="888d3-103">Метод ИРТК:: Куеристатионс</span><span class="sxs-lookup"><span data-stu-id="888d3-103">IRTC::QueryStations method</span></span>

<span data-ttu-id="888d3-104">Метод **куеристатионс** предоставляет список всех компьютеров, в настоящее время использующих сетевой монитор для записи сетевых данных.</span><span class="sxs-lookup"><span data-stu-id="888d3-104">The **QueryStations** method provides a list of all computers currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="888d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="888d3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="888d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="888d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="888d3-107">*лпкуеритабле* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="888d3-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="888d3-108">Указатель на структуру [**куеритабле**](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="888d3-108">A pointer to a [**QUERYTABLE**](querytable.md) structure.</span></span> <span data-ttu-id="888d3-109">На входе эта структура должна содержать максимальное число компьютеров, которые сетевой монитор возвращать, и массив структур [**статионкуери**](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="888d3-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [**STATIONQUERY**](stationquery.md) structures.</span></span>

<span data-ttu-id="888d3-110">На выходе эта структура возвращает число компьютеров, записывающих данные, и структуру [**статионкуери**](stationquery.md) для каждого найденного компьютера.</span><span class="sxs-lookup"><span data-stu-id="888d3-110">On output, this structure returns the number of computers capturing data and a [**STATIONQUERY**](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="888d3-111">Имейте в виду, что это могут быть компьютеры, использующие версии сетевой монитор, которые имеют дату до версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="888d3-111">Be aware that this may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="888d3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="888d3-112">Return value</span></span>

<span data-ttu-id="888d3-113">Если метод выполнен успешно, возвращается значение **нмерр \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="888d3-113">If the method is successful, the return value is **NMERR\_SUCCESS**.</span></span>

<span data-ttu-id="888d3-114">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="888d3-114">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="888d3-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="888d3-115">Return code</span></span>                                                                                           | <span data-ttu-id="888d3-116">Описание</span><span class="sxs-lookup"><span data-stu-id="888d3-116">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="888d3-117"><dt>**НМЕРР \_ недостаточно \_ \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="888d3-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="888d3-118">Объем памяти, необходимый для обработки этого запроса, недоступен.</span><span class="sxs-lookup"><span data-stu-id="888d3-118">The memory required to process this query is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="888d3-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="888d3-119">Remarks</span></span>

<span data-ttu-id="888d3-120">Этот метод можно вызвать в любое время после вызова метода [**креатенппинтерфаце**](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="888d3-120">This method can be called at any time after the [**CreateNPPInterface**](createnppinterface.md) method is called.</span></span> <span data-ttu-id="888d3-121">Вызов этого метода является синхронным вызовом, который может занять несколько секунд, в то время как сетевой монитор ожидает ответа удаленных компьютеров на запрос.</span><span class="sxs-lookup"><span data-stu-id="888d3-121">A call to this method is a synchronous call, which may take several seconds to complete while Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="888d3-122">Можно запрашивать только компьютеры в локальной подсети.</span><span class="sxs-lookup"><span data-stu-id="888d3-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="888d3-123">Пользователь должен выделить память для структуры [**куеритабле**](querytable.md) и освободить память после того, как таблица больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="888d3-123">The user must allocate the memory for the [**QUERYTABLE**](querytable.md) structure and free that memory after the table is no longer required.</span></span> <span data-ttu-id="888d3-124">Это требование включает в себя память, необходимую для массива [**статионкуери**](stationquery.md) , используемого в **куеритабле**.</span><span class="sxs-lookup"><span data-stu-id="888d3-124">This requirement includes memory needed for the [**STATIONQUERY**](stationquery.md) array used in **QUERYTABLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="888d3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="888d3-125">Requirements</span></span>



| <span data-ttu-id="888d3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="888d3-126">Requirement</span></span> | <span data-ttu-id="888d3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="888d3-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="888d3-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="888d3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="888d3-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="888d3-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="888d3-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="888d3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="888d3-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="888d3-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="888d3-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="888d3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="888d3-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="888d3-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="888d3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="888d3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="888d3-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="888d3-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="888d3-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="888d3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888d3-137">**иртк**</span><span class="sxs-lookup"><span data-stu-id="888d3-137">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="888d3-138">**куеритабле**</span><span class="sxs-lookup"><span data-stu-id="888d3-138">**QUERYTABLE**</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="888d3-139">**статионкуери**</span><span class="sxs-lookup"><span data-stu-id="888d3-139">**STATIONQUERY**</span></span>](stationquery.md)
</dt> </dl>

 

 




