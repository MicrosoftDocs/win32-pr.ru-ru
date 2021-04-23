---
title: IMsRdpClientNonScriptable5 Жетремотемониторсбаундингбокс, свойство
description: Задает ограничивающий прямоугольник удаленного монитора.
ms.assetid: 4A8794F7-1DB4-4415-8538-6B2A365B22D3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Жетремотемониторсбаундингбокс
- Службы удаленных рабочих столов свойства Жетремотемониторсбаундингбокс, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Жетремотемониторсбаундингбокс
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.GetRemoteMonitorsBoundingBox
- IMsRdpClientNonScriptable5.get_GetRemoteMonitorsBoundingBox
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f67192b78c734359fc6113969eb5eb410e1bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988944"
---
# <a name="imsrdpclientnonscriptable5getremotemonitorsboundingbox-property"></a><span data-ttu-id="e1301-106">Свойство IMsRdpClientNonScriptable5:: Жетремотемониторсбаундингбокс</span><span class="sxs-lookup"><span data-stu-id="e1301-106">IMsRdpClientNonScriptable5::GetRemoteMonitorsBoundingBox property</span></span>

<span data-ttu-id="e1301-107">Задает ограничивающий прямоугольник удаленного монитора.</span><span class="sxs-lookup"><span data-stu-id="e1301-107">Specifies the bounding rectangle of the remote monitor.</span></span>

<span data-ttu-id="e1301-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e1301-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1301-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1301-109">Syntax</span></span>


```C++
HRESULT get_GetRemoteMonitorsBoundingBox(
  [out] LONG *pLeft,
  [out] LONG *pTop,
  [out] LONG *pRight,
  [out] LONG *pBottom
);
```



## <a name="property-value"></a><span data-ttu-id="e1301-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e1301-110">Property value</span></span>

<span data-ttu-id="e1301-111">Получает левую границу прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e1301-111">Receives the left edge of the rectangle.</span></span>

<span data-ttu-id="e1301-112">Получает верхний край прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e1301-112">Receives the top edge of the rectangle.</span></span>

<span data-ttu-id="e1301-113">Получает правую границу прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e1301-113">Receives the right edge of the rectangle.</span></span>

<span data-ttu-id="e1301-114">Получает нижнюю границу прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e1301-114">Receives the bottom edge of the rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1301-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1301-115">Remarks</span></span>

<span data-ttu-id="e1301-116">Все координаты находятся в координатах виртуального экрана, которые находятся относительно левого верхнего угла основного монитора.</span><span class="sxs-lookup"><span data-stu-id="e1301-116">All coordinates are in virtual screen coordinates, which are relative to the upper-left corner of the primary monitor.</span></span> <span data-ttu-id="e1301-117">Если это не основной монитор, некоторые или все из этих значений могут быть отрицательными.</span><span class="sxs-lookup"><span data-stu-id="e1301-117">If this is not the primary monitor, some or all of these values may be negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1301-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e1301-118">Requirements</span></span>



| <span data-ttu-id="e1301-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e1301-119">Requirement</span></span> | <span data-ttu-id="e1301-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e1301-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1301-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1301-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e1301-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1301-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e1301-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1301-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e1301-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e1301-124">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="e1301-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e1301-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1301-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1301-126"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e1301-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e1301-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1301-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1301-128"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e1301-129">IID</span><span class="sxs-lookup"><span data-stu-id="e1301-129">IID</span></span><br/>                      | <span data-ttu-id="e1301-130">IID \_ IMsRdpClientNonScriptable5 определен как 4f6996d5-d7b1-412c-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="e1301-130">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1301-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1301-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1301-132">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="e1301-132">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





