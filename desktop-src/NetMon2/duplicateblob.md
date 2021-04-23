---
description: Функция Дупликатеблоб копирует конкретный большой двоичный объект.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: Функция Дупликатеблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650997"
---
# <a name="duplicateblob-function"></a><span data-ttu-id="94795-103">Функция Дупликатеблоб</span><span class="sxs-lookup"><span data-stu-id="94795-103">DuplicateBlob function</span></span>

<span data-ttu-id="94795-104">Функция **дупликатеблоб** копирует конкретный большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="94795-104">The **DuplicateBlob** function copies a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="94795-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94795-105">Syntax</span></span>


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="94795-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="94795-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94795-107">*хсркблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94795-107">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94795-108">Обработчик для копируемого большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="94795-108">Handle to the BLOB that is copied.</span></span>

</dd> <dt>

<span data-ttu-id="94795-109">*хблобсатвиллбекреатед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="94795-109">*hBlobThatWillBeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94795-110">Обработчик для повторяющегося большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="94795-110">Handle to the duplicate BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94795-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94795-111">Return value</span></span>

<span data-ttu-id="94795-112">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="94795-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="94795-113">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="94795-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="94795-114">Требования</span><span class="sxs-lookup"><span data-stu-id="94795-114">Requirements</span></span>



| <span data-ttu-id="94795-115">Требование</span><span class="sxs-lookup"><span data-stu-id="94795-115">Requirement</span></span> | <span data-ttu-id="94795-116">Значение</span><span class="sxs-lookup"><span data-stu-id="94795-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94795-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94795-117">Minimum supported client</span></span><br/> | <span data-ttu-id="94795-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="94795-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94795-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94795-119">Minimum supported server</span></span><br/> | <span data-ttu-id="94795-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="94795-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94795-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="94795-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="94795-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="94795-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="94795-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="94795-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="94795-124"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94795-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="94795-125">DLL</span><span class="sxs-lookup"><span data-stu-id="94795-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94795-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94795-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94795-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94795-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94795-128">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="94795-128">CreateBlob</span></span>](createblob.md)
</dt> <dt>

[<span data-ttu-id="94795-129">дестройблоб</span><span class="sxs-lookup"><span data-stu-id="94795-129">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 




