---
description: Функция Жетфрамерекогнизедата возвращает таблицу структур РЕКОГНИЗЕДАТА. Каждая из этих структур содержит идентификатор протокола и смещение, которое указывает на начало указанного протокола в данных.
ms.assetid: 3bf809ff-8d87-4746-95ee-fb68c5e51d42
title: Функция Жетфрамерекогнизедата (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameRecognizeData
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 627ba046b3adead0291239f5d94f4e56958e6a80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990902"
---
# <a name="getframerecognizedata-function"></a><span data-ttu-id="10e5d-104">Функция Жетфрамерекогнизедата</span><span class="sxs-lookup"><span data-stu-id="10e5d-104">GetFrameRecognizeData function</span></span>

<span data-ttu-id="10e5d-105">Функция **жетфрамерекогнизедата** возвращает таблицу структур **рекогнизедата** .</span><span class="sxs-lookup"><span data-stu-id="10e5d-105">The **GetFrameRecognizeData** function returns a table of **RECOGNIZEDATA** structures.</span></span> <span data-ttu-id="10e5d-106">Каждая из этих структур содержит идентификатор протокола и смещение, которое указывает на начало указанного протокола в данных.</span><span class="sxs-lookup"><span data-stu-id="10e5d-106">Each of these structures contains a protocol identifier and an offset that points to the start of the specified protocol in the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="10e5d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10e5d-107">Syntax</span></span>


```C++
LPRECOGNIZEDATATABLE WINAPI GetFrameRecognizeData(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="10e5d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="10e5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e5d-109">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="10e5d-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10e5d-110">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="10e5d-110">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e5d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10e5d-111">Return value</span></span>

<span data-ttu-id="10e5d-112">Если функция выполнена успешно, возвращаемое значение является указателем на структуру **рекогнизедататабле** .</span><span class="sxs-lookup"><span data-stu-id="10e5d-112">If the function is successful, the return value is a pointer to a **RECOGNIZEDATATABLE** structure.</span></span>

<span data-ttu-id="10e5d-113">Если функция не выполнена успешно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="10e5d-113">If the function is not successful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="10e5d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10e5d-114">Remarks</span></span>

<span data-ttu-id="10e5d-115">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамерекогнизедата** .</span><span class="sxs-lookup"><span data-stu-id="10e5d-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameRecognizeData** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="10e5d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="10e5d-116">Requirements</span></span>



| <span data-ttu-id="10e5d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="10e5d-117">Requirement</span></span> | <span data-ttu-id="10e5d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="10e5d-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10e5d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10e5d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="10e5d-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="10e5d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="10e5d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10e5d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="10e5d-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="10e5d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="10e5d-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="10e5d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="10e5d-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="10e5d-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="10e5d-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="10e5d-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="10e5d-126"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10e5d-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="10e5d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="10e5d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10e5d-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10e5d-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




