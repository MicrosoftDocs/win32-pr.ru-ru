---
title: Свойство DisplayName Иресултпроперти (Вдсшаредидл. h)
description: Локализованное отображаемое имя свойства.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Свойства DisplayName устаревшие функции среды Windows
- Свойства DisplayName устаревшие компоненты среды Windows, интерфейс Иресултпроперти
- Интерфейс Иресултпроперти устаревшие функции среды Windows, свойство DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f36aa934d2ddf31d841478cef1cb9a33b0531224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136482"
---
# <a name="iresultpropertydisplayname-property"></a><span data-ttu-id="f0e47-106">Иресултпроперти: свойство Исплайнаме:D</span><span class="sxs-lookup"><span data-stu-id="f0e47-106">IResultProperty::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="f0e47-107">Windows Desktop Search 2. x — это устаревшая технология, которая изначально была доступна в качестве надстройки для Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f0e47-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="f0e47-108">В более поздних выпусках используйте [API поиска Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="f0e47-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="f0e47-109">Локализованное отображаемое имя свойства.</span><span class="sxs-lookup"><span data-stu-id="f0e47-109">Localized display name of the property.</span></span>

<span data-ttu-id="f0e47-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f0e47-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e47-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0e47-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="f0e47-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f0e47-112">Property value</span></span>

<span data-ttu-id="f0e47-113">Возвращает указатель на локализованное отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="f0e47-113">returns a pointer to the localized display name.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e47-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f0e47-114">Requirements</span></span>



| <span data-ttu-id="f0e47-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f0e47-115">Requirement</span></span> | <span data-ttu-id="f0e47-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f0e47-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e47-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0e47-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e47-118">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0e47-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f0e47-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0e47-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e47-120">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0e47-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f0e47-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f0e47-121">Redistributable</span></span><br/>          | <span data-ttu-id="f0e47-122">Windows Desktop Search (WDS) версии 2.6.5</span><span class="sxs-lookup"><span data-stu-id="f0e47-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="f0e47-123">Header</span><span class="sxs-lookup"><span data-stu-id="f0e47-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0e47-124"><dt>Вдсшаредидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0e47-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





