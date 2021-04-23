---
description: Вызывает вспомогательную функциональность для интерфейса IDispatch.
ms.assetid: ccef47af-d9dd-48c3-93d3-ee997dacf7a8
title: Функция Инвокеидиспатч
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InvokeIDispatch
api_type:
- LibDef
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4989e3ec23a1ffa97ba317831143ecf0920ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702479"
---
# <a name="invokeidispatch-function"></a><span data-ttu-id="c9052-103">Функция Инвокеидиспатч</span><span class="sxs-lookup"><span data-stu-id="c9052-103">InvokeIDispatch function</span></span>

<span data-ttu-id="c9052-104">Вызывает вспомогательную функциональность для интерфейса IDispatch.</span><span class="sxs-lookup"><span data-stu-id="c9052-104">Invokes helper functionality for the IDispatch interface.</span></span>

<span data-ttu-id="c9052-105">Эта функция не предназначена для использования в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="c9052-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9052-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9052-106">Syntax</span></span>


```C++
HRESULT WINAPI InvokeIDispatch(
        IDispatch  *pDispatch,
        DISPID     dispid,
        DISPPARAMS *pDisp,
  _Out_ VARIANT    *pVarResult
);
```



## <a name="parameters"></a><span data-ttu-id="c9052-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9052-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9052-108">*пдиспатч*</span><span class="sxs-lookup"><span data-stu-id="c9052-108">*pDispatch*</span></span> 
</dt> <dd>

<span data-ttu-id="c9052-109">Экземпляр интерфейса IDispatch.</span><span class="sxs-lookup"><span data-stu-id="c9052-109">The instance of the IDispatch interface.</span></span>

</dd> <dt>

<span data-ttu-id="c9052-110">*DISPID*</span><span class="sxs-lookup"><span data-stu-id="c9052-110">*dispid*</span></span> 
</dt> <dd>

<span data-ttu-id="c9052-111">Метод, свойство или аргумент для передачи.</span><span class="sxs-lookup"><span data-stu-id="c9052-111">The method, property, or argument to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="c9052-112">*пдисп*</span><span class="sxs-lookup"><span data-stu-id="c9052-112">*pDisp*</span></span> 
</dt> <dd>

<span data-ttu-id="c9052-113">Параметры для передачи.</span><span class="sxs-lookup"><span data-stu-id="c9052-113">The parameters to pass in.</span></span>

</dd> <dt>

<span data-ttu-id="c9052-114">*пварресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c9052-114">*pVarResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9052-115">Структура, принимающая извлеченные значения.</span><span class="sxs-lookup"><span data-stu-id="c9052-115">A structure that receives the retrieved values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9052-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9052-116">Return value</span></span>

<span data-ttu-id="c9052-117">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="c9052-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c9052-118">В случае неудачи возможные коды возврата включают, но не ограничиваются значениями, приведенными в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c9052-118">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="c9052-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c9052-119">Return code</span></span>                                                                                  | <span data-ttu-id="c9052-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c9052-120">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="c9052-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c9052-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c9052-122">Недопустимое значение для *пдиспатч* .</span><span class="sxs-lookup"><span data-stu-id="c9052-122">The value for *pDispatch* is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9052-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c9052-123">Requirements</span></span>



| <span data-ttu-id="c9052-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c9052-124">Requirement</span></span> | <span data-ttu-id="c9052-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c9052-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9052-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9052-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c9052-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c9052-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c9052-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9052-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c9052-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c9052-129">None supported</span></span><br/>                                                             |
| <span data-ttu-id="c9052-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9052-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9052-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9052-131"><dt>InkObj.dll</dt></span></span> </dl> |



 

 




