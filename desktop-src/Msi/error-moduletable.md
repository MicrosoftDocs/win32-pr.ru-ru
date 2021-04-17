---
description: Свойство Модулетабле только для чтения возвращает имя таблицы в модуле, вызвавшем ошибку.
ms.assetid: 390f5889-d638-4c1c-b95c-76d38c934e7c
title: Ошибка. свойство Модулетабле (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleTable
- IMsmError.get_ModuleTable
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 063898419596fc852d073bf83ce7504a7691a10e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685309"
---
# <a name="errormoduletable-property"></a><span data-ttu-id="3b8d5-103">Ошибка. Модулетабле, свойство</span><span class="sxs-lookup"><span data-stu-id="3b8d5-103">Error.ModuleTable property</span></span>

<span data-ttu-id="3b8d5-104">Свойство **модулетабле** только для чтения возвращает имя таблицы в модуле, вызвавшем ошибку.</span><span class="sxs-lookup"><span data-stu-id="3b8d5-104">The read-only **ModuleTable** Property returns the name of the table in the module that caused the error.</span></span>

<span data-ttu-id="3b8d5-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3b8d5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8d5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b8d5-106">Syntax</span></span>


```JScript
propVal = Error.ModuleTable
```



## <a name="property-value"></a><span data-ttu-id="3b8d5-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3b8d5-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3b8d5-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b8d5-108">Remarks</span></span>

<span data-ttu-id="3b8d5-109">Если значения не применяются к типу ошибки, коллекция пуста.</span><span class="sxs-lookup"><span data-stu-id="3b8d5-109">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="3b8d5-110">Тип ошибки можно определить, вызвав свойство [**Type**](error-type.md) объекта [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8d5-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="3b8d5-111">C++</span><span class="sxs-lookup"><span data-stu-id="3b8d5-111">C++</span></span>

<span data-ttu-id="3b8d5-112">См. раздел [**Получение функции \_ модулетабле**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) .</span><span class="sxs-lookup"><span data-stu-id="3b8d5-112">See [**get\_ModuleTable**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_moduletable) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b8d5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3b8d5-113">Requirements</span></span>



| <span data-ttu-id="3b8d5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3b8d5-114">Requirement</span></span> | <span data-ttu-id="3b8d5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3b8d5-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8d5-116">Версия</span><span class="sxs-lookup"><span data-stu-id="3b8d5-116">Version</span></span><br/> | <span data-ttu-id="3b8d5-117">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3b8d5-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3b8d5-118">Header</span><span class="sxs-lookup"><span data-stu-id="3b8d5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3b8d5-119"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b8d5-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b8d5-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3b8d5-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b8d5-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b8d5-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

