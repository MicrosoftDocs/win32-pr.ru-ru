---
description: Функция Креатепропертидатабасе создает базу данных свойств, в которой хранятся свойства протокола.
ms.assetid: 0a3be6ae-d7ce-4315-b4f2-b46bcfa25b69
title: Функция Креатепропертидатабасе (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2955aa3367648c4e9e23fd748fa27d6343ef78a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673642"
---
# <a name="createpropertydatabase-function"></a><span data-ttu-id="1036b-103">Функция Креатепропертидатабасе</span><span class="sxs-lookup"><span data-stu-id="1036b-103">CreatePropertyDatabase function</span></span>

<span data-ttu-id="1036b-104">Функция **креатепропертидатабасе** создает базу данных свойств, в которой хранятся свойства протокола.</span><span class="sxs-lookup"><span data-stu-id="1036b-104">The **CreatePropertyDatabase** function creates a property database that stores the properties of a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="1036b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1036b-105">Syntax</span></span>


```C++
DWORD WINAPI CreatePropertyDatabase(
  _In_ HPROTOCOL hProtocol,
  _In_ DWORD     nProperties
);
```



## <a name="parameters"></a><span data-ttu-id="1036b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1036b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1036b-107">*хпротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1036b-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1036b-108">Маркер протокола, связанного с базой данных.</span><span class="sxs-lookup"><span data-stu-id="1036b-108">Handle of the protocol that is associated with the database.</span></span> <span data-ttu-id="1036b-109">Когда сетевой монитор вызывает функцию [Register](register-parser.md) , сетевой монитор передает этот маркер протоколу в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="1036b-109">When Network Monitor calls the [Register](register-parser.md) function, Network Monitor passes the protocol handle to the parser DLL.</span></span>

</dd> <dt>

<span data-ttu-id="1036b-110">*нпропертиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1036b-110">*nProperties* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1036b-111">Число свойств, хранящихся в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1036b-111">Number of properties stored in the database.</span></span> <span data-ttu-id="1036b-112">Задайте для этого параметра количество свойств, поддерживаемых протоколом.</span><span class="sxs-lookup"><span data-stu-id="1036b-112">Set this parameter to the number of properties that the protocol supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1036b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1036b-113">Return value</span></span>

<span data-ttu-id="1036b-114">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1036b-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1036b-115">Если функция завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="1036b-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="1036b-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1036b-116">Return code</span></span>                                                                                             | <span data-ttu-id="1036b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1036b-117">Description</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1036b-118"><dt>**\_Внутренняя \_ Ошибка нмерр**</dt></span><span class="sxs-lookup"><span data-stu-id="1036b-118"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="1036b-119">Произошла внутренняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="1036b-119">An internal error has occurred.</span></span><br/>                                     |
| <dl> <span data-ttu-id="1036b-120"><dt>**НМЕРР \_ недопустимое \_ хпотокол**</dt></span><span class="sxs-lookup"><span data-stu-id="1036b-120"><dt>**NMERR\_INVALID\_HPOTOCOL**</dt></span></span> </dl> | <span data-ttu-id="1036b-121">Недопустимый обработчик для протокола, указанного в *хпротокол* .</span><span class="sxs-lookup"><span data-stu-id="1036b-121">The handle to the protocol specified in *hProtocol* is invalid.</span></span><br/>     |
| <dl> <span data-ttu-id="1036b-122"><dt>**НМЕРР \_ недостаточно \_ \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="1036b-122"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="1036b-123">Сетевой монитор не хватает памяти для создания базы данных.</span><span class="sxs-lookup"><span data-stu-id="1036b-123">Network Monitor does not have enough memory to create the database.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1036b-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1036b-124">Remarks</span></span>

<span data-ttu-id="1036b-125">Функция **креатепропертидатабасе** должна вызываться только при реализации функции [Register](register-parser.md) .</span><span class="sxs-lookup"><span data-stu-id="1036b-125">The **CreatePropertyDatabase** function should be called only when implementing the [Register](register-parser.md) function.</span></span> <span data-ttu-id="1036b-126">Средство синтаксического анализа использует **креатепропертидатабасе** для создания базы данных свойств, описывающей свойства протокола.</span><span class="sxs-lookup"><span data-stu-id="1036b-126">The parser uses **CreatePropertyDatabase** to create a property database that describes the properties of a protocol.</span></span> <span data-ttu-id="1036b-127">Сетевой монитор использует базу данных для интерпретации информации в протоколе.</span><span class="sxs-lookup"><span data-stu-id="1036b-127">Network Monitor uses the database to interpret the information within the protocol.</span></span>

<span data-ttu-id="1036b-128">Функция **креатепропертидатабасе** выделяет структуры, которые сетевой монитор должны поддерживать базу данных свойств.</span><span class="sxs-lookup"><span data-stu-id="1036b-128">The **CreatePropertyDatabase** function allocates the structures that Network Monitor needs to maintain a property database.</span></span>

## <a name="requirements"></a><span data-ttu-id="1036b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="1036b-129">Requirements</span></span>



| <span data-ttu-id="1036b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="1036b-130">Requirement</span></span> | <span data-ttu-id="1036b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="1036b-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1036b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1036b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1036b-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1036b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1036b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1036b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1036b-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1036b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1036b-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1036b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1036b-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1036b-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1036b-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1036b-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="1036b-139"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1036b-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1036b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1036b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1036b-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1036b-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1036b-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1036b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1036b-143">Зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="1036b-143">Register</span></span>](register-parser.md)
</dt> </dl>

 

 




