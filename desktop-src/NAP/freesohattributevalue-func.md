---
title: Функция Фрисохаттрибутевалуе (Напутил. h)
description: Освобождает структуру данных Сохаттрибутевалуе.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- Фрисохаттрибутевалуе функция NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd56049eb727554227bd5eb509969f6795670a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071952"
---
# <a name="freesohattributevalue-function"></a><span data-ttu-id="0df73-104">Функция Фрисохаттрибутевалуе</span><span class="sxs-lookup"><span data-stu-id="0df73-104">FreeSoHAttributeValue function</span></span>

> [!Note]  
> <span data-ttu-id="0df73-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="0df73-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0df73-106">Функция **фрисохаттрибутевалуе** освобождает структуру данных [**сохаттрибутевалуе**](sohattributevalue-union.md) .</span><span class="sxs-lookup"><span data-stu-id="0df73-106">The **FreeSoHAttributeValue** function frees an [**SoHAttributeValue**](sohattributevalue-union.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0df73-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0df73-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="0df73-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0df73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0df73-109">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0df73-109">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df73-110">Значение [**сохаттрибутетипе**](sohattributetype-enum.md) , указывающее тип значения атрибута SoH для освобождения.</span><span class="sxs-lookup"><span data-stu-id="0df73-110">A [**SoHAttributeType**](sohattributetype-enum.md) value that specifies the type of SoH attribute value to free.</span></span>

</dd> <dt>

<span data-ttu-id="0df73-111">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0df73-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0df73-112">Указатель на [**сохаттрибутевалуе**](sohattributevalue-union.md) для освобождения.</span><span class="sxs-lookup"><span data-stu-id="0df73-112">A pointer to the [**SoHAttributeValue**](sohattributevalue-union.md) to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0df73-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0df73-113">Remarks</span></span>

<span data-ttu-id="0df73-114">Все COM-интерфейсы, поддерживаемые системой защиты доступа к сети, используют стандартные правила управления памятью COM и распределителя памяти COM (**CoTaskMemAlloc** и **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="0df73-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="0df73-115">**Входные** параметры выделяются и освобождаются вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="0df73-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="0df73-116">**Выходные** параметры выделяются вызываемым методом и освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="0df73-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="0df73-117">**Входные и выходные** параметры выделяются вызывающим объектом, освобождаются и перераспределяются вызываемым объектом, и в итоге освобождаются вызывающей стороной с помощью **котаскмем**.</span><span class="sxs-lookup"><span data-stu-id="0df73-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="0df73-118">Все функции NAP для освобождения памяти также освобождают все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="0df73-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="0df73-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0df73-119">Requirements</span></span>



| <span data-ttu-id="0df73-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0df73-120">Requirement</span></span> | <span data-ttu-id="0df73-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0df73-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0df73-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0df73-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0df73-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0df73-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0df73-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0df73-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0df73-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0df73-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0df73-126">Header</span><span class="sxs-lookup"><span data-stu-id="0df73-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0df73-127"><dt>Напутил. h</dt></span><span class="sxs-lookup"><span data-stu-id="0df73-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="0df73-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0df73-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0df73-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0df73-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





