---
description: Метод Клоседатабасе объекта Merge закрывает текущую открытую установщик Windows базу данных.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Метод Merge. Клоседатабасе (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674781"
---
# <a name="mergeclosedatabase-method"></a><span data-ttu-id="04c31-103">Метод Merge. Клоседатабасе</span><span class="sxs-lookup"><span data-stu-id="04c31-103">Merge.CloseDatabase method</span></span>

<span data-ttu-id="04c31-104">Метод **клоседатабасе** объекта [**Merge**](merge-object.md) закрывает текущую открытую установщик Windows базу данных.</span><span class="sxs-lookup"><span data-stu-id="04c31-104">The **CloseDatabase** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer database.</span></span>

## <a name="syntax"></a><span data-ttu-id="04c31-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04c31-105">Syntax</span></span>


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a><span data-ttu-id="04c31-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04c31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04c31-107">*бкоммит*</span><span class="sxs-lookup"><span data-stu-id="04c31-107">*bCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="04c31-108">**Значение true** , если необходимо сохранить изменения; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="04c31-108">**TRUE** if changes should be saved, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04c31-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04c31-109">Return value</span></span>

<span data-ttu-id="04c31-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="04c31-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04c31-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04c31-111">Remarks</span></span>

<span data-ttu-id="04c31-112">При закрытии базы данных удаляются все сведения о зависимостях, но не затрагиваются все ошибки, которые не были получены.</span><span class="sxs-lookup"><span data-stu-id="04c31-112">Closing a database clears all dependency information but does not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="04c31-113">C++</span><span class="sxs-lookup"><span data-stu-id="04c31-113">C++</span></span>

<span data-ttu-id="04c31-114">См. раздел Функция [**клоседатабасе**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) .</span><span class="sxs-lookup"><span data-stu-id="04c31-114">See [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="04c31-115">Требования</span><span class="sxs-lookup"><span data-stu-id="04c31-115">Requirements</span></span>



| <span data-ttu-id="04c31-116">Требование</span><span class="sxs-lookup"><span data-stu-id="04c31-116">Requirement</span></span> | <span data-ttu-id="04c31-117">Значение</span><span class="sxs-lookup"><span data-stu-id="04c31-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04c31-118">Версия</span><span class="sxs-lookup"><span data-stu-id="04c31-118">Version</span></span><br/> | <span data-ttu-id="04c31-119">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="04c31-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="04c31-120">Header</span><span class="sxs-lookup"><span data-stu-id="04c31-120">Header</span></span><br/>  | <dl> <span data-ttu-id="04c31-121"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="04c31-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="04c31-122">DLL</span><span class="sxs-lookup"><span data-stu-id="04c31-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="04c31-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04c31-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
