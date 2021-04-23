---
description: Функция "отменить регистрацию экспорта" освобождает ресурсы, используемые для создания базы данных свойств протокола. Библиотека DLL средства синтаксического анализа должна реализовывать отмену регистрации.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Отменить регистрацию функции обратного вызова (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264368"
---
# <a name="deregister-callback-function"></a><span data-ttu-id="befcf-104">Отменить регистрацию функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="befcf-104">Deregister callback function</span></span>

<span data-ttu-id="befcf-105">Функция " **отменить регистрацию** экспорта" освобождает ресурсы, используемые для создания [*базы данных свойств*](p.md)протокола.</span><span class="sxs-lookup"><span data-stu-id="befcf-105">The **Deregister** export function frees the resources used to create the protocol [*property database*](p.md).</span></span> <span data-ttu-id="befcf-106">Библиотека DLL средства синтаксического анализа должна реализовывать **отмену регистрации**.</span><span class="sxs-lookup"><span data-stu-id="befcf-106">The parser DLL must implement **Deregister**.</span></span>

## <a name="syntax"></a><span data-ttu-id="befcf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="befcf-107">Syntax</span></span>


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="befcf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="befcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="befcf-109">*хпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="befcf-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="befcf-110">Маркер протокола для определенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="befcf-110">Handle of the protocol for a specific database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="befcf-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="befcf-111">Return value</span></span>

<span data-ttu-id="befcf-112">Нет.</span><span class="sxs-lookup"><span data-stu-id="befcf-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="befcf-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="befcf-113">Remarks</span></span>

<span data-ttu-id="befcf-114">Сетевой монитор вызывает метод **Unregister** после передачи всех сведений о записи в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="befcf-114">Network Monitor calls **Deregister** after passing all the capture information to the parser DLL.</span></span> <span data-ttu-id="befcf-115">Библиотека DLL средства синтаксического анализа должна реализовать функцию **дерегистрации** для каждого протокола, поддерживаемого средством синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="befcf-115">The parser DLL must implement a **Deregister** function for each protocol that the parser supports.</span></span>

<span data-ttu-id="befcf-116">При реализации **отмены регистрации** библиотека DLL средства синтаксического анализа должна вызывать функцию [дестройпропертидатабасе](destroypropertydatabase.md) для освобождения ресурсов [*базы данных свойств*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="befcf-116">When implementing **Deregister**, the parser DLL must call the [DestroyPropertyDatabase](destroypropertydatabase.md) function to release the [*property database*](p.md) resources.</span></span>



| <span data-ttu-id="befcf-117">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="befcf-117">For information on</span></span>                                        | <span data-ttu-id="befcf-118">См.</span><span class="sxs-lookup"><span data-stu-id="befcf-118">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="befcf-119">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="befcf-119">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="befcf-120">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="befcf-120">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="befcf-121">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="befcf-121">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="befcf-122">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="befcf-122">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="befcf-123">Реализация **отмены регистрации**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="befcf-123">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="befcf-124">Реализация отмены регистрации</span><span class="sxs-lookup"><span data-stu-id="befcf-124">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="befcf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="befcf-125">Requirements</span></span>



| <span data-ttu-id="befcf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="befcf-126">Requirement</span></span> | <span data-ttu-id="befcf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="befcf-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="befcf-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="befcf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="befcf-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="befcf-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="befcf-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="befcf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="befcf-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="befcf-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="befcf-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="befcf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="befcf-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="befcf-133"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="befcf-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="befcf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befcf-135">дестройпропертидатабасе</span><span class="sxs-lookup"><span data-stu-id="befcf-135">DestroyPropertyDatabase</span></span>](destroypropertydatabase.md)
</dt> </dl>

 

 




