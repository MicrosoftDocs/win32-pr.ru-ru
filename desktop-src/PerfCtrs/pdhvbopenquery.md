---
description: Функция Пдхвбопенкуери создает и инициализирует уникальную структуру запроса, которая используется для управления сбором данных о производительности.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: Функция Пдхвбопенкуери
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156523"
---
# <a name="pdhvbopenquery-function"></a><span data-ttu-id="ae9ff-103">Функция Пдхвбопенкуери</span><span class="sxs-lookup"><span data-stu-id="ae9ff-103">PdhVbOpenQuery function</span></span>

<span data-ttu-id="ae9ff-104">Функция **пдхвбопенкуери** создает и инициализирует уникальную структуру запроса, которая используется для управления сбором данных о производительности.</span><span class="sxs-lookup"><span data-stu-id="ae9ff-104">The **PdhVbOpenQuery** function creates and initializes a unique query structure that is used to manage the collection of performance data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae9ff-105">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="ae9ff-105">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="ae9ff-106">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ae9ff-106">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="ae9ff-107">Функция Пдхвбопенкуери ( \_ ByVal Куерихандле как long \_ )</span><span class="sxs-lookup"><span data-stu-id="ae9ff-107">Function PdhVbOpenQuery( \_ ByVal QueryHandle As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="ae9ff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae9ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae9ff-109">*куерихандле*</span><span class="sxs-lookup"><span data-stu-id="ae9ff-109">*QueryHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="ae9ff-110">Переменная, которая была удалена (равна 0) перед вызовом функции и, если функция выполнена успешно, содержит уникальный идентификатор созданного и открытого запроса.</span><span class="sxs-lookup"><span data-stu-id="ae9ff-110">Variable that is cleared (equals 0) before the function is called and, if the function is successful, contains the unique ID of the query that is created and opened.</span></span> <span data-ttu-id="ae9ff-111">Этот маркер используется при последующих вызовах других функций PDH для обнаружения запроса.</span><span class="sxs-lookup"><span data-stu-id="ae9ff-111">This handle is used in the subsequent calls to other PDH functions to identify the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae9ff-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae9ff-112">Return value</span></span>

<span data-ttu-id="ae9ff-113">Если функция завершается успешно, она возвращает **длинное** целое число, равное \_ успешному выполнению, и новый маркер в переменной *куерихандле* .</span><span class="sxs-lookup"><span data-stu-id="ae9ff-113">If the function succeeds, it returns a **Long** integer equal to ERROR\_SUCCESS and a new handle in the *QueryHandle* variable.</span></span>

<span data-ttu-id="ae9ff-114">Если функция завершается ошибкой, возвращаемое значение является [кодом системной ошибки](/windows/desktop/Debug/system-error-codes) или [кодом ошибки PDH](pdh-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ae9ff-114">If the function fails, the return value is a [system error code](/windows/desktop/Debug/system-error-codes) or a [PDH error code](pdh-error-codes.md).</span></span> <span data-ttu-id="ae9ff-115">Ниже приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="ae9ff-115">The following are possible values.</span></span>



| <span data-ttu-id="ae9ff-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ae9ff-116">Return code</span></span>                                                                                                     | <span data-ttu-id="ae9ff-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ae9ff-117">Description</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="ae9ff-118"><dt>**\_Недопустимый \_ аргумент PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ff-118"><dt>**PDH\_INVALID\_ARGUMENT**</dt></span></span> </dl>           | <span data-ttu-id="ae9ff-119">Аргумент является недопустимым или неверным.</span><span class="sxs-lookup"><span data-stu-id="ae9ff-119">The argument is invalid or incorrect.</span></span><br/>             |
| <dl> <span data-ttu-id="ae9ff-120"><dt>**\_ \_ сбой выделения памяти \_ PDH**</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ff-120"><dt>**PDH\_MEMORY\_ALLOCATION\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="ae9ff-121">Не удалось выделить временный буфер памяти.</span><span class="sxs-lookup"><span data-stu-id="ae9ff-121">A temporary memory buffer could not be allocated.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ae9ff-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ae9ff-122">Requirements</span></span>



| <span data-ttu-id="ae9ff-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ae9ff-123">Requirement</span></span> | <span data-ttu-id="ae9ff-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ae9ff-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9ff-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae9ff-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ae9ff-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ae9ff-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae9ff-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae9ff-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ae9ff-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae9ff-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ae9ff-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ae9ff-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae9ff-130"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ff-130"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="ae9ff-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ae9ff-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae9ff-132"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae9ff-132"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae9ff-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae9ff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9ff-134">**пдхклосекуери**</span><span class="sxs-lookup"><span data-stu-id="ae9ff-134">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

