---
description: Функция Жетпропертитекст возвращает указатель на текст свойства.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: Функция Жетпропертитекст (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342752"
---
# <a name="getpropertytext-function"></a><span data-ttu-id="e472e-103">Функция Жетпропертитекст</span><span class="sxs-lookup"><span data-stu-id="e472e-103">GetPropertyText function</span></span>

<span data-ttu-id="e472e-104">Функция **жетпропертитекст** возвращает указатель на текст свойства.</span><span class="sxs-lookup"><span data-stu-id="e472e-104">The **GetPropertyText** function returns a pointer to the property text.</span></span>

## <a name="syntax"></a><span data-ttu-id="e472e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e472e-105">Syntax</span></span>


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="e472e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e472e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e472e-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e472e-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e472e-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="e472e-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="e472e-109">*лппи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e472e-109">*lpPI* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e472e-110">Указатель на экземпляр свойства.</span><span class="sxs-lookup"><span data-stu-id="e472e-110">Pointer to a property instance.</span></span>

</dd> <dt>

<span data-ttu-id="e472e-111">*сзбуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e472e-111">*szBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e472e-112">Указатель на текстовую строку свойства.</span><span class="sxs-lookup"><span data-stu-id="e472e-112">Pointer to the property text string.</span></span>

</dd> <dt>

<span data-ttu-id="e472e-113">*BufferSize* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e472e-113">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e472e-114">Размер буфера текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="e472e-114">Size of the text string buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e472e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e472e-115">Return value</span></span>

<span data-ttu-id="e472e-116">Если функция выполнена успешно, возвращаемое значение является указателем на текст свойства.</span><span class="sxs-lookup"><span data-stu-id="e472e-116">If the function is successful, the return value is a pointer to the property text.</span></span>

<span data-ttu-id="e472e-117">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="e472e-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e472e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e472e-118">Remarks</span></span>

<span data-ttu-id="e472e-119">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетпропертитекст** .</span><span class="sxs-lookup"><span data-stu-id="e472e-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyText** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e472e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e472e-120">Requirements</span></span>



| <span data-ttu-id="e472e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e472e-121">Requirement</span></span> | <span data-ttu-id="e472e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e472e-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e472e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e472e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e472e-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e472e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e472e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e472e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e472e-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e472e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e472e-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e472e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e472e-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e472e-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e472e-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e472e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e472e-130"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e472e-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e472e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e472e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e472e-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e472e-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




