---
description: Метод Куеристатионс предоставляет список всех компьютеров, которые в данный момент записывают данные с помощью сетевой монитор.
ms.assetid: feebcb28-914b-450e-95d4-10a60cbf1438
title: 'Метод Истатс:: Куеристатионс (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 99c3be3926191c27ad038034373e411b5c22d9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081228"
---
# <a name="istatsquerystations-method"></a><span data-ttu-id="353ab-103">Метод Истатс:: Куеристатионс</span><span class="sxs-lookup"><span data-stu-id="353ab-103">IStats::QueryStations method</span></span>

<span data-ttu-id="353ab-104">Метод **куеристатионс** предоставляет список всех компьютеров, которые в данный момент записывают данные с помощью сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="353ab-104">The **QueryStations** method provides a list of all computers who are currently capturing data using Network Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="353ab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="353ab-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="353ab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="353ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="353ab-107">*лпкуеритабле* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="353ab-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="353ab-108">Указатель на структуру [куеритабле](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="353ab-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="353ab-109">На входе эта структура должна содержать максимальное число компьютеров, которые сетевой монитор возвращать, и массив структур [статионкуери](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="353ab-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="353ab-110">В выходных данных эта структура возвращает число компьютеров, которые записывают данные, и структуру [статионкуери](stationquery.md) для каждого найденного компьютера.</span><span class="sxs-lookup"><span data-stu-id="353ab-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="353ab-111">Обратите внимание, что эта информация может включать компьютеры, использующие версии сетевой монитор, которые имеют дату до версии 2,0.</span><span class="sxs-lookup"><span data-stu-id="353ab-111">Note that this information may include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="353ab-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="353ab-112">Return value</span></span>

<span data-ttu-id="353ab-113">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="353ab-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="353ab-114">Если метод завершился неудачно, возвращаемое значение является следующим кодом ошибки:</span><span class="sxs-lookup"><span data-stu-id="353ab-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="353ab-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="353ab-115">Return code</span></span>                                                                                           | <span data-ttu-id="353ab-116">Описание</span><span class="sxs-lookup"><span data-stu-id="353ab-116">Description</span></span>                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="353ab-117"><dt>**НМЕРР \_ недостаточно \_ \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="353ab-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="353ab-118">Объем памяти, необходимый для обработки этого запроса, был недоступен.</span><span class="sxs-lookup"><span data-stu-id="353ab-118">The memory required to process this query was unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="353ab-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="353ab-119">Remarks</span></span>

<span data-ttu-id="353ab-120">Этот метод можно вызвать в любое время после вызова [креатенппинтерфаце](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="353ab-120">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="353ab-121">Вызов этого метода является синхронным вызовом, выполнение которого может занять несколько секунд, так как сетевой монитор ожидает ответа удаленных компьютеров на запрос.</span><span class="sxs-lookup"><span data-stu-id="353ab-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="353ab-122">Можно запрашивать только компьютеры в локальной подсети.</span><span class="sxs-lookup"><span data-stu-id="353ab-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="353ab-123">Вы обязаны выделить память для структуры [куеритабле](querytable.md) и освободить память после того, как таблица больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="353ab-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="353ab-124">Это требование включает в себя память, необходимую для массива [статионкуери](stationquery.md) , используемого в куеритабле.</span><span class="sxs-lookup"><span data-stu-id="353ab-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="353ab-125">Требования</span><span class="sxs-lookup"><span data-stu-id="353ab-125">Requirements</span></span>



| <span data-ttu-id="353ab-126">Требование</span><span class="sxs-lookup"><span data-stu-id="353ab-126">Requirement</span></span> | <span data-ttu-id="353ab-127">Значение</span><span class="sxs-lookup"><span data-stu-id="353ab-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="353ab-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="353ab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="353ab-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="353ab-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="353ab-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="353ab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="353ab-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="353ab-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="353ab-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="353ab-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="353ab-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="353ab-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="353ab-134">DLL</span><span class="sxs-lookup"><span data-stu-id="353ab-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="353ab-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="353ab-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="353ab-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="353ab-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="353ab-137">истатс</span><span class="sxs-lookup"><span data-stu-id="353ab-137">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="353ab-138">куеритабле</span><span class="sxs-lookup"><span data-stu-id="353ab-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="353ab-139">статионкуери</span><span class="sxs-lookup"><span data-stu-id="353ab-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




