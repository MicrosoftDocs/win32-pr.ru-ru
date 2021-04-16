---
description: Функция Парсертемпорарилоккфраме блокирует кадр при входе в средство синтаксического анализа и разблокирует кадр, когда функция выходит из средства синтаксического анализа.
ms.assetid: c1c52f62-1974-47cc-8c37-61918fbce54a
title: Функция Парсертемпорарилоккфраме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserTemporaryLockFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 48fa646e709982d88093e0cbeb5e60375643351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664313"
---
# <a name="parsertemporarylockframe-function"></a><span data-ttu-id="0f5a7-103">Функция Парсертемпорарилоккфраме</span><span class="sxs-lookup"><span data-stu-id="0f5a7-103">ParserTemporaryLockFrame function</span></span>

<span data-ttu-id="0f5a7-104">Функция **парсертемпорарилоккфраме** блокирует кадр при входе в средство синтаксического анализа и разблокирует кадр, когда функция выходит из средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="0f5a7-104">The **ParserTemporaryLockFrame** function locks a frame when it enters a parser and unlocks the frame when the function exits the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5a7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f5a7-105">Syntax</span></span>


```C++
LPBYTE WINAPI ParserTemporaryLockFrame(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="0f5a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f5a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f5a7-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f5a7-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f5a7-108">Указатель на кадр, на который указывает средство синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="0f5a7-108">Handle to the frame that the parser points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f5a7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f5a7-109">Return value</span></span>

<span data-ttu-id="0f5a7-110">Если функция выполнена успешно, возвращаемое значение является указателем на первый байт данных в кадре.</span><span class="sxs-lookup"><span data-stu-id="0f5a7-110">If the function is successful, the return value is a pointer to the first byte of data in the frame.</span></span>

<span data-ttu-id="0f5a7-111">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="0f5a7-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f5a7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f5a7-112">Remarks</span></span>

<span data-ttu-id="0f5a7-113">Средства синтаксического анализа не должны вызывать функцию **локкфраме** .</span><span class="sxs-lookup"><span data-stu-id="0f5a7-113">Parsers should not call the **LockFrame** function.</span></span> <span data-ttu-id="0f5a7-114">Если средство синтаксического анализа принимает блокировку, а затем создает ошибку или возвращает результат без разблокировки кадра, средство синтаксического анализа оставляет систему в состоянии, в котором она не может изменять протоколы или вырезание или копирование кадров.</span><span class="sxs-lookup"><span data-stu-id="0f5a7-114">If a parser takes a lock and then generates a fault or returns without unlocking the frame, the parser leaves the system in a state where it cannot change protocols or cut or copy frames.</span></span> <span data-ttu-id="0f5a7-115">Средства синтаксического анализа должны использовать функцию **парсертемпорарилоккфраме** , которая предоставляет блокировку только во время контекста записи функции в средство синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="0f5a7-115">Parsers should use the **ParserTemporaryLockFrame** function, which grants a lock only during the context of the function entry into the parser.</span></span> <span data-ttu-id="0f5a7-116">При выходе из средства синтаксического анализа блокировка для этого кадра освобождается.</span><span class="sxs-lookup"><span data-stu-id="0f5a7-116">On exit from the parser, the lock for that frame is released.</span></span> <span data-ttu-id="0f5a7-117">В результате указатель будет действителен только после того, как средство синтаксического анализа вернется из вызова функции **аттачпропертиес** или **рекогнизефраме** .</span><span class="sxs-lookup"><span data-stu-id="0f5a7-117">As a result, the pointer will be valid only after the parser returns from the call to the **AttachProperties** or **RecognizeFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5a7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0f5a7-118">Requirements</span></span>



| <span data-ttu-id="0f5a7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0f5a7-119">Requirement</span></span> | <span data-ttu-id="0f5a7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0f5a7-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5a7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f5a7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f5a7-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f5a7-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0f5a7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f5a7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f5a7-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f5a7-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0f5a7-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0f5a7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f5a7-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f5a7-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0f5a7-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0f5a7-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f5a7-128"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f5a7-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0f5a7-129">DLL</span><span class="sxs-lookup"><span data-stu-id="0f5a7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f5a7-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f5a7-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




