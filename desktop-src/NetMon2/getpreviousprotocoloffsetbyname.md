---
description: Функция Жетпревиауспротоколоффсетбинаме возвращает предыдущий экземпляр данного протокола.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Функция Жетпревиауспротоколоффсетбинаме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673183"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a><span data-ttu-id="5e59b-103">Функция Жетпревиауспротоколоффсетбинаме</span><span class="sxs-lookup"><span data-stu-id="5e59b-103">GetPreviousProtocolOffsetByName function</span></span>

<span data-ttu-id="5e59b-104">Функция **жетпревиауспротоколоффсетбинаме** возвращает предыдущий экземпляр данного протокола.</span><span class="sxs-lookup"><span data-stu-id="5e59b-104">The **GetPreviousProtocolOffsetByName** function returns the previous instance of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e59b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e59b-105">Syntax</span></span>


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a><span data-ttu-id="5e59b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e59b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e59b-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e59b-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e59b-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="5e59b-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="5e59b-109">*двстартоффсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e59b-109">*dwStartOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e59b-110">Смещение в кадре.</span><span class="sxs-lookup"><span data-stu-id="5e59b-110">Offset in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="5e59b-111">*сзпротоколнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e59b-111">*szProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e59b-112">Имя протокола, который нужно найти.</span><span class="sxs-lookup"><span data-stu-id="5e59b-112">Name of the protocol you want to search for.</span></span>

</dd> <dt>

<span data-ttu-id="5e59b-113">*пдвпревиаусоффсет* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5e59b-113">*pdwPreviousOffset* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e59b-114">Указатель на **DWORD** , содержащий смещение к предыдущему протоколу (если функция выполнена).</span><span class="sxs-lookup"><span data-stu-id="5e59b-114">Pointer to a **DWORD** that contains the offset to the previous protocol (if the function succeeds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e59b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e59b-115">Return value</span></span>

<span data-ttu-id="5e59b-116">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5e59b-116">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5e59b-117">Если функция завершилась неудачно, возвращаемое значение — НМЕРР \_ Protocol \_ не \_ найдено.</span><span class="sxs-lookup"><span data-stu-id="5e59b-117">If the function is unsuccessful, the return value is NMERR\_PROTOCOL\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e59b-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e59b-118">Remarks</span></span>

<span data-ttu-id="5e59b-119">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать **жетпревиауспротоколоффсетбинаме**.</span><span class="sxs-lookup"><span data-stu-id="5e59b-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPreviousProtocolOffsetByName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e59b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5e59b-120">Requirements</span></span>



| <span data-ttu-id="5e59b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5e59b-121">Requirement</span></span> | <span data-ttu-id="5e59b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5e59b-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5e59b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e59b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5e59b-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5e59b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5e59b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e59b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5e59b-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5e59b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5e59b-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5e59b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e59b-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e59b-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5e59b-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5e59b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e59b-130"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e59b-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5e59b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5e59b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e59b-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e59b-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




