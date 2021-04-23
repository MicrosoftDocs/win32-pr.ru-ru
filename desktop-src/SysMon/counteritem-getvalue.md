---
title: Каунтеритем. GetValue, метод
description: Извлекает Последнее значение счетчика.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- Метод GetValue Сисмон
- Метод GetValue Сисмон, класс Каунтеритем
- Класс Каунтеритем Сисмон, метод GetValue
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661955"
---
# <a name="counteritemgetvalue-method"></a><span data-ttu-id="a9e13-106">Каунтеритем. GetValue, метод</span><span class="sxs-lookup"><span data-stu-id="a9e13-106">CounterItem.GetValue method</span></span>

<span data-ttu-id="a9e13-107">Извлекает Последнее значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="a9e13-107">Retrieves the last value of the counter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9e13-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9e13-108">Syntax</span></span>


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a><span data-ttu-id="a9e13-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9e13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9e13-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a9e13-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e13-111">Последнее значение выборки счетчика.</span><span class="sxs-lookup"><span data-stu-id="a9e13-111">Last sampled value of the counter.</span></span>

</dd> <dt>

<span data-ttu-id="a9e13-112">*состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a9e13-112">*status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e13-113">Указывает, является ли значение допустимым.</span><span class="sxs-lookup"><span data-stu-id="a9e13-113">Indicates if the value is valid.</span></span>



| <span data-ttu-id="a9e13-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a9e13-114">Value</span></span>                                                                                              | <span data-ttu-id="a9e13-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a9e13-115">Meaning</span></span>                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="a9e13-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9e13-116"><dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a9e13-117">Значение является допустимым.</span><span class="sxs-lookup"><span data-stu-id="a9e13-117">The value is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="a9e13-118"><dt>0xC0000BBA (3221228474)</dt></span><span class="sxs-lookup"><span data-stu-id="a9e13-118"><dt>0xC0000BBA (3221228474)</dt></span></span> </dl> | <span data-ttu-id="a9e13-119">Недопустимое значение.</span><span class="sxs-lookup"><span data-stu-id="a9e13-119">The value is not valid.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9e13-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9e13-120">Return value</span></span>

<span data-ttu-id="a9e13-121">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a9e13-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9e13-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9e13-122">Remarks</span></span>

<span data-ttu-id="a9e13-123">Если источником данных счетчика является файл журнала, значение является последним значением счетчика в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="a9e13-123">If the source of the counter data is from a log file, the value is the last counter value in the log file.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9e13-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a9e13-124">Requirements</span></span>



| <span data-ttu-id="a9e13-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a9e13-125">Requirement</span></span> | <span data-ttu-id="a9e13-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a9e13-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e13-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9e13-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a9e13-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9e13-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a9e13-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9e13-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a9e13-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9e13-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9e13-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a9e13-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9e13-132"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a9e13-132"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9e13-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9e13-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9e13-134">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="a9e13-134">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="a9e13-135">**Каунтеритем. статистики**</span><span class="sxs-lookup"><span data-stu-id="a9e13-135">**CounterItem.GetStatistics**</span></span>](counteritem-getstatistics.md)
</dt> <dt>

[<span data-ttu-id="a9e13-136">**Каунтеритем. Value**</span><span class="sxs-lookup"><span data-stu-id="a9e13-136">**CounterItem.Value**</span></span>](counteritem-value.md)
</dt> </dl>

 

 





