---
description: Функция Мержеблоб копирует все записи из исходного BLOB-объекта в целевой большой двоичный объект.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Функция Мержеблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991207"
---
# <a name="mergeblob-function"></a><span data-ttu-id="cac68-103">Функция Мержеблоб</span><span class="sxs-lookup"><span data-stu-id="cac68-103">MergeBlob function</span></span>

<span data-ttu-id="cac68-104">Функция **мержеблоб** копирует все записи из исходного BLOB-объекта в целевой большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="cac68-104">The **MergeBlob** function copies all of the entries from the source BLOB into a destination BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac68-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cac68-105">Syntax</span></span>


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a><span data-ttu-id="cac68-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cac68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac68-107">*хдстблоб* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cac68-107">*hDstBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cac68-108">Обработайте с целевым BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="cac68-108">Handle to the destination BLOB.</span></span> <span data-ttu-id="cac68-109">На входе этот BLOB-объект содержит исходные сведения.</span><span class="sxs-lookup"><span data-stu-id="cac68-109">On input, this BLOB contains its original information.</span></span> <span data-ttu-id="cac68-110">В выходных данных этот большой двоичный объект содержит исходные сведения и все данные исходного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="cac68-110">On output, this BLOB contains its original information plus all the information of the source BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="cac68-111">*хсркблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cac68-111">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac68-112">Обработайте с исходным BLOB-объектом.</span><span class="sxs-lookup"><span data-stu-id="cac68-112">Handle to the source BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac68-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cac68-113">Return value</span></span>

<span data-ttu-id="cac68-114">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="cac68-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="cac68-115">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="cac68-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="cac68-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cac68-116">Remarks</span></span>

<span data-ttu-id="cac68-117">Записи, общие для исходного и целевого файлов, будут перезаписаны данными из исходного большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="cac68-117">Entries common to source and destination files will be overwritten with data from the source BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac68-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cac68-118">Requirements</span></span>



| <span data-ttu-id="cac68-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cac68-119">Requirement</span></span> | <span data-ttu-id="cac68-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cac68-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cac68-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cac68-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cac68-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cac68-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cac68-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cac68-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cac68-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cac68-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cac68-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cac68-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac68-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac68-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="cac68-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cac68-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="cac68-128"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cac68-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="cac68-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cac68-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cac68-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cac68-130"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




