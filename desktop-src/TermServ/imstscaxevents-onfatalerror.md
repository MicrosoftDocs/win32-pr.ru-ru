---
title: Имстскаксевентс Онфаталеррор, метод
description: Вызывается, когда клиентский элемент управления обнаруживает неустранимую ошибку.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онфаталеррор
- Службы удаленных рабочих столов метода Онфаталеррор, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онфаталеррор
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892201"
---
# <a name="imstscaxeventsonfatalerror-method"></a><span data-ttu-id="1d2cc-106">Метод Имстскаксевентс:: Онфаталеррор</span><span class="sxs-lookup"><span data-stu-id="1d2cc-106">IMsTscAxEvents::OnFatalError method</span></span>

<span data-ttu-id="1d2cc-107">Вызывается, когда клиентский элемент управления обнаруживает неустранимую ошибку.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-107">Called when the client control encounters a fatal error.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d2cc-108">Syntax</span></span>


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="1d2cc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d2cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d2cc-110">*код ошибки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1d2cc-110">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2cc-111">Указывает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-111">Indicates the error code.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="1d2cc-112"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="1d2cc-113">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-113">An unknown error has occurred.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="1d2cc-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="1d2cc-115">Код внутренней ошибки 1.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-115">Internal error code 1.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="1d2cc-116"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="1d2cc-117">Произошла ошибка нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-117">An out-of-memory error has occurred.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="1d2cc-118"><span id="3"></span>**3-5**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-118"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="1d2cc-119">Произошла ошибка при создании окна.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-119">A window-creation error has occurred.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="1d2cc-120"><span id="4"></span>**четырех**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-120"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="1d2cc-121">Код внутренней ошибки 2.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-121">Internal error code 2.</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="1d2cc-122"><span id="5"></span>**5.0**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-122"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="1d2cc-123">Код внутренней ошибки 3.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-123">Internal error code 3.</span></span> <span data-ttu-id="1d2cc-124">Это недопустимое состояние.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-124">This is not a valid state.</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="1d2cc-125"><span id="6"></span>**1-6**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-125"><span id="6"></span>**6**</span></span>


</dt> <dd>

<span data-ttu-id="1d2cc-126">Код внутренней ошибки 4.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-126">Internal error code 4.</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="1d2cc-127"><span id="7"></span>**7**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-127"><span id="7"></span>**7**</span></span>


</dt> <dd>

<span data-ttu-id="1d2cc-128">Во время подключения клиента произошла неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-128">An unrecoverable error has occurred during client connection.</span></span>

</dd> <dt>

<span id="100"></span>

<span data-ttu-id="1d2cc-129"><span id="100"></span>**100**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-129"><span id="100"></span>**100**</span></span>


</dt> <dd>

<span data-ttu-id="1d2cc-130">Ошибка инициализации Winsock.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-130">Winsock initialization error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d2cc-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d2cc-131">Return value</span></span>

<span data-ttu-id="1d2cc-132">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-132">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d2cc-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d2cc-133">Remarks</span></span>

<span data-ttu-id="1d2cc-134">В ответ на это событие контейнер отображает сообщение об ошибке и завершает работу.</span><span class="sxs-lookup"><span data-stu-id="1d2cc-134">In response to this event, the container displays an error message and shuts down.</span></span>

<span data-ttu-id="1d2cc-135">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1d2cc-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2cc-136">Требования</span><span class="sxs-lookup"><span data-stu-id="1d2cc-136">Requirements</span></span>



| <span data-ttu-id="1d2cc-137">Требование</span><span class="sxs-lookup"><span data-stu-id="1d2cc-137">Requirement</span></span> | <span data-ttu-id="1d2cc-138">Значение</span><span class="sxs-lookup"><span data-stu-id="1d2cc-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2cc-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d2cc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2cc-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d2cc-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1d2cc-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d2cc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2cc-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d2cc-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1d2cc-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1d2cc-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="1d2cc-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2cc-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d2cc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1d2cc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d2cc-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2cc-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1d2cc-147">IID</span><span class="sxs-lookup"><span data-stu-id="1d2cc-147">IID</span></span><br/>                      | <span data-ttu-id="1d2cc-148">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="1d2cc-148">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="1d2cc-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d2cc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2cc-150">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="1d2cc-150">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





