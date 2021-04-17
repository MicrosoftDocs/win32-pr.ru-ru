---
description: Отображает окно сообщения с указанной строкой, именем исходного файла и номером строки. Пользователь может проигнорировать сообщение, ввести отладчик или выйти из приложения. Игнорируется в розничных сборках.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Макрос Дбгбреак (Вксдебуг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657965"
---
# <a name="dbgbreak-macro"></a><span data-ttu-id="d7ac9-105">Макрос Дбгбреак</span><span class="sxs-lookup"><span data-stu-id="d7ac9-105">DbgBreak macro</span></span>

<span data-ttu-id="d7ac9-106">Отображает окно сообщения с указанной строкой, именем исходного файла и номером строки.</span><span class="sxs-lookup"><span data-stu-id="d7ac9-106">Displays a message box with the specified string, the name of the source file, and the line number.</span></span> <span data-ttu-id="d7ac9-107">Пользователь может проигнорировать сообщение, ввести отладчик или выйти из приложения.</span><span class="sxs-lookup"><span data-stu-id="d7ac9-107">The user can ignore the message, enter the debugger, or quit the application.</span></span> <span data-ttu-id="d7ac9-108">Игнорируется в розничных сборках.</span><span class="sxs-lookup"><span data-stu-id="d7ac9-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ac9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7ac9-109">Syntax</span></span>


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="d7ac9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7ac9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ac9-111">*стрлитерал*</span><span class="sxs-lookup"><span data-stu-id="d7ac9-111">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ac9-112">Текстовая строка.</span><span class="sxs-lookup"><span data-stu-id="d7ac9-112">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ac9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7ac9-113">Return value</span></span>

<span data-ttu-id="d7ac9-114">Этот макрос не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d7ac9-114">This macro does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d7ac9-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="d7ac9-115">Examples</span></span>


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a><span data-ttu-id="d7ac9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d7ac9-116">Requirements</span></span>



| <span data-ttu-id="d7ac9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d7ac9-117">Requirement</span></span> | <span data-ttu-id="d7ac9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d7ac9-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ac9-119">Header</span><span class="sxs-lookup"><span data-stu-id="d7ac9-119">Header</span></span><br/> | <dl> <span data-ttu-id="d7ac9-120"><dt>Вксдебуг. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7ac9-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ac9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7ac9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ac9-122">Макросы Assert и точка останова</span><span class="sxs-lookup"><span data-stu-id="d7ac9-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




