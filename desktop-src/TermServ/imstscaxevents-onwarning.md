---
title: Имстскаксевентс, метод OnWarning
description: Вызывается, когда клиентский элемент управления обнаруживает неустранимое условие ошибки.
ms.assetid: af43d3aa-0ae8-4721-b85d-bb043b20dc40
ms.tgt_platform: multiple
keywords:
- Метод OnWarning службы удаленных рабочих столов
- Метод OnWarning службы удаленных рабочих столов, интерфейс Имстскаксевентс
- Интерфейс Имстскаксевентс службы удаленных рабочих столов, метод OnWarning
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnWarning
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadc7013f34c93406f93841896a9041bbb1b7cfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802711"
---
# <a name="imstscaxeventsonwarning-method"></a><span data-ttu-id="7a207-106">Метод Имстскаксевентс:: OnWarning</span><span class="sxs-lookup"><span data-stu-id="7a207-106">IMsTscAxEvents::OnWarning method</span></span>

<span data-ttu-id="7a207-107">Вызывается, когда клиентский элемент управления обнаруживает неустранимое условие ошибки.</span><span class="sxs-lookup"><span data-stu-id="7a207-107">Called when the client control encounters an error condition that is not fatal.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a207-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a207-108">Syntax</span></span>


```C++
void OnWarning(
  [in] long warningCode
);
```



## <a name="parameters"></a><span data-ttu-id="7a207-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a207-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a207-110">*варнингкоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a207-110">*warningCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a207-111">Код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7a207-111">The error code.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="7a207-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="7a207-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="7a207-113">Кэш точечных рисунков поврежден.</span><span class="sxs-lookup"><span data-stu-id="7a207-113">Bitmap cache is corrupt.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a207-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a207-114">Return value</span></span>

<span data-ttu-id="7a207-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7a207-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a207-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a207-116">Remarks</span></span>

<span data-ttu-id="7a207-117">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7a207-117">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a207-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7a207-118">Requirements</span></span>



| <span data-ttu-id="7a207-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7a207-119">Requirement</span></span> | <span data-ttu-id="7a207-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7a207-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a207-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a207-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7a207-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a207-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7a207-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a207-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7a207-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a207-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7a207-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7a207-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a207-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a207-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a207-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7a207-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a207-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a207-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a207-129">IID</span><span class="sxs-lookup"><span data-stu-id="7a207-129">IID</span></span><br/>                      | <span data-ttu-id="7a207-130">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="7a207-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="7a207-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a207-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a207-132">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="7a207-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





