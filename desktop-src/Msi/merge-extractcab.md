---
description: Метод Екстракткаб объекта Merge извлекает из модуля внедренный CAB-файл и сохраняет его как указанный файл. Установщик создаст этот файл, если он еще не существует, и перезаписал его, если он существует.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Метод Merge. Екстракткаб (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665192"
---
# <a name="mergeextractcab-method"></a><span data-ttu-id="6d557-104">Метод Merge. Екстракткаб</span><span class="sxs-lookup"><span data-stu-id="6d557-104">Merge.ExtractCAB method</span></span>

<span data-ttu-id="6d557-105">Метод **екстракткаб** объекта [**Merge**](merge-object.md) извлекает из модуля внедренный CAB-файл и сохраняет его как указанный файл.</span><span class="sxs-lookup"><span data-stu-id="6d557-105">The **ExtractCAB** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and saves it as the specified file.</span></span> <span data-ttu-id="6d557-106">Установщик создаст этот файл, если он еще не существует, и перезаписал его, если он существует.</span><span class="sxs-lookup"><span data-stu-id="6d557-106">The installer creates this file if it does not already exist and overwritten if it does exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d557-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d557-107">Syntax</span></span>


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a><span data-ttu-id="6d557-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d557-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d557-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="6d557-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="6d557-110">Полный файл назначения.</span><span class="sxs-lookup"><span data-stu-id="6d557-110">The fully qualified destination file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d557-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d557-111">Return value</span></span>

<span data-ttu-id="6d557-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6d557-112">This method does not return a value.</span></span>

## <a name="c"></a><span data-ttu-id="6d557-113">C++</span><span class="sxs-lookup"><span data-stu-id="6d557-113">C++</span></span>

<span data-ttu-id="6d557-114">См. раздел Функция [**екстракткаб**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) .</span><span class="sxs-lookup"><span data-stu-id="6d557-114">See [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d557-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6d557-115">Requirements</span></span>



| <span data-ttu-id="6d557-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6d557-116">Requirement</span></span> | <span data-ttu-id="6d557-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6d557-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d557-118">Версия</span><span class="sxs-lookup"><span data-stu-id="6d557-118">Version</span></span><br/> | <span data-ttu-id="6d557-119">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6d557-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="6d557-120">Header</span><span class="sxs-lookup"><span data-stu-id="6d557-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6d557-121"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d557-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d557-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6d557-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="6d557-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d557-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
