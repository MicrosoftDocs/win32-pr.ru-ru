---
description: Метод Клосемодуле объекта Merge закрывает открытый в данный момент модуль слияния установщик Windows.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Метод Merge. Клосемодуле (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665049"
---
# <a name="mergeclosemodule-method"></a><span data-ttu-id="30988-103">Метод Merge. Клосемодуле</span><span class="sxs-lookup"><span data-stu-id="30988-103">Merge.CloseModule method</span></span>

<span data-ttu-id="30988-104">Метод **клосемодуле** объекта [**Merge**](merge-object.md) закрывает открытый в данный момент модуль слияния установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="30988-104">The **CloseModule** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer merge module.</span></span>

## <a name="syntax"></a><span data-ttu-id="30988-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30988-105">Syntax</span></span>


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a><span data-ttu-id="30988-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30988-106">Parameters</span></span>

<span data-ttu-id="30988-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="30988-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30988-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30988-108">Return value</span></span>

<span data-ttu-id="30988-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="30988-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30988-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30988-110">Remarks</span></span>

<span data-ttu-id="30988-111">Закрытие модуля слияния не повлияет на ошибки, которые не были получены.</span><span class="sxs-lookup"><span data-stu-id="30988-111">Closing a merge module will not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="30988-112">C++</span><span class="sxs-lookup"><span data-stu-id="30988-112">C++</span></span>

<span data-ttu-id="30988-113">См. раздел Функция [**клосемодуле**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) .</span><span class="sxs-lookup"><span data-stu-id="30988-113">See [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="30988-114">Требования</span><span class="sxs-lookup"><span data-stu-id="30988-114">Requirements</span></span>



| <span data-ttu-id="30988-115">Требование</span><span class="sxs-lookup"><span data-stu-id="30988-115">Requirement</span></span> | <span data-ttu-id="30988-116">Значение</span><span class="sxs-lookup"><span data-stu-id="30988-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30988-117">Версия</span><span class="sxs-lookup"><span data-stu-id="30988-117">Version</span></span><br/> | <span data-ttu-id="30988-118">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="30988-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="30988-119">Header</span><span class="sxs-lookup"><span data-stu-id="30988-119">Header</span></span><br/>  | <dl> <span data-ttu-id="30988-120"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="30988-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="30988-121">DLL</span><span class="sxs-lookup"><span data-stu-id="30988-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="30988-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30988-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
