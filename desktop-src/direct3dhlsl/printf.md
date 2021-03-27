---
title: printf - функция
description: Отправляет настраиваемое сообщение шейдера в информационную очередь.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- Функция printf HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103987014"
---
# <a name="printf-function"></a><span data-ttu-id="bab40-104">printf - функция</span><span class="sxs-lookup"><span data-stu-id="bab40-104">printf function</span></span>

<span data-ttu-id="bab40-105">Отправляет настраиваемое сообщение шейдера в информационную очередь.</span><span class="sxs-lookup"><span data-stu-id="bab40-105">Submits a custom shader message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab40-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bab40-106">Syntax</span></span>

``` syntax
void printf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="bab40-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bab40-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab40-108">*format*</span><span class="sxs-lookup"><span data-stu-id="bab40-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="bab40-109">Строка формата.</span><span class="sxs-lookup"><span data-stu-id="bab40-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="bab40-110">*аргумент...*</span><span class="sxs-lookup"><span data-stu-id="bab40-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="bab40-111">Необязательные аргументы.</span><span class="sxs-lookup"><span data-stu-id="bab40-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab40-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bab40-112">Return value</span></span>

<span data-ttu-id="bab40-113">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bab40-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab40-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bab40-114">Remarks</span></span>

<span data-ttu-id="bab40-115">Эта операция не выполняет никаких действий на устройствах, которые ее не поддерживают.</span><span class="sxs-lookup"><span data-stu-id="bab40-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="bab40-116">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bab40-116">Minimum Shader Model</span></span>

<span data-ttu-id="bab40-117">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bab40-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bab40-118">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bab40-118">Shader Model</span></span>                                                        | <span data-ttu-id="bab40-119">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="bab40-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="bab40-120">Shader Model 4 (DirectX HLSL) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bab40-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bab40-121">да</span><span class="sxs-lookup"><span data-stu-id="bab40-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="bab40-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bab40-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab40-123">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="bab40-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




