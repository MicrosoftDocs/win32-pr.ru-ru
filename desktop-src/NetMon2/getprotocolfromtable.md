---
description: Функция Жетпротоколфромтабле возвращает маркер для протокола&\# 8212; на основе заданной переданной таблицы и значения.
ms.assetid: 34b07079-0b20-40d8-a529-4179ecc68ebf
title: Функция Жетпротоколфромтабле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 498892fc2cc5ada2e177b8fb3f70f40a1ef10dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990896"
---
# <a name="getprotocolfromtable-function"></a><span data-ttu-id="5496c-103">Функция Жетпротоколфромтабле</span><span class="sxs-lookup"><span data-stu-id="5496c-103">GetProtocolFromTable function</span></span>

<span data-ttu-id="5496c-104">Функция **жетпротоколфромтабле** возвращает маркер для протокола на основе заданной переданной таблицы и значения.</span><span class="sxs-lookup"><span data-stu-id="5496c-104">The **GetProtocolFromTable** function returns a handle to a protocol based on a given handoff table and value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5496c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5496c-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromTable(
  _In_  LPHANDOFFTABLE hTable,
  _In_  DWORD          ItemToFind,
  _Out_ PDWORD_PTR     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="5496c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5496c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5496c-107">*хтабле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5496c-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5496c-108">Обработчик для переданной таблицы.</span><span class="sxs-lookup"><span data-stu-id="5496c-108">Handle to a handoff table.</span></span>

</dd> <dt>

<span data-ttu-id="5496c-109">*Итемтофинд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5496c-109">*ItemToFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5496c-110">Значение, используемое для нахождение протокола в таблице передачи.</span><span class="sxs-lookup"><span data-stu-id="5496c-110">Value used to locate the protocol in a handoff table.</span></span> <span data-ttu-id="5496c-111">Значение должно быть доступно в данных протокола.</span><span class="sxs-lookup"><span data-stu-id="5496c-111">The value must be available in the protocol data.</span></span>

</dd> <dt>

<span data-ttu-id="5496c-112">*лпинстдата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5496c-112">*lpInstData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5496c-113">При наличии в таблице передачи данные экземпляра для следующего протокола.</span><span class="sxs-lookup"><span data-stu-id="5496c-113">If available in the handoff table, instance data for the next protocol.</span></span> <span data-ttu-id="5496c-114">Длина данных экземпляра не может превышать значение типа DWORD \_ .</span><span class="sxs-lookup"><span data-stu-id="5496c-114">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5496c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5496c-115">Return value</span></span>

<span data-ttu-id="5496c-116">Если функция выполнена успешно, возвращаемое значение является маркером протокола.</span><span class="sxs-lookup"><span data-stu-id="5496c-116">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="5496c-117">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="5496c-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5496c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5496c-118">Remarks</span></span>

<span data-ttu-id="5496c-119">При реализации функции экспорта [рекогнизефраме](recognizeframe.md) функция **жетпротоколфромтабле** используется для получения маркера для следующего протокола.</span><span class="sxs-lookup"><span data-stu-id="5496c-119">When implementing the [RecognizeFrame](recognizeframe.md) export function, the **GetProtocolFromTable** function is used to obtain a handle to the next protocol.</span></span> <span data-ttu-id="5496c-120">Функция **жетпротоколфромтабле** вызывается для получения маркера из следующего протокола, если протокол определяет, какой именно протокол следует.</span><span class="sxs-lookup"><span data-stu-id="5496c-120">The **GetProtocolFromTable** function is called to retrieve a handle from the next protocol if the protocol identifies which protocol follows.</span></span>

<span data-ttu-id="5496c-121">**Данные экземпляров**</span><span class="sxs-lookup"><span data-stu-id="5496c-121">**Instance data**</span></span>

<span data-ttu-id="5496c-122">Данные экземпляра могут быть любыми данными, размер которых меньше или равен DWORD или \_ указателем на данные, например необработанные данные кадра, которые не должны выделяться или освобождаться анализатором.</span><span class="sxs-lookup"><span data-stu-id="5496c-122">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>

## <a name="requirements"></a><span data-ttu-id="5496c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5496c-123">Requirements</span></span>



| <span data-ttu-id="5496c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5496c-124">Requirement</span></span> | <span data-ttu-id="5496c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5496c-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5496c-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5496c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5496c-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5496c-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5496c-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5496c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5496c-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5496c-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5496c-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5496c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5496c-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5496c-131"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5496c-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5496c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5496c-133"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5496c-133"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5496c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5496c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5496c-135"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5496c-135"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5496c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5496c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5496c-137">рекогнизефраме</span><span class="sxs-lookup"><span data-stu-id="5496c-137">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




