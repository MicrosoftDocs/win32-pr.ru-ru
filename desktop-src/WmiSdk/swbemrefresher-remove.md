---
description: Метод Свбемрефрешер. Refresh удаляет из Обновитель объект Свбемрефрешаблеитем с указанным индексом.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Метод Свбемрефрешер. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999940"
---
# <a name="swbemrefresherremove-method"></a><span data-ttu-id="4b72a-103">Свбемрефрешер. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="4b72a-103">SWbemRefresher.Remove method</span></span>

<span data-ttu-id="4b72a-104">Метод **свбемрефрешер. Refresh** удаляет из Обновитель объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) с указанным индексом.</span><span class="sxs-lookup"><span data-stu-id="4b72a-104">The **SWbemRefresher.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object with the specified index from the refresher.</span></span> <span data-ttu-id="4b72a-105">Объект **свбемрефрешаблеитем** может представлять либо один объект, либо набор объектов.</span><span class="sxs-lookup"><span data-stu-id="4b72a-105">The **SWbemRefreshableItem** object can represent either a single object or an object set.</span></span>

<span data-ttu-id="4b72a-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="4b72a-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b72a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b72a-107">Syntax</span></span>


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4b72a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b72a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b72a-109">*линдекс*</span><span class="sxs-lookup"><span data-stu-id="4b72a-109">*LIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="4b72a-110">Индекс элемента в объекте [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="4b72a-110">Index of the item in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="4b72a-111">*ифлагс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="4b72a-111">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b72a-112">Флаги должны быть установлены в T0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="4b72a-112">Flags must be set t0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="4b72a-113">*обжвбемнамедвалуесет* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="4b72a-113">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4b72a-114">NULL.</span><span class="sxs-lookup"><span data-stu-id="4b72a-114">Null.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b72a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b72a-115">Return value</span></span>

<span data-ttu-id="4b72a-116">Этот метод не имеет возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="4b72a-116">This method has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b72a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b72a-117">Remarks</span></span>

<span data-ttu-id="4b72a-118">**Коды ошибок** Если у Обновитель нет элемента с указанным индексом, **вбемеррнотфаунд** создается.</span><span class="sxs-lookup"><span data-stu-id="4b72a-118">**Error codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b72a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4b72a-119">Requirements</span></span>



| <span data-ttu-id="4b72a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4b72a-120">Requirement</span></span> | <span data-ttu-id="4b72a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4b72a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b72a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b72a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4b72a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b72a-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4b72a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b72a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4b72a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b72a-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4b72a-126">Header</span><span class="sxs-lookup"><span data-stu-id="4b72a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b72a-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b72a-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b72a-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4b72a-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b72a-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4b72a-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4b72a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4b72a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b72a-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b72a-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4b72a-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="4b72a-132">CLSID</span></span><br/>                    | <span data-ttu-id="4b72a-133">\_СВБЕМРЕФРЕШЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="4b72a-133">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="4b72a-134">IID</span><span class="sxs-lookup"><span data-stu-id="4b72a-134">IID</span></span><br/>                      | <span data-ttu-id="4b72a-135">IID \_ исвбемрефрешер</span><span class="sxs-lookup"><span data-stu-id="4b72a-135">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="4b72a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b72a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b72a-137">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="4b72a-137">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




