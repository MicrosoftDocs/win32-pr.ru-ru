---
description: Функция регистрации экспорта должна быть реализована во всех библиотеках DLL средства синтаксического анализа. Реализация Register создает и заполняет базу данных свойств для протокола. Сетевой монитор использует базу данных для определения свойств, поддерживаемых протоколом.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Регистрация функции обратного вызова средства синтаксического анализа (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673548"
---
# <a name="register-parser-callback-function"></a><span data-ttu-id="9c97e-105">Регистрация функции обратного вызова средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="9c97e-105">Register Parser callback function</span></span>

<span data-ttu-id="9c97e-106">Функция **регистрации** экспорта должна быть реализована во всех библиотеках DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="9c97e-106">The **Register** export function must be implemented in all parser DLLs.</span></span> <span data-ttu-id="9c97e-107">Реализация **Register** создает и заполняет [*базу данных свойств*](p.md) для протокола.</span><span class="sxs-lookup"><span data-stu-id="9c97e-107">The implementation of **Register** creates and fills-in a [*property database*](p.md) for a protocol.</span></span> <span data-ttu-id="9c97e-108">Сетевой монитор использует базу данных для определения свойств, поддерживаемых протоколом.</span><span class="sxs-lookup"><span data-stu-id="9c97e-108">Network Monitor uses the database to determine which properties the protocol supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c97e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c97e-109">Syntax</span></span>


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="9c97e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c97e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c97e-111">*хпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c97e-111">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c97e-112">Маркер протокола, который сетевой монитор предоставляет при вызове **Register**.</span><span class="sxs-lookup"><span data-stu-id="9c97e-112">The handle of the protocol that Network Monitor provides when calling **Register**.</span></span> <span data-ttu-id="9c97e-113">При вызове вспомогательных функций экспорта требуется обработчик *хпротокол* .</span><span class="sxs-lookup"><span data-stu-id="9c97e-113">The *hProtocol* handle is needed when calling export helper functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c97e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c97e-114">Return value</span></span>

<span data-ttu-id="9c97e-115">Нет.</span><span class="sxs-lookup"><span data-stu-id="9c97e-115">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c97e-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="9c97e-116">Remarks</span></span>

<span data-ttu-id="9c97e-117">Сетевой монитор начинает вызывать функцию **Register** сразу после загрузки записи.</span><span class="sxs-lookup"><span data-stu-id="9c97e-117">Network Monitor starts calling the **Register** function as soon as a capture is loaded.</span></span> <span data-ttu-id="9c97e-118">Сетевой монитор вызывает функцию **Register** для каждого протокола, который он может опознать.</span><span class="sxs-lookup"><span data-stu-id="9c97e-118">Network Monitor calls the **Register** function for each protocol it can identify.</span></span> <span data-ttu-id="9c97e-119">Функция [креатепротокол](createprotocol.md) передает указатель на функцию **Register** .</span><span class="sxs-lookup"><span data-stu-id="9c97e-119">The [CreateProtocol](createprotocol.md) function passes a pointer to the **Register** function.</span></span>

<span data-ttu-id="9c97e-120">Реализация **Register** включает в себя вызовы следующих функций.</span><span class="sxs-lookup"><span data-stu-id="9c97e-120">The implementation of **Register** includes calls to the following functions.</span></span>

-   <span data-ttu-id="9c97e-121">Вызов функций [креатепропертидатабасе](createpropertydatabase.md) и [AddProperty](/previous-versions/bb251873(v=msdn.10)) для создания базы данных всех свойств, поддерживаемых протоколом.</span><span class="sxs-lookup"><span data-stu-id="9c97e-121">A call to the [CreatePropertyDatabase](createpropertydatabase.md) and [AddProperty](/previous-versions/bb251873(v=msdn.10)) functions to create a database of all the properties that the protocol supports.</span></span>
-   <span data-ttu-id="9c97e-122">Вызов функции [креатехандоффтабле](createhandofftable.md) требуется, если протокол использует [*переданный набор*](h.md).</span><span class="sxs-lookup"><span data-stu-id="9c97e-122">A call to the [CreateHandoffTable](createhandofftable.md) function is required if the protocol uses a [*handoff set*](h.md).</span></span>

<span data-ttu-id="9c97e-123">Если DLL-файл средства синтаксического анализа содержит несколько синтаксических анализаторов и средство синтаксического анализа может обнаружить более одного протокола, необходимо реализовать функцию **Register** для каждого протокола.</span><span class="sxs-lookup"><span data-stu-id="9c97e-123">If the parser DLL contains multiple parsers, and the parser can detect more than one protocol, you must implement a **Register** function for each protocol.</span></span>



| <span data-ttu-id="9c97e-124">Дополнительные сведения о</span><span class="sxs-lookup"><span data-stu-id="9c97e-124">For Information on</span></span>                                        | <span data-ttu-id="9c97e-125">См.</span><span class="sxs-lookup"><span data-stu-id="9c97e-125">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="9c97e-126">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="9c97e-126">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="9c97e-127">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="9c97e-127">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="9c97e-128">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="9c97e-128">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="9c97e-129">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="9c97e-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="9c97e-130">Реализация **регистра**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="9c97e-130">How to implement **Register**  includes an example.</span></span>       | [<span data-ttu-id="9c97e-131">Реализация регистра</span><span class="sxs-lookup"><span data-stu-id="9c97e-131">Implementing Register</span></span>](implementing-register.md)     |



 

## <a name="requirements"></a><span data-ttu-id="9c97e-132">Требования</span><span class="sxs-lookup"><span data-stu-id="9c97e-132">Requirements</span></span>



| <span data-ttu-id="9c97e-133">Требование</span><span class="sxs-lookup"><span data-stu-id="9c97e-133">Requirement</span></span> | <span data-ttu-id="9c97e-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9c97e-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9c97e-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c97e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9c97e-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c97e-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9c97e-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c97e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9c97e-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9c97e-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9c97e-139">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9c97e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c97e-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c97e-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c97e-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c97e-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c97e-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9c97e-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="9c97e-143">креатехандоффтабле</span><span class="sxs-lookup"><span data-stu-id="9c97e-143">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> <dt>

[<span data-ttu-id="9c97e-144">креатепропертидатабасе</span><span class="sxs-lookup"><span data-stu-id="9c97e-144">CreatePropertyDatabase</span></span>](createpropertydatabase.md)
</dt> <dt>

[<span data-ttu-id="9c97e-145">креатепротокол</span><span class="sxs-lookup"><span data-stu-id="9c97e-145">CreateProtocol</span></span>](createprotocol.md)
</dt> </dl>

 

