---
description: Метод Куеристатионс предоставляет список всех компьютеров, в настоящее время использующих сетевой монитор для сбора данных.
ms.assetid: 8e578f50-685e-4799-90ca-5da8810ec2a3
title: 'Метод Иделайдк:: Куеристатионс (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5a45f5046dbd2e5714424baf42621e0c1d5539ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682471"
---
# <a name="idelaydcquerystations-method"></a><span data-ttu-id="6b2be-103">Метод Иделайдк:: Куеристатионс</span><span class="sxs-lookup"><span data-stu-id="6b2be-103">IDelaydC::QueryStations method</span></span>

<span data-ttu-id="6b2be-104">Метод **куеристатионс** предоставляет список всех компьютеров, в настоящее время использующих сетевой монитор для сбора данных.</span><span class="sxs-lookup"><span data-stu-id="6b2be-104">The **QueryStations** method provides a list of all computers that are currently using Network Monitor to capture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b2be-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a><span data-ttu-id="6b2be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b2be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b2be-107">*лпкуеритабле* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6b2be-107">*lpQueryTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b2be-108">Указатель на структуру [куеритабле](querytable.md) .</span><span class="sxs-lookup"><span data-stu-id="6b2be-108">Pointer to a [QUERYTABLE](querytable.md) structure.</span></span> <span data-ttu-id="6b2be-109">На входе эта структура должна содержать максимальное число компьютеров, которые сетевой монитор возвращать, и массив структур [статионкуери](stationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="6b2be-109">On input, this structure must contain the maximum number of computers you want Network Monitor to return and an array of [STATIONQUERY](stationquery.md) structures.</span></span>

<span data-ttu-id="6b2be-110">В выходных данных эта структура возвращает число компьютеров, которые записывают данные, и структуру [статионкуери](stationquery.md) для каждого найденного компьютера.</span><span class="sxs-lookup"><span data-stu-id="6b2be-110">On output, this structure returns the number of computers that are capturing data and a [STATIONQUERY](stationquery.md) structure for each computer found.</span></span> <span data-ttu-id="6b2be-111">Обратите внимание, что этот список может включать компьютеры, использующие версии сетевой монитор с предустановленной версией 2,0.</span><span class="sxs-lookup"><span data-stu-id="6b2be-111">Note that this list might include computers using versions of Network Monitor that predate version 2.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b2be-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b2be-112">Return value</span></span>

<span data-ttu-id="6b2be-113">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6b2be-113">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6b2be-114">Если метод завершился неудачно, возвращаемое значение является следующим кодом ошибки:</span><span class="sxs-lookup"><span data-stu-id="6b2be-114">If the method is unsuccessful, the return value is the following error code:</span></span>



| <span data-ttu-id="6b2be-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6b2be-115">Return code</span></span>                                                                                           | <span data-ttu-id="6b2be-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6b2be-116">Description</span></span>                                               |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="6b2be-117"><dt>**НМЕРР \_ недостаточно \_ \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="6b2be-117"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="6b2be-118">Недостаточно памяти для обработки этого запроса.</span><span class="sxs-lookup"><span data-stu-id="6b2be-118">No memory was available to process this query.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b2be-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b2be-119">Remarks</span></span>

<span data-ttu-id="6b2be-120">Этот метод можно вызвать в любое время после вызова [креатенппинтерфаце](createnppinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="6b2be-120">This method can be called at any time after [CreateNPPInterface](createnppinterface.md) is called.</span></span> <span data-ttu-id="6b2be-121">Вызов этого метода является синхронным вызовом, выполнение которого может занять несколько секунд, так как сетевой монитор ожидает ответа удаленных компьютеров на запрос.</span><span class="sxs-lookup"><span data-stu-id="6b2be-121">A call to this method is a synchronous call, which may take several seconds to complete as Network Monitor waits for remote computers to respond to the query.</span></span> <span data-ttu-id="6b2be-122">Можно запрашивать только компьютеры в локальной подсети.</span><span class="sxs-lookup"><span data-stu-id="6b2be-122">Only computers on the local subnet can be queried.</span></span>

<span data-ttu-id="6b2be-123">Вы обязаны выделить память для структуры [куеритабле](querytable.md) и освободить память после того, как таблица больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="6b2be-123">It is your responsibility to allocate the memory for the [QUERYTABLE](querytable.md) structure and free that memory after the table is no longer needed.</span></span> <span data-ttu-id="6b2be-124">Это требование включает в себя память, необходимую для массива [статионкуери](stationquery.md) , используемого в куеритабле.</span><span class="sxs-lookup"><span data-stu-id="6b2be-124">This requirement includes the memory needed for the [STATIONQUERY](stationquery.md) array used in QUERYTABLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b2be-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6b2be-125">Requirements</span></span>



| <span data-ttu-id="6b2be-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6b2be-126">Requirement</span></span> | <span data-ttu-id="6b2be-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6b2be-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2be-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b2be-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6b2be-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b2be-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6b2be-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b2be-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6b2be-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6b2be-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6b2be-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6b2be-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b2be-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b2be-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6b2be-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6b2be-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b2be-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b2be-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b2be-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b2be-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2be-137">иделайдк</span><span class="sxs-lookup"><span data-stu-id="6b2be-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="6b2be-138">куеритабле</span><span class="sxs-lookup"><span data-stu-id="6b2be-138">QUERYTABLE</span></span>](querytable.md)
</dt> <dt>

[<span data-ttu-id="6b2be-139">статионкуери</span><span class="sxs-lookup"><span data-stu-id="6b2be-139">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




