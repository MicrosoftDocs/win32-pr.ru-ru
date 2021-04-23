---
description: Функция Дестройблоб освобождает всю память, связанную с большим двоичным объектом, а затем уничтожает большой двоичный объект.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: Функция Дестройблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664416"
---
# <a name="destroyblob-function"></a><span data-ttu-id="e4bf0-103">Функция Дестройблоб</span><span class="sxs-lookup"><span data-stu-id="e4bf0-103">DestroyBlob function</span></span>

<span data-ttu-id="e4bf0-104">Функция **дестройблоб** освобождает всю память, связанную с большим двоичным объектом, а затем уничтожает большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-104">The **DestroyBlob** function frees all memory associated with the BLOB and then destroys the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4bf0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4bf0-105">Syntax</span></span>


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="e4bf0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4bf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4bf0-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4bf0-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4bf0-108">Обработчик для объекта, который уничтожается.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-108">Handle to the to the BLOB that is destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4bf0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4bf0-109">Return value</span></span>

<span data-ttu-id="e4bf0-110">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e4bf0-111">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="e4bf0-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4bf0-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e4bf0-112">Requirements</span></span>



| <span data-ttu-id="e4bf0-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e4bf0-113">Requirement</span></span> | <span data-ttu-id="e4bf0-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e4bf0-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4bf0-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4bf0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e4bf0-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e4bf0-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e4bf0-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4bf0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e4bf0-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e4bf0-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4bf0-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e4bf0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4bf0-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4bf0-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e4bf0-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e4bf0-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4bf0-122"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4bf0-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e4bf0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e4bf0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4bf0-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4bf0-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4bf0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4bf0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4bf0-126">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="e4bf0-126">CreateBlob</span></span>](createblob.md)
</dt> </dl>

 

 




