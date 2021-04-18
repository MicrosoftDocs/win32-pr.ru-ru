---
description: Метод Свбемрефрешаблеитем. Remove удаляет объект Свбемрефрешаблеитем из родительского объекта Свбемрефрешер. Объект Свбемрефрешаблеитем из родительского объекта Свбемрефрешер.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: Метод Свбемрефрешаблеитем. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693840"
---
# <a name="swbemrefreshableitemremove-method"></a><span data-ttu-id="e72ff-103">Свбемрефрешаблеитем. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="e72ff-103">SWbemRefreshableItem.Remove method</span></span>

<span data-ttu-id="e72ff-104">Метод **свбемрефрешаблеитем. Remove** удаляет объект [**свбемрефрешаблеитем**](swbemrefreshableitem.md) из родительского объекта [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="e72ff-104">The **SWbemRefreshableItem.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="e72ff-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e72ff-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e72ff-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e72ff-106">Syntax</span></span>


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e72ff-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e72ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e72ff-108">*лфлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e72ff-108">*lFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e72ff-109">Этот параметр должен иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="e72ff-109">This parameter must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e72ff-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e72ff-110">Return value</span></span>

<span data-ttu-id="e72ff-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e72ff-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e72ff-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e72ff-112">Remarks</span></span>

<span data-ttu-id="e72ff-113">**Коды ошибок** Если у Обновитель нет элемента с указанным индексом, **вбемеррнотфаунд** создается.</span><span class="sxs-lookup"><span data-stu-id="e72ff-113">**Error Codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="e72ff-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e72ff-114">Requirements</span></span>



| <span data-ttu-id="e72ff-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e72ff-115">Requirement</span></span> | <span data-ttu-id="e72ff-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e72ff-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e72ff-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e72ff-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e72ff-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e72ff-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e72ff-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e72ff-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e72ff-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e72ff-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e72ff-121">Header</span><span class="sxs-lookup"><span data-stu-id="e72ff-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e72ff-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e72ff-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e72ff-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e72ff-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="e72ff-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e72ff-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e72ff-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e72ff-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e72ff-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e72ff-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e72ff-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="e72ff-127">CLSID</span></span><br/>                    | <span data-ttu-id="e72ff-128">\_СВБЕМРЕФРЕШАБЛЕИТЕМ CLSID</span><span class="sxs-lookup"><span data-stu-id="e72ff-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="e72ff-129">IID</span><span class="sxs-lookup"><span data-stu-id="e72ff-129">IID</span></span><br/>                      | <span data-ttu-id="e72ff-130">IID \_ исвбемрефрешаблеитем</span><span class="sxs-lookup"><span data-stu-id="e72ff-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="e72ff-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e72ff-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e72ff-132">**свбемрефрешаблеитем**</span><span class="sxs-lookup"><span data-stu-id="e72ff-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="e72ff-133">**свбемрефрешер**</span><span class="sxs-lookup"><span data-stu-id="e72ff-133">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




