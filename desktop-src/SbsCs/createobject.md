---
description: Метод CreateObject объекта Microsoft. Windows. Акткткс создает объект в контексте текущего манифеста.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: Метод Акткткс. CreateObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265024"
---
# <a name="actctxcreateobject-method"></a><span data-ttu-id="d3b0e-103">Метод Акткткс. CreateObject</span><span class="sxs-lookup"><span data-stu-id="d3b0e-103">ActCtx.CreateObject method</span></span>

<span data-ttu-id="d3b0e-104">Метод **CreateObject** объекта [**Microsoft. Windows. акткткс**](microsoft-windows-actctx-object.md) создает объект в контексте текущего манифеста.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-104">The **CreateObject** method of the [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object creates an object in the context of the current manifest.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3b0e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3b0e-105">Syntax</span></span>


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a><span data-ttu-id="d3b0e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3b0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b0e-107">*ИД*</span><span class="sxs-lookup"><span data-stu-id="d3b0e-107">*objectId*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b0e-108">Строка, указывающая тип создаваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-108">A string that specifies the type of object to create.</span></span> <span data-ttu-id="d3b0e-109">Например, COM ProgID.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-109">For example, a COM ProgID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b0e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3b0e-110">Return value</span></span>

<span data-ttu-id="d3b0e-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d3b0e-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b0e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d3b0e-112">Requirements</span></span>



| <span data-ttu-id="d3b0e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d3b0e-113">Requirement</span></span> | <span data-ttu-id="d3b0e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d3b0e-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b0e-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d3b0e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b0e-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3b0e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d3b0e-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d3b0e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b0e-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3b0e-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d3b0e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d3b0e-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3b0e-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3b0e-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="d3b0e-121">IID</span><span class="sxs-lookup"><span data-stu-id="d3b0e-121">IID</span></span><br/>                      | <span data-ttu-id="d3b0e-122">IID \_ иакткткс определен как 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="d3b0e-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="d3b0e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d3b0e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b0e-124">**Метод GetObject**</span><span class="sxs-lookup"><span data-stu-id="d3b0e-124">**GetObject Method**</span></span>](getobject.md)
</dt> </dl>

 

 




