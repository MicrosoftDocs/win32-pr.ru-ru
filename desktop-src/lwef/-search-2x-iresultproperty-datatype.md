---
title: Свойство DataType Иресултпроперти (Вдсшаредидл. h)
description: Тип данных Properties.
ms.assetid: 2bf83256-0d69-48f2-aa7d-d34dcba17050
keywords:
- Свойства DataType устаревшие функции среды Windows
- Свойство DataType устаревшие компоненты среды Windows, интерфейс Иресултпроперти
- Интерфейс Иресултпроперти устаревшие функции среды Windows, свойство DataType
topic_type:
- apiref
api_name:
- IResultProperty.DataType
- IResultProperty.get_DataType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d887642594ed5ac7f78de1d4eac76fb4709f0dfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701061"
---
# <a name="iresultpropertydatatype-property"></a><span data-ttu-id="df2ab-106">Иресултпроперти: свойство Ататипе:D</span><span class="sxs-lookup"><span data-stu-id="df2ab-106">IResultProperty::DataType property</span></span>

> [!NOTE]
> <span data-ttu-id="df2ab-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="df2ab-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="df2ab-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="df2ab-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="df2ab-109">Тип данных Properties.</span><span class="sxs-lookup"><span data-stu-id="df2ab-109">A properties data type.</span></span>

<span data-ttu-id="df2ab-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="df2ab-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df2ab-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df2ab-111">Syntax</span></span>


```C++
HRESULT get_DataType(
  [out, retval] VARTYPE *vt
);
```



## <a name="property-value"></a><span data-ttu-id="df2ab-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="df2ab-112">Property value</span></span>

<span data-ttu-id="df2ab-113">Возвращает указатель на тип данных Properties.</span><span class="sxs-lookup"><span data-stu-id="df2ab-113">returns a pointer to the properties data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="df2ab-114">Требования</span><span class="sxs-lookup"><span data-stu-id="df2ab-114">Requirements</span></span>



| <span data-ttu-id="df2ab-115">Требование</span><span class="sxs-lookup"><span data-stu-id="df2ab-115">Requirement</span></span> | <span data-ttu-id="df2ab-116">Значение</span><span class="sxs-lookup"><span data-stu-id="df2ab-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="df2ab-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df2ab-117">Minimum supported client</span></span><br/> | <span data-ttu-id="df2ab-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="df2ab-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="df2ab-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df2ab-119">Minimum supported server</span></span><br/> | <span data-ttu-id="df2ab-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="df2ab-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="df2ab-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="df2ab-121">Redistributable</span></span><br/>          | <span data-ttu-id="df2ab-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="df2ab-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="df2ab-123">Header</span><span class="sxs-lookup"><span data-stu-id="df2ab-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="df2ab-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="df2ab-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





