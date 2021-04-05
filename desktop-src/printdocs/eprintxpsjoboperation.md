---
description: Указывает, находится ли задание печати XPS в очереди печати или на этапе отрисовки.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Перечисление Епринткспсжобоператион (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813545"
---
# <a name="eprintxpsjoboperation-enumeration"></a><span data-ttu-id="d4619-103">Перечисление Епринткспсжобоператион</span><span class="sxs-lookup"><span data-stu-id="d4619-103">EPrintXPSJobOperation enumeration</span></span>

<span data-ttu-id="d4619-104">Указывает, находится ли задание печати XPS в очереди печати или на этапе отрисовки.</span><span class="sxs-lookup"><span data-stu-id="d4619-104">Specifies whether an XPS print job is in the spooling or the rendering phase.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4619-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4619-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a><span data-ttu-id="d4619-106">Константы</span><span class="sxs-lookup"><span data-stu-id="d4619-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d4619-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**кжобпродуктион**</span><span class="sxs-lookup"><span data-stu-id="d4619-107"><span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**</span></span>
</dt> <dd>

<span data-ttu-id="d4619-108">Задание XPS находится в очереди.</span><span class="sxs-lookup"><span data-stu-id="d4619-108">The XPS job is spooling.</span></span>

</dd> <dt>

<span data-ttu-id="d4619-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**кжобконсумптион**</span><span class="sxs-lookup"><span data-stu-id="d4619-109"><span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**</span></span>
</dt> <dd>

<span data-ttu-id="d4619-110">Идет подготовка задания XPS.</span><span class="sxs-lookup"><span data-stu-id="d4619-110">The XPS job is rendering.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4619-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4619-111">Remarks</span></span>

<span data-ttu-id="d4619-112">Это перечисление в основном используется в качестве параметра функции [**репортжобпроцессингпрогресс**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="d4619-112">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4619-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d4619-113">Requirements</span></span>



| <span data-ttu-id="d4619-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d4619-114">Requirement</span></span> | <span data-ttu-id="d4619-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d4619-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4619-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4619-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d4619-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4619-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d4619-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4619-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d4619-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d4619-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d4619-120">Header</span><span class="sxs-lookup"><span data-stu-id="d4619-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4619-121"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4619-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




