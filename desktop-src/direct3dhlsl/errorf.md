---
title: Функция еррорф
description: Отправляет сообщение об ошибке в информационную очередь.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- Функция еррорф HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068862"
---
# <a name="errorf-function"></a><span data-ttu-id="b9145-104">Функция еррорф</span><span class="sxs-lookup"><span data-stu-id="b9145-104">errorf function</span></span>

<span data-ttu-id="b9145-105">Отправляет сообщение об ошибке в информационную очередь.</span><span class="sxs-lookup"><span data-stu-id="b9145-105">Submits an error message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9145-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9145-106">Syntax</span></span>

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="b9145-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9145-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9145-108">*format*</span><span class="sxs-lookup"><span data-stu-id="b9145-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="b9145-109">Строка формата.</span><span class="sxs-lookup"><span data-stu-id="b9145-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="b9145-110">*аргумент...*</span><span class="sxs-lookup"><span data-stu-id="b9145-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="b9145-111">Необязательные аргументы.</span><span class="sxs-lookup"><span data-stu-id="b9145-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9145-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9145-112">Return value</span></span>

<span data-ttu-id="b9145-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b9145-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9145-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9145-114">Remarks</span></span>

<span data-ttu-id="b9145-115">Эта операция не выполняет никаких действий на устройствах, которые ее не поддерживают.</span><span class="sxs-lookup"><span data-stu-id="b9145-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="b9145-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b9145-116">Minimum Shader Model</span></span>

<span data-ttu-id="b9145-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b9145-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b9145-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b9145-118">Shader Model</span></span>                                                        | <span data-ttu-id="b9145-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b9145-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="b9145-120">Shader Model 4 (DirectX HLSL) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b9145-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b9145-121">да</span><span class="sxs-lookup"><span data-stu-id="b9145-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b9145-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9145-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9145-123">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="b9145-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




