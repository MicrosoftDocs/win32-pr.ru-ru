---
description: Функция CreateBlob создает пустой большой двоичный объект.
ms.assetid: fa31855b-af85-4ab5-b434-e54111731d8f
title: Функция CreateBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: f2abb32afd68dd321a520c1d56c217e801fa9101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814208"
---
# <a name="createblob-function"></a><span data-ttu-id="96208-103">Функция CreateBlob</span><span class="sxs-lookup"><span data-stu-id="96208-103">CreateBlob function</span></span>

<span data-ttu-id="96208-104">Функция **CreateBlob** создает пустой большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="96208-104">The **CreateBlob** function creates an empty BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="96208-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96208-105">Syntax</span></span>


```C++
DWORD CreateBlob(
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="96208-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="96208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96208-107">*фблоб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="96208-107">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96208-108">Указатель на переменную, в которой возвращается указатель на новый большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="96208-108">Pointer to the variable where the pointer to the new BLOB is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96208-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96208-109">Return value</span></span>

<span data-ttu-id="96208-110">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="96208-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="96208-111">Если функция завершается неудачно, возвращается значение НМЕРР, описывающее ошибку.</span><span class="sxs-lookup"><span data-stu-id="96208-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="96208-112">Требования</span><span class="sxs-lookup"><span data-stu-id="96208-112">Requirements</span></span>



| <span data-ttu-id="96208-113">Требование</span><span class="sxs-lookup"><span data-stu-id="96208-113">Requirement</span></span> | <span data-ttu-id="96208-114">Значение</span><span class="sxs-lookup"><span data-stu-id="96208-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96208-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96208-115">Minimum supported client</span></span><br/> | <span data-ttu-id="96208-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96208-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="96208-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96208-117">Minimum supported server</span></span><br/> | <span data-ttu-id="96208-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96208-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96208-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="96208-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="96208-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="96208-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="96208-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="96208-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="96208-122"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96208-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="96208-123">DLL</span><span class="sxs-lookup"><span data-stu-id="96208-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96208-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96208-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96208-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96208-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96208-126">дестройблоб</span><span class="sxs-lookup"><span data-stu-id="96208-126">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 




