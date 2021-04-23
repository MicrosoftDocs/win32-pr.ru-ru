---
description: Функция Дестройпропертидатабасе освобождает ресурсы, используемые для создания базы данных свойств протокола.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: Функция Дестройпропертидатабасе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999399"
---
# <a name="destroypropertydatabase-function"></a><span data-ttu-id="e81c4-103">Функция Дестройпропертидатабасе</span><span class="sxs-lookup"><span data-stu-id="e81c4-103">DestroyPropertyDatabase function</span></span>

<span data-ttu-id="e81c4-104">Функция **дестройпропертидатабасе** освобождает ресурсы, используемые для создания [*базы данных свойств*](p.md)протокола.</span><span class="sxs-lookup"><span data-stu-id="e81c4-104">The **DestroyPropertyDatabase** function releases the resources used to create the protocol [*property database*](p.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e81c4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e81c4-105">Syntax</span></span>


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="e81c4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e81c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e81c4-107">*хпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e81c4-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e81c4-108">Обработчик для уничтожения базы данных свойств.</span><span class="sxs-lookup"><span data-stu-id="e81c4-108">Handle to the property database to be destroyed.</span></span> <span data-ttu-id="e81c4-109">Этот маркер передается в библиотеку DLL средства синтаксического анализа, когда сетевой монитор вызывает функцию [дерегистрации](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="e81c4-109">The handle is passed to the parser DLL when Network Monitor calls the [Deregister](deregister.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e81c4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e81c4-110">Return value</span></span>

<span data-ttu-id="e81c4-111">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e81c4-111">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e81c4-112">Если функция завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="e81c4-112">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="e81c4-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e81c4-113">Return code</span></span>                                                                                              | <span data-ttu-id="e81c4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e81c4-114">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="e81c4-115"><dt>**\_Внутренняя \_ Ошибка нмерр**</dt></span><span class="sxs-lookup"><span data-stu-id="e81c4-115"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="e81c4-116">Внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="e81c4-116">An internal error occurred.</span></span> <br/>    |
| <dl> <span data-ttu-id="e81c4-117"><dt>**НМЕРР \_ недопустимое \_ хпротокол**</dt></span><span class="sxs-lookup"><span data-stu-id="e81c4-117"><dt>**NMERR\_INVALID\_HPROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="e81c4-118">Недопустимый маркер в *хпротокол*.</span><span class="sxs-lookup"><span data-stu-id="e81c4-118">Invalid handle in *hProtocol*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="e81c4-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e81c4-119">Remarks</span></span>

<span data-ttu-id="e81c4-120">Функцию **дестройпропертидатабасе** следует вызывать только при реализации функции [дерегистрации](deregister.md) экспорта для протокола.</span><span class="sxs-lookup"><span data-stu-id="e81c4-120">The **DestroyPropertyDatabase** function should be called only when implementing the [Deregister](deregister.md) export function for the protocol.</span></span> <span data-ttu-id="e81c4-121">Для библиотек DLL синтаксического анализатора, поддерживающих несколько протоколов, функция **дестройпропертидатабасе** вызывается для каждой реализации **отмены регистрации**.</span><span class="sxs-lookup"><span data-stu-id="e81c4-121">For parser DLLs that support multiple protocols, the **DestroyPropertyDatabase** function is called for each implementation of **Deregister**.</span></span>



| <span data-ttu-id="e81c4-122">Для получения информации о</span><span class="sxs-lookup"><span data-stu-id="e81c4-122">For information on</span></span>                                        | <span data-ttu-id="e81c4-123">См.</span><span class="sxs-lookup"><span data-stu-id="e81c4-123">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="e81c4-124">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="e81c4-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="e81c4-125">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="e81c4-125">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="e81c4-126">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="e81c4-126">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="e81c4-127">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="e81c4-127">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="e81c4-128">Реализация **отмены регистрации**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="e81c4-128">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="e81c4-129">Реализация отмены регистрации</span><span class="sxs-lookup"><span data-stu-id="e81c4-129">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="e81c4-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e81c4-130">Requirements</span></span>



| <span data-ttu-id="e81c4-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e81c4-131">Requirement</span></span> | <span data-ttu-id="e81c4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e81c4-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e81c4-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e81c4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e81c4-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e81c4-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e81c4-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e81c4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e81c4-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e81c4-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e81c4-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e81c4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e81c4-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e81c4-138"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e81c4-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e81c4-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="e81c4-140"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e81c4-140"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e81c4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e81c4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e81c4-142"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e81c4-142"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e81c4-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e81c4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e81c4-144">Отмена регистрации</span><span class="sxs-lookup"><span data-stu-id="e81c4-144">Deregister</span></span>](deregister.md)
</dt> </dl>

 

 




